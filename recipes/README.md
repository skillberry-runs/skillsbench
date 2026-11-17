# recipes/

cap-evolve project configs (the `capevolve.*.yaml` + `split_ids.*.json` a rerun needs),
organized one subdirectory per experiment configuration. Paired with `../artifacts/` (the
`seed`/`best` skill packages those recipes produced) — a recipe alone reruns the
experiment from scratch; the paired artifact is what it actually produced.

- `all/` — the two "sweep everything" variants: the full 87-task recipe (stalled at seed)
  and the derived 43-task runnable-subset recipe (reached an accepted candidate).
- `task-by-task/` — one project per SkillsBench task, 87 in total.
- `a0f-full-vocab/` — arm A0f: one project per task, same shape as `task-by-task/` but
  `capability_path` points at the shared 196-skill union instead of the task's own seed
  skills, at `max_iterations: 0`. 10 of 87 so far; see `a0f-full-vocab/README.md`.

Train-test-split recipes are not yet harvested here — that experiment is still running.

## Rerunning against cap-evolve today

- **Which cap-evolve.** These runs didn't record the cap-evolve commit they used. They ran from
  cap-evolve worktrees (`intake_skillbench_*`). The last cap-evolve commit with the layout these
  files refer to is `bbe99a5` on `main` (2026-11-08).
- **Paths since cap-evolve [#959](https://github.com/skillberry-ai/cap-evolve/pull/959) (2026-11-08):**
  `examples/tau2_airline/adapters/` is now `benchmarks/tau2/examples/airline/adapters/`,
  `examples/skillsbench/` is now `benchmarks/skillsbench/examples/shared_skills/`, and
  `templates/adapters/skillsbench/` is now `benchmarks/skillsbench/template/`. Here they appear only in
  comments (e.g. `task-by-task/_shared/adapters/anthropic_env.py`); no script or config depends on them.
- **The branch name.** This repo was cap-evolve's `skillsbench-history` branch until 2026-11-09;
  where a doc says "skillsbench-history", read this repo.
