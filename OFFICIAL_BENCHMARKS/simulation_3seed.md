# 3-Seed Simulation — K_AUTOROUND

**Seeds:** `18193` · `49530` · `83729`

**Seed method:** `sha256("K_AUTOROUND")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `K_AUTOROUND`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 6.9103 | 0.0146 | ±0.0286 |
| throughput_tokens_per_sec | 5566.4667 | 30.7827 | ±60.3341 |
| p50_latency_ms | 49.11 | 4.6103 | ±9.0362 |
| p99_latency_ms | 127.7567 | 1.5085 | ±2.9567 |
| ttft_ms | 31.92 | 1.4142 | ±2.7718 |
| mmlu_proxy | 0.748 | 0.0 | ±0.0 |
| hellaswag_proxy | 0.8145 | 0.0168 | ±0.0329 |
| truthfulqa_proxy | 0.5745 | 0.0145 | ±0.0284 |
| arc_proxy | 0.662 | 0.0159 | ±0.0312 |
| complexity_cyclomatic | 4.1433 | 0.0377 | ±0.0739 |
| maintainability_index | 67.5533 | 4.1342 | ±8.103 |
| security_issues_high | 0.6667 | 0.4714 | ±0.9239 |
| dependency_freshness_pct | 80.9333 | 6.8825 | ±13.4897 |
| test_coverage_pct | 60.3333 | 0.2357 | ±0.462 |
| doc_coverage_pct | 59.1 | 2.2627 | ±4.4349 |
| memory_mb | 133.1333 | 12.068 | ±23.6533 |
| gpu_util_pct | 68.4333 | 6.6939 | ±13.12 |
| openssf_score | 6.09 | 0.3394 | ±0.6652 |
| eu_ai_act_compliance_pct | 80.4 | 0.5657 | ±1.1088 |
| slsa_level | 2.0 | 0.0 | ±0.0 |

## Per-Seed Raw Results

| Metric | Seed 18193 | Seed 49530 | Seed 83729 |
|--------|------------|------------|------------|
| trl_score | 6.9 | 6.931 | 6.9 |
| throughput_tokens_per_sec | 5544.7 | 5610.0 | 5544.7 |
| p50_latency_ms | 52.37 | 42.59 | 52.37 |
| p99_latency_ms | 126.69 | 129.89 | 126.69 |
| ttft_ms | 30.92 | 33.92 | 30.92 |
| mmlu_proxy | 0.748 | 0.748 | 0.748 |
| hellaswag_proxy | 0.8264 | 0.7907 | 0.8264 |
| truthfulqa_proxy | 0.5848 | 0.554 | 0.5848 |
| arc_proxy | 0.6733 | 0.6395 | 0.6733 |
| complexity_cyclomatic | 4.17 | 4.09 | 4.17 |
| maintainability_index | 64.63 | 73.4 | 64.63 |
| security_issues_high | 1 | 0 | 1 |
| dependency_freshness_pct | 85.8 | 71.2 | 85.8 |
| test_coverage_pct | 60.5 | 60.0 | 60.5 |
| doc_coverage_pct | 57.5 | 62.3 | 57.5 |
| memory_mb | 124.6 | 150.2 | 124.6 |
| gpu_util_pct | 63.7 | 77.9 | 63.7 |
| openssf_score | 6.33 | 5.61 | 6.33 |
| eu_ai_act_compliance_pct | 80.0 | 81.2 | 80.0 |
| slsa_level | 2 | 2 | 2 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._