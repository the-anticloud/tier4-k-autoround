# Radon_Complexity_Lab_Results
**Project:** `K_AUTOROUND` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `10`
- **average_complexity:** `{'grade': 'B', 'score': 5.505813953488372}`
- **complexity_grade:** `B`
- **complexity_score:** `5.505813953488372`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_AUTOROUND\UPSTREAM\setup.py - A (61.63)
E:\fenta\Downloads\Th`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_AUTOROUND\UPSTREAM\setup.py
    F 36:0 get_build_version - B (6)
    F 86:0 is_cpu_env - A (4)
    F 25:0 is_commit_on_tag - A (2)
    F 72:0 is_hpu_available - A (2)
    F 104:0 fetch_requirements - A (2)
    F 60:0 is_habana_framework_installed - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_AUTOROUND\UPSTREAM\auto_round\autoround.py
    F 334:0 _normalize_alg_configs - F (53)
    F 154:0 _select_rtn_compressor_base_cls - D (26)
    M 532:4 _CompressorBuilder.__new__ - D (24)
    C 511:0 _CompressorBuilder - C (15)
    F 281:0 _discover_alg_config_fields - B (8)
    C 687:0 AutoRound - B (8)
    M 729:4 AutoRound.__new__ - B (7)
    F 77:0 _resolve_quant_config_for_routing - B (6)
    F 138:0 _build_model_type_ctor_kwargs - B (6)
    F 49:0 _get_compressor_class - A (5)
    F 263:0 _iter_registered_alg_configs - A (5)
    F 307:0 _filter_supported_entry_kwargs - A (4)
    M 522:4 _CompressorBuilder._resolve_config - A (4)
    F 101:0 _build_model_free_compressor - A (3)
    F 330:0 _owning_algorithm_names - A (3)
    F 505:0 _prepare_entry_kwargs - A (3)
    F 319:0 _split_entry_kwargs - A (2)
    C 796:0 AutoRoundLLM - A (2)
    C 802:0 AutoRoundAdam - A (2)
    C 809:0 AutoRoundMLLM - A (2)
    C 815:0 AutoRoundDiffusion - A (2)
    F 326:0 _config_fields - A (1)
    M 797:4 AutoRoundLLM.__new__ - A (1)
    M 803:4 AutoRoundAdam.__new__ - A (1)
    M 810:4 AutoRoundMLLM.__new__ - A (1)
    M 816
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_