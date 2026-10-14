# Students — OPENMCT

**Project:** OPENMCT  
**Category:** SPACE_AEROTECH  
**Upstream:** https://github.com/nasa/openmct  
**Pinned commit:** `b589f7f4de94f847aa8660e90fd85c87fa5e4026`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `fd7d9d7aa13e5107068fd2436956df6c028ae21d8cf690f2adcea4a9af208145`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `b589f7f4de94f847aa8660e90fd85c87fa5e4026`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `fd7d9d7aa13e5107068fd2436956df6c028ae21d8cf690f2adcea4a9af208145`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
