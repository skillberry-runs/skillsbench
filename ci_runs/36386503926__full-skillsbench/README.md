# full / skillsbench — run 36386503926

A cap-evolve benchmark run, backfilled on 2026-11-18 from its CI artifact (the run predates per-run folders, so `recipe/` is missing). Its row is on the [benchmark-runs dashboard](https://skillberry-runs.github.io/dashboard/).

[Actions run](https://github.com/skillberry-ai/cap-evolve/actions/runs/36386503926) · [PR #556](https://github.com/skillberry-ai/cap-evolve/pull/556) · [commit `606e6c874`](https://github.com/skillberry-ai/cap-evolve/tree/606e6c874a61d4984020f5eb2363d5ed9093cc20)

## Run

| | |
|---|---|
| Benchmark / tier | `skillsbench` / `full` |
| Source | PR #556 |
| Date (UTC) | 2026-09-28T06:27:24Z |
| Conclusion | failure |
| Agent model | `ibm-ete-int/aws/gpt-oss-120b` |
| Optimizer model | `ibm-ete-int/claude-opus-4-8` |
| Algorithm | `hill-climb-all` |
| Iterations / trials | 10 / 1 |
| Gate (k·SE) | 1.0 |

## Results

- No suite result: the run did not finish successfully (see `report.md` and the Actions run).

Details per task are in `report.md`.

## Files

- [`report.md`](report.md) — the run's metrics report (also its PR comment)
- [`runmeta.json`](runmeta.json) — how the run was launched: models, tier, iterations, trials, commit
- [`metrics.jsonl`](metrics.jsonl) — one row per task: baseline vs optimized reward
- `recipe/` was not available for this run (published from its CI artifact); the tier's definition is `ci/benchmarks/skillsbench/full/` at the commit above.

## Re-running it

The tier's tasks, split and overrides are committed in cap-evolve under `ci/benchmarks/skillsbench/full/`. To run the same configuration again, dispatch the Benchmarks workflow on a branch at the commit above:

```bash
gh workflow run benchmarks.yml -R skillberry-ai/cap-evolve --ref <branch> -f tier=full -f bench=skillsbench \
  -f iterations=10 -f trials=1 -f agent_model=ibm-ete-int/aws/gpt-oss-120b \
  -f optimizer_model=ibm-ete-int/claude-opus-4-8 -f algorithm=hill-climb-all
```

Model calls are sampled, so a re-run gives a new measurement, not the same numbers.
