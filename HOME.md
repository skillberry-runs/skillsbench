<div class="generated">
<!-- Front page of this benchmark's section on the dashboard (https://skillberry-runs.github.io/dashboard/skillsbench/). Moved here from cap-evolve's site/skillsbench/index.html on 2026-11-16. -->
<h1>SkillsBench experiments</h1>
<p class="lead">
Three experiments cap-evolve has run against
<a href="https://github.com/benchflow-ai/skillsbench">BenchFlow's SkillsBench</a> (87 tasks,
8 categories). Each card is level 1 — a row on the <a href="../">Benchmarks</a>
dashboard — with links onward to level 2 (a heatmap or per-task table) and, where it exists,
level 3 (a per-task report).
</p>
<div class="callout callout-warn">
<div class="callout-title">Level 3 is not fully on-site yet</div>
<p>
Per-task reports below are rendered from the
<a class="ext-link" href="https://github.com/skillberry-runs/skillsbench" title="Private repo: only skillberry-runs org members can open this (others get a 404)">skillberry-runs/skillsbench (private)</a>
repo, but the skill packages they discuss (<code>seed/</code>, <code>best/</code>,
<code>PROCESS.md</code> under <code>artifacts/</code> — about 27 MB) are not published on this site.
That repo is <strong>private</strong>: the links to it on each report page, marked
<a class="ext-link" href="#">GitHub (private)</a>, open only for members of the
<code>skillberry-runs</code> GitHub org. Anyone else gets a 404, which means no access, not a broken link.
</p>
</div>
<h2 id="task-by-task">task-by-task — one skill per task (87 tasks)</h2>
<p>
EvoSkills-style: each task gets its own optimized skill, seeded from the task's own
<code>environment/skills/</code>. The full 3-level drill-down exists for this experiment.
</p>
<div class="card-grid reveal">
<a class="card" href="results/task-by-task-87/summary.html">
<div class="card-title">Level 2 — summary</div>
<p class="card-desc">Aggregate pass rate, per-category breakdown, comparison to the EvoSkills 71.1% headline.</p>
</a>
<a class="card" href="ui/heatmap.html">
<div class="card-title">Level 2 — heatmap</div>
<p class="card-desc">Interactive per-task × per-candidate score grid, 87 tasks. Click a task name for its report.</p>
</a>
<a class="card" href="reports/README.html">
<div class="card-title">Level 3 — per-task reports</div>
<p class="card-desc">87 reports: why a task moved (or didn't), and what it teaches.</p>
</a>
</div>
<h2 id="transfer-eval-8fold">transfer-eval-8fold — zero-shot skill transfer (8 folds)</h2>
<p>
Does a skill optimized for one task carry over to a different task, evaluated zero-shot
(<code>--max-iterations 0</code>, no adaptation)? No level 3 — this experiment doesn't
produce per-task skill artifacts of its own, only a comparison table.
</p>
<div class="card-grid reveal">
<a class="card" href="results/transfer-eval-8fold/summary.html">
<div class="card-title">Level 2 — summary</div>
<p class="card-desc">The full 8-fold writeup, reading, methodological caveats, and CCC/LSF operational notes.</p>
</a>
<a class="card" href="results/transfer-eval-8fold/heatmap.html">
<div class="card-title">Level 2 — heatmap</div>
<p class="card-desc">Transfer reward vs. each test task's own native seed/optimized score, 8 folds.</p>
</a>
</div>
<h2 id="runnable-subset-43">runnable-subset-43 — whole-suite optimization (43 tasks)</h2>
<p>
One shared skill package optimized across all 43 tasks that actually run on our CCC podman
setup. Cancelled at iteration 4 (optimizer hang); best accepted candidate is <code>cand_0002</code>.
</p>
<div class="card-grid reveal">
<a class="card" href="results/runnable-43task-opt/summary.html">
<div class="card-title">Level 2 — summary</div>
<p class="card-desc">Aggregate reward, iteration table, passing/partial/regressed task lists, cost and wall clock.</p>
</a>
<a class="card" href="results/runnable-43task-opt/heatmap.html">
<div class="card-title">Level 2 — heatmap</div>
<p class="card-desc">Seed-baseline reward per task, annotated with cand_0002's pass/partial outcome. No full candidate × task matrix exists for this run — see the page for why.</p>
</a>
</div>
<h2 id="more">More</h2>
<div class="card-grid reveal">
<a class="card" href="insights/SKILLS_TASKS_MAP.html">
<div class="card-title">Skills ↔ tasks map</div>
<p class="card-desc">All 87 tasks and their skills, numbered and cross-referenced, plus a per-category train/test split for skill optimization.</p>
</a>
<a class="card" href="insights/SKILLSBENCH_INVENTORY.html">
<div class="card-title">Task inventory</div>
<p class="card-desc">All 87 tasks by category, difficulty, task type, and shipped skills.</p>
</a>
</div>
</div>
