# Technical Architecture — OPENMCT

**Upstream:** [https://github.com/nasa/openmct](https://github.com/nasa/openmct)
**License:** Apache 2.0
**Category:** SPACE_AEROTECH
**Anticloud Integration:** PAX L5 Narrow L2 General 27B + AIOSS + Offline-First

## Upstream Description

NASA open mission control framework

## Anticloud Architectural Changes

1. PAX L5 Narrow L2 General 27B local mission planning and anomaly detection — air-gapped
2. AIOSS tamper-evident telemetry log with SHA3-256 integrity
3. AES-256 encryption for all mission-critical data
4. Single-binary flight software package deployable on radiation-hardened hardware
5. Zero-cloud: all inference runs on-vehicle or at ground station
6. GPU/CPU equalizer: scales from embedded ARM to ground station GPU cluster
7. Offline trajectory optimization replacing cloud compute APIs
8. Open command protocol replacing proprietary ground control interfaces

## Integration Points

- **PAX Inference Socket:** Local HTTP endpoint at `127.0.0.1:11434/v1/chat` — same OpenAI-compatible API, zero cloud
- **AIOSS Hook:** Every write operation calls `aioss_append(event, payload)` before commit
- **Encryption Layer:** All file I/O routed through `anticloud_crypto.encrypt_at_rest()`
- **Single Binary Build:** `pyinstaller anticloud_openmct.spec` or `go build -o openmct`

## Deployment Modes

| Mode | Hardware | Notes |
| --- | --- | --- |
| Edge CPU | Raspberry Pi 4 / Intel NUC | Full feature set, PAX on CPU |
| Desktop GPU | RTX 3060 / A10 | PAX GPU inference, <1s latency |
| Server | 2× A100 | Full batch throughput |
| Air-gapped | Any x86/ARM | Zero network dependency |