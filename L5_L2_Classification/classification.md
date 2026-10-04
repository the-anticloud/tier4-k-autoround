# L5 Narrow / L2 General Classification — K_AUTOROUND
**Platform:** Anticloud | **Tier:** TIER_4_INFERENCE_AGENTS | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
K_AUTOROUND specializes in AutoRound quantization for the Anticloud model corpus. Narrow scope: INT4/INT8 quantization of PAX 27B and TIER_4 inference models with Anticloud-specific calibration data. Does not attempt general quantization of arbitrary architectures.

## L2 General
L2 General: AutoRound-quantized GGUF artifacts are consumed by all 9 tiers. TIER_7 biosignal and TIER_9 robotics deployments both load the same quantized PAX 27B via identical GGUF interface.

## PAX 27B Integration
PAX 27B is quantized by K_AUTOROUND using corpus-specific calibration data. Every quantized artifact is AIOSS-chained with its accuracy benchmark delta before deployment.

## AIOSS Audit Chain
Every quantization artifact (source weight hash + config hash + output weight hash + accuracy delta) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
NIST SP 800-133 (cryptographic module integrity during weight handling). ISO/IEC 42001 (document accuracy tradeoffs).
