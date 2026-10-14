# Onboarding — OPENMCT

**Project:** OPENMCT  
**Category:** SPACE_AEROTECH  
**Upstream:** https://github.com/nasa/openmct  
**Pinned commit:** `b589f7f4de94f847aa8660e90fd85c87fa5e4026`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `fd7d9d7aa13e5107068fd2436956df6c028ae21d8cf690f2adcea4a9af208145`  
**Date:** October 2026

## First hour

1. Read `README.md` — what the project is and what it measures.
2. Read `ISOLATED_LAB_RESULTS/03_Result_Register.md` — the 16 checks and their
   evidence hashes.
3. Run the suite: `python tools/run_bench.py --out BENCH.json`.
4. Verify a hash: recompute SHA3-256 of a file in `04_Evidence/` and compare.

## First day

- `10_TECHNICAL_HANDOFF` — architecture and interfaces
- `11_TUTORIAL_DEVELOPERS` — build and test
- `18_COMMAND_LINE_INTERFACE` — CLI reference
- `27_DEPENDENCIES` — the offline dependency mirror

## Getting help

lois@0-1.gg · 0-1.gg
