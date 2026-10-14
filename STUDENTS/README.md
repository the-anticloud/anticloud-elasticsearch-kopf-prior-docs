# Students — ELASTICSEARCH_KOPF_PRIOR_DOCS

**Project:** ELASTICSEARCH_KOPF_PRIOR_DOCS  
**Category:** ONLINE_RETAIL  
**Upstream:** https://github.com/lmenezes/elasticsearch-kopf  
**Pinned commit:** `31a58acf4117794389af5821b391539604bb1b50`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `ffc56e4bc9c8214db93b995a53245de063504e93114b3039dfbd739085f6293f`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `31a58acf4117794389af5821b391539604bb1b50`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `ffc56e4bc9c8214db93b995a53245de063504e93114b3039dfbd739085f6293f`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
