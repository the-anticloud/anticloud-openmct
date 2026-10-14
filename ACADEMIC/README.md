# Academic Use — OPENMCT

**Project:** OPENMCT  
**Category:** SPACE_AEROTECH  
**Upstream:** https://github.com/nasa/openmct  
**Pinned commit:** `b589f7f4de94f847aa8660e90fd85c87fa5e4026`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `fd7d9d7aa13e5107068fd2436956df6c028ae21d8cf690f2adcea4a9af208145`  
**Date:** October 2026

## Scope

OPENMCT is available for academic research under the Apache 2.0 terms of the
Anticommons 0.1.0 dual licence. Citation details are in `23_HOW_TO_CITE`.

## What is available to researchers

- The full upstream source, pinned at `b589f7f4de94f847aa8660e90fd85c87fa5e4026`
- The 16-check assurance register with per-check evidence and hashes
- The AIOSS ledger attesting the project artifacts
- Benchmark output in `BENCH.json`

## Reproducing the result

```
python tools/run_bench.py --out BENCH.json
```

Then recompute any row's SHA3-256 from `ISOLATED_LAB_RESULTS/04_Evidence/`.

## Contact

lois@0-1.gg · 0-1.gg
