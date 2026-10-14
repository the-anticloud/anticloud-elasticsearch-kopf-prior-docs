# Educators — ELASTICSEARCH_KOPF_PRIOR_DOCS

**Project:** ELASTICSEARCH_KOPF_PRIOR_DOCS  
**Category:** ONLINE_RETAIL  
**Upstream:** https://github.com/lmenezes/elasticsearch-kopf  
**Pinned commit:** `31a58acf4117794389af5821b391539604bb1b50`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `ffc56e4bc9c8214db93b995a53245de063504e93114b3039dfbd739085f6293f`  
**Date:** October 2026

## Teaching with ELASTICSEARCH_KOPF_PRIOR_DOCS

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `ffc56e4bc9c8214db93b995a53245de063504e93114b3039dfbd739085f6293f` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
