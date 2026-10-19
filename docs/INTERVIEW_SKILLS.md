# Interview Skills from This Reproduction / 项目关联面试技术栈

**Focus:** 人形运动模仿与全身动作控制
**Target job families:** 人形机器人 WBC / 动作学习 / RL 运控岗位（进阶）

## Core required skills
- Phase-conditioned motion tracking
- retargeting
- floating-base dynamics
- learned action correction/delta-action model
- reward/termination
- data provenance
- training/finetuning
- simulator physics mismatch
- Sim2Sim vs Sim2Real

## Portfolio / interview drill
Explain source paper claim and equation-to-code mapping; run controlled tracking on one legal motion clip; compare tracking with/without delta model; document where physics discrepancy data came from.

## Evidence policy
- Knowledge != implemented code != verified experiment. Demonstrate the exact level using code links and logs.
- Prepare one 3-minute overview and one 15-minute whiteboard walkthrough.
- Be ready to answer: Why this algorithm? Which baselines? What are training and evaluation metrics? How do you debug failures? What is your independent contribution?
- If this remains a numerical simulation, **do not** advertise physical robot experience, Sim2Real transfer or field deployment.

## Links
See [plan](REPRODUCTION_PLAN.md), [experiment matrix](EXPERIMENT_MATRIX.md), [resume evidence](RESUME_EVIDENCE.md).
