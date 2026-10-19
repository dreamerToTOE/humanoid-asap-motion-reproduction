# Reproduction Execution Plan / 分阶段复现计划

**Project:** ASAP phase-based motion tracking, retargeting, delta action model and Sim2Sim
**Status:** PLANNED; no results have been executed or validated.

## Prior-learning checkpoint (required before coding)
Produce an explanation of (1) scientific/engineering problem; (2) main solution and why; (3) innovations vs baselines; (4) full published experiments; (5) which parts are reproducible from open source; (6) proposed numerical simulation scope. Do not silently omit experiments and do not claim original quantitative reproduction based on simulation visuals alone.

## Gates
- **A0** — paper-code-data: record setup and acceptance evidence in docs/PROGRESS.md; if incomplete mark BLOCKED with cause.
- **A1** — install: record setup and acceptance evidence in docs/PROGRESS.md; if incomplete mark BLOCKED with cause.
- **A2** — tracking: record setup and acceptance evidence in docs/PROGRESS.md; if incomplete mark BLOCKED with cause.
- **A3** — retargeting: record setup and acceptance evidence in docs/PROGRESS.md; if incomplete mark BLOCKED with cause.
- **A4** — delta model: record setup and acceptance evidence in docs/PROGRESS.md; if incomplete mark BLOCKED with cause.
- **A5** — fine-tune: record setup and acceptance evidence in docs/PROGRESS.md; if incomplete mark BLOCKED with cause.
- **A6** — Sim2Sim: record setup and acceptance evidence in docs/PROGRESS.md; if incomplete mark BLOCKED with cause.

## Project-specific actions
1. Read ASAP paper fully and make an equation-by-equation paper ↔ code ↔ experiment matrix before environment installation.
2. Audit HumanoidVerse/IsaacGym/IsaacLab/Genesis compatibility, physical data availability, models and dataset terms.
3. Reproduce phase-based motion tracking baseline on one reproducible sequence and report trackable pose/joint error metrics.
4. Reproduce the retargeting transforms and quantify mismatch between human source and humanoid reference trajectories.
5. Implement/evaluate delta action model only if original training data and supervision can be accessed; otherwise document blocked dependency.
6. Contrast tracking-policy fine-tuning with/without delta model with fixed budget and report MuJoCo Sim2Sim if available.

## Minimum acceptance
- Reproducible pinned source SHA, environment manifest and deterministic smoke test.
- Paper/baseline code map and honest difference log.
- A run manifest for **each** metric or figure; no fabricated results.
- At least 3 random seeds *if computationally feasible*; otherwise explicit budget and uncertainty.
- Held-out evaluation conditions separated from training, raw episodes and summary plots.
- Metrics: motion-tracking pose errors, joint errors, task completion, delta prediction error, transfer/generalization.
- Completion report must distinguish validated claims, partial reproductions, extra extensions, and blocked claims.

## Stop/go rules
Stop after three distinct failed attempts on the same blocker; escalate cause and proposed alternatives. Do not silently lower model/environment complexity or invent synthetic 'paper-equivalent' evidence. Prefer numerical simulation verification where physical testing unavailable, clearly labeled. No unapproved long/high-cost runs.
