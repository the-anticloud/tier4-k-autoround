# HF_Leaderboard_Lab_Results

**Project:** `K_AUTOROUND`  
**Tier:** `TIER_4_INFERENCE_AGENTS`  
**Slug:** `intel/auto-round`  
**Commit:** `5606837a3842`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **49.95 ms** |
| Min latency | 43.04 ms |
| Max latency | 57.03 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **38** |
| Tokenization latency | 1.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5882 |
| Classification latency | 85.74 ms |
| Status | **PASS** |

**Input text tokenized:**
```
K_AUTOROUND (intel/auto-round) — 1000 files, 333904 source lines, licence Apache-2.0, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'k', '_', 'auto', '##rou', '##nd', '(', 'intel', '/', 'auto', '-', 'round', ')', '—', '1000', 'files', ',', '333', '##90', '##4']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_