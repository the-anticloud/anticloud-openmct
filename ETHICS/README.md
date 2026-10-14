# Ethics — OPENMCT

**Project:** OPENMCT  
**Category:** SPACE_AEROTECH  
**Upstream:** https://github.com/nasa/openmct  
**Pinned commit:** `b589f7f4de94f847aa8660e90fd85c87fa5e4026`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `fd7d9d7aa13e5107068fd2436956df6c028ae21d8cf690f2adcea4a9af208145`  
**Date:** October 2026

## Position

OPENMCT is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
