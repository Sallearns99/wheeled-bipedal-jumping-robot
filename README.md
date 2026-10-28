# Wheeled-Bipedal Jumping Robot (Bio-Inspired Robotics)

*Group study of agile control for a wheeled-bipedal robot that can jump.*

## Overview

Bio-Inspired Robotics group project (Group 4) analysing the design and control of an agile wheeled-bipedal jumping robot - locomotion, balance and jumping control strategies drawn from the literature.

The study is a critical review of the paper:

> H. Chen, B. Wang, Z. Hong, C. Shen, P. M. Wensing and W. Zhang, "Underactuated Motion Planning and Control for Jumping With Wheeled-Bipedal Robots," *IEEE Robotics and Automation Letters*, vol. 6, no. 2, pp. 747-754, April 2021. doi: [10.1109/LRA.2020.3047787](https://doi.org/10.1109/LRA.2020.3047787)

The presentation breaks the paper's hierarchical planning-and-control framework down into its parts, explains the maths behind each one, and ends with a critical analysis of its strengths and limitations.

**Team:** Bassam ElSaadani, Salma Farid, Islam Ibrahim

**Tech & tools:** Bio-inspired control, wheeled-bipedal dynamics, literature review.

## Topics covered

The deck (28 slides) is organised into five sections:

1. **Introduction and background** - wheeled vs. bipedal locomotion, why hybrid wheeled-bipedal robots are hard to control, and the key models and terms: T-WIP (two-wheeled inverted pendulum), SLIP / W-SLIP, differential flatness, quadratic programming (QP), LQR and disturbance observers.
2. **Stance and flight planning** - the Wheeled Spring-Loaded Inverted Pendulum (W-SLIP) template; stance-phase planning (reference generation, forward simulation, polynomial fitting with QP); flight-phase planning (ballistic CoM, conserved angular momentum, leg-length optimisation for obstacle clearance).
3. **Mathematical motion planning** - how a differential-flatness-like property of W-SLIP makes the underactuated planning problem a small QP that can be solved online at 25 Hz.
4. **Tracking control and robustness** - the composite controller: a task-space PD controller for the hips and knees, a time-varying LQR for the wheels, and disturbance observers that compensate for coupling between the two.
5. **Validation and critical analysis** - region-of-attraction results, the V-REP simulation of the 12.7 kg SUSTech "Nezha" prototype, and a discussion of the method's strengths and limitations (for example, a purely 2D sagittal-plane model, and no modelling of soft or uneven terrain).

## What's inside

```
docs/
├── Jumping_Robot_Presentation.pptx   Group presentation (28 slides) - the main deliverable
├── figure.png                        One-page summary infographic of the framework
└── Jumping_Robot.pdf                 The reviewed IEEE RA-L paper (reference material, not written by the team)
```

## How to use

There is nothing to build or run. Open the files directly:

- `docs/Jumping_Robot_Presentation.pptx` - open in PowerPoint, LibreOffice Impress, or Google Slides. Some slides contain animated GIFs, so open it in an application rather than a static preview.
- `docs/figure.png` - a one-page visual summary.
- `docs/Jumping_Robot.pdf` - the source paper, for the full derivations and simulation results.

The `.pptx` file is about 30 MB. Use `git clone --depth 1` if you only need the latest version.

## Status & notes

This was a **group project and a literature/analysis deliverable - there is no source code**. All quantitative results described here (planning rates, torque limits, apex heights, slope landing) come from the reviewed paper's V-REP simulations, not from experiments run by the team. Shared here for completeness of the portfolio.

---

*By Salma Farid — Mechatronics & Robotics Engineering, BUE / LSBU. This is coursework/graduation work shared as a portfolio; I'll keep refining it.*
