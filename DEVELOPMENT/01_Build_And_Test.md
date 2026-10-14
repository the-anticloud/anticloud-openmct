# Build and Test

**Project:** `OPENMCT`
**Upstream:** https://github.com/nasa/openmct
**License:** Apache 2.0

## Quick Start

```bash
git clone https://github.com/nasa/openmct
cd openmct
pip install -r requirements-anticloud.txt
python anticloud_main.py --offline --pax-local
```

## Anticloud Improvements Applied

1. PAX L5 Narrow L2 General 27B local mission planning and anomaly detection — air-gapped
2. AIOSS tamper-evident telemetry log with SHA3-256 integrity
3. AES-256 encryption for all mission-critical data
4. Single-binary flight software package deployable on radiation-hardened hardware
5. Zero-cloud: all inference runs on-vehicle or at ground station
6. GPU/CPU equalizer: scales from embedded ARM to ground station GPU cluster
7. Offline trajectory optimization replacing cloud compute APIs
8. Open command protocol replacing proprietary ground control interfaces

## Benchmark Targets

| Metric | Target |
| --- | --- |
| Latency | Primary inference task: <5s on CPU, <1s on GPU |
| Throughput | Batch processing: >100 items/hour on single CPU server |
| Memory | <8GB RAM for standard deployment |
| Accuracy | Task-specific accuracy within 5% of cloud-API baseline |

## Build Status

Not yet measured. Run verified build and record actual figures above.
