<div class="generated">
<!-- Generated once (2026-11-16) from this folder's JSON by cap-evolve's scripts/build_skillsbench_site.py; the experiment is finished, so it does not need regenerating. -->
<h1>transfer-eval-8fold — heatmap</h1>
<p class="lead">Zero-shot skill transfer, 8 folds, generated 2026-09-02.</p>
<div class="callout callout-warn">
<div class="callout-title">Read this before the table</div>
<ul>
<li>Every fold reports best_id='seed', test_reward == test_baseline_reward, test_delta == 0.0. This is an artifact of --max-iterations 0: the transfer project's seed IS the frozen donor skill and is the only artifact evaluated, so cap-evolve compares it against itself. Real transfer effect = transfer_reward - native_seed.</li>
<li>For tasks with status KILLED_ceiling, native_optimized is the in-loop val score (results.json 'best'), not a held-out test score, because final_test is null - the run was stopped on saturation before a held-out eval ran.</li>
<li>8 folds over 5 tasks in 2 domains; directional only.</li>
</ul>
</div>
<table>
<thead><tr>
<th>#</th><th>train task</th><th>test task</th><th>job</th><th>status</th>
<th>transfer reward</th><th>native seed</th><th>native optimized</th><th>transfer − native seed</th>
</tr></thead>
<tbody>
<tr><td>1</td><td><code>shock-analysis-demand</code></td><td><code>shock-analysis-supply</code></td><td>555427</td><td>DONE</td><td>0.10</td><td>0.00</td><td>0.20</td><td><span class="delta-pos">+0.10</span></td></tr><tr><td>2</td><td><code>shock-analysis-demand</code></td><td><code>weighted-gdp-calc</code></td><td>540431</td><td>DONE</td><td>0.20</td><td>0.80</td><td>1.00 ‡</td><td><span class="delta-neg">-0.60</span></td></tr><tr><td>3</td><td><code>shock-analysis-supply</code></td><td><code>shock-analysis-demand</code></td><td>543167</td><td>DONE</td><td>0.00</td><td>0.00</td><td>0.90</td><td><span class="delta-zero">0.00</span></td></tr><tr><td>4</td><td><code>shock-analysis-supply</code></td><td><code>weighted-gdp-calc</code></td><td>540433</td><td>DONE</td><td>0.30</td><td>0.80</td><td>1.00 ‡</td><td><span class="delta-neg">-0.50</span></td></tr><tr><td>5</td><td><code>weighted-gdp-calc</code></td><td><code>shock-analysis-demand</code></td><td>543168</td><td>DONE</td><td>0.00</td><td>0.00</td><td>0.90</td><td><span class="delta-zero">0.00</span></td></tr><tr><td>6</td><td><code>weighted-gdp-calc</code></td><td><code>shock-analysis-supply</code></td><td>543169</td><td>DONE</td><td>0.10</td><td>0.00</td><td>0.20</td><td><span class="delta-pos">+0.10</span></td></tr><tr><td>7</td><td><code>exam-block-sequencing</code></td><td><code>paratransit-routing</code></td><td>543170</td><td>DONE</td><td>0.20</td><td>0.00</td><td>1.00 ‡</td><td><span class="delta-pos">+0.20</span></td></tr><tr><td>8</td><td><code>paratransit-routing</code></td><td><code>exam-block-sequencing</code></td><td>543171</td><td>DONE</td><td>0.40</td><td>0.10</td><td>1.00 ‡</td><td><span class="delta-pos">+0.30</span></td></tr>
</tbody>
</table>
<p><small>‡ in-loop val score, not a held-out test score (task is <code>KILLED_ceiling</code> in results.json).</small></p>
<p><a href="summary.html">← back to the fold-by-fold writeup</a></p>
</div>
