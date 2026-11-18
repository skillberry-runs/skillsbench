## Smoke suite — skillsbench  (train-fit, no holdout)

Agent `aws/gpt-oss-120b` · optimizer Claude Code `claude-opus-4-8` · 1 iteration(s) · **all 10 tasks optimized together** · `train==val==test` (FIT metric, not a generalization/held-out claim).

| bench | task | reward (base→opt) | Δ | note |
|---|---|---|---|:--:|
| skillsbench | `offer-letter-generator` | 0.000 → ⚠️ infra-error | — | ⚠️ |
| skillsbench | `exceltable-in-ppt` | 0.000 → ⚠️ infra-error | — | ⚠️ |
| skillsbench | `xlsx-recover-data` | 0.000 → ⚠️ infra-error | — | ⚠️ |
| skillsbench | `sales-pivot-analysis` | 0.000 → ⚠️ infra-error | — | ⚠️ |
| skillsbench | `invoice-fraud-detection` | 0.000 → ⚠️ infra-error | — | ⚠️ |
| skillsbench | `weighted-gdp-calc` | 0.000 → ⚠️ infra-error | — | ⚠️ |
| skillsbench | `financial-modeling-qa` | 0.000 → ⚠️ infra-error | — | ⚠️ |
| skillsbench | `pdf-excel-diff` | 0.000 → ⚠️ infra-error | — | ⚠️ |
| skillsbench | `pptx-reference-formatting` | 0.000 → ⚠️ infra-error | — | ⚠️ |
| skillsbench | `reserves-at-risk-calc` | 0.000 → ⚠️ infra-error | — | ⚠️ |

**Suite (train-fit):** mean reward 0.000 → 0.000 (Δ +0.000) · best = seed (no candidate beat baseline) · optimizer $1.01 over 1 iter(s) · 10 task(s) infra-errored

> No candidate was accepted, so base→opt is the seed against itself and Δ is 0.000 by construction. Re-scoring those same bytes for the finalize read 0.000 against the baseline's 0.000 — a spread of 0.000. That is this tier's re-measurement **noise**, not a change in the capability, and it is the floor any real effect here would have to clear.

### Iterations

| phase | iter | candidate | accepted | reward | optimizer $ | optimizer time | eval $ | eval time |
|---|:--:|---|:--:|---|---|---|---|---|
| baseline | — | `seed` | — | 0.000 | $0.0000 | 0s | $0.0000 | 1m41s |
| iterate | 1 | `cand_0001` | ❌ | 0.000 | $1.0056 | 4m18s | $0.0000 | 1m41s |
| finalize | — | `seed` | — | 0.000 | $0.0000 | 0s | $0.0000 | 1m41s |

**Totals:** optimizer $1.0056 over 4m18s · eval $0.0000 over 5m03s
