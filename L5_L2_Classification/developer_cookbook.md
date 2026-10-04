# Developer Cookbook — K_AUTOROUND
**Stack:** Python 3.11, PyTorch 2.10+, auto-round 0.3+, neural-compressor 2.5+, CUDA 12.x
**Domain:** LLM weight quantization: AutoRound INT4/INT8 for PAX 27B and TIER_4 models

## Quantize PAX 27B to INT4
```python
from k_autoround import AutoRoundQuantizer

quantizer = AutoRoundQuantizer(
    model_path="./pax-27b-fp16.safetensors",
    bits=4, group_size=128,
    calibration_dataset="./anticloud_calibration/",
    aioss_chain="./autoround.aioss"
)
result = quantizer.quantize(output_path="./pax-27b-q4.gguf")
print(f"Accuracy delta: {result.accuracy_delta:.3f}")
print(f"Compression: {result.compression_ratio:.1f}x")
print(f"Chain: {result.chain_hash}")
```

## Generate calibration dataset
```python
from k_autoround import CalibrationDataset
cal = CalibrationDataset.from_directory(
    "E:/fenta/Downloads/The Anticloud", n_samples=512
)
cal.save("./anticloud_calibration/")
```

## Benchmark quantized model
```python
bench = quantizer.benchmark(
    model_path="./pax-27b-q4.gguf",
    test_prompts="./anticloud_bench_prompts.jsonl"
)
print(f"Perplexity: {bench.perplexity:.2f}, Throughput: {bench.tokens_per_sec:.1f} tok/s")
```

## INT8 (lower accuracy loss)
```python
result8 = quantizer.quantize(bits=8, output_path="./pax-27b-q8.gguf")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
