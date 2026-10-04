# Deploy Guide — K_AUTOROUND
**Tier:** TIER_4_INFERENCE_AGENTS | **Stack:** Python 3.11, PyTorch 2.10+, auto-round 0.3+, neural-compressor 2.5+, CUDA 12.x
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, PyTorch 2.10+, auto-round 0.3+, neural-compressor 2.5+, CUDA 12.x. 80GB RAM for full PAX 27B quantization.

## Environment
A100 80GB GPU for PAX 27B; T4 for smaller models. 80GB RAM minimum. CUDA 12.x.

## AIOSS Integration
```bash
aioss init --module K_AUTOROUND --output ./k_autoround.aioss
aioss append --chain ./k_autoround.aioss --payload ./output.bin --module K_AUTOROUND
aioss verify --chain ./k_autoround.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_AUTOROUND",
    aioss_chain="./K_AUTOROUND.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_AUTOROUND.aioss --verbose
python -m K_AUTOROUND.tests.smoke
```
