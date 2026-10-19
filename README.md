# ASAP Humanoid Motion Reproduction | 人形全身动作跟踪复现

> Status: **PLANNED / 未开始复现** · Advanced/stretch humanoid project; **deferred until arm RL and Go2 results**

## Research target
Reproduce the simulation-side core of [ASAP: Aligning Simulation and Real-World Physics for Learning Agile Humanoid Whole-Body Skills (RSS 2025)](https://arxiv.org/abs/2502.01143).

Upstream: https://github.com/LeCAR-Lab/ASAP
Project website: https://agile.human2humanoid.com/
Related: https://github.com/LeCAR-Lab/HumanoidVerse

## Scientific components to understand and reproduce
1. Phase-based humanoid motion tracking.
2. Motion data / retargeting pipeline: provenance, transformations, joint correspondence and metrics.
3. Delta action model (simulation-to-reality physics discrepancy modeling), paired-control comparisons.
4. Fine-tuning a motion-tracking policy with the delta action model.
5. MuJoCo Sim2Sim evaluation (not Sim2Real unless physical data/deployment actually exist).

## Milestones
| Gate | Task | Exit criterion |
|---|---|---|
| A0 | Full paper-to-code-to-dataset audit | Exact method equations, dependencies, model, dataset license and available source |
| A1 | Setup + model smoke | Pin upstream branch/commit; CPU/GPU and dataset audit; run smoke |
| A2 | Reproduce phase tracking baseline | Motion error, completion/termination, robustness, independent seeds |
| A3 | Reproduce retargeting | One declared motion sequence; pose/orientation/joint alignment diagnostics |
| A4 | Reproduce delta action model | Supervision/data pipeline and prediction metric; compare with no delta |
| A5 | Policy fine-tune/ablation | Same motions, simulator, seeds, evaluation budget |
| A6 | Sim2Sim & paper comparison | Document mismatches and missing dependencies; no unearned result claims |

## Important scope boundaries
- **Do not substitute motion-tracking demos for physics-alignment reproduction.**
- **Do not automatically upgrade Isaac Gym / Isaac Sim or the existing ROS2 + Isaac Sim installation.** Check compatibility first.
- If hardware datasets, restricted licenses or physical prerequisites are inaccessible, record exact gaps and numerical-simulation scope.
- Original repo README currently references Isaac Gym Preview 4, Isaac Sim 4.2.0 and Genesis 0.2.1; environment versions must be pinned and reverified.

## Documents
- [AGENTS.md](AGENTS.md)
- [docs/REPRODUCTION_PLAN.md](docs/REPRODUCTION_PLAN.md)
- [docs/EXPERIMENT_MATRIX.md](docs/EXPERIMENT_MATRIX.md)
- [docs/PAPER_CODE_ALIGNMENT.md](docs/PAPER_CODE_ALIGNMENT.md)
- [docs/FAILURE_LOG.md](docs/FAILURE_LOG.md)
- [docs/RESUME_EVIDENCE.md](docs/RESUME_EVIDENCE.md)
