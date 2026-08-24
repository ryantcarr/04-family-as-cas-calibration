# Family-as-CAS Calibration

Working title: **Family-as-CAS Calibration: Multi-Agent Relational Response Simulation Using FAD and SCORE-15 Benchmarks**

This is a standalone LaTeX/Git project for the Family-as-CAS simulation paper contribution identified in the practicum proposal presentation.

## Status

- `main.tex` — **draft v0.1 (methods-forward), 2026-06-11**: full prose for
  Introduction, Background, Architecture, and Calibration Design; Results are
  pre-registered shells pending FORWARD_PLAN Phase 7 (Rung-2 runs after the
  Rung-1 freeze). `[LEAD]` flags = unverified literature; `[PENDING]` flags =
  later-phase outputs. Neither may survive into a submitted version.
- `MISSING_INFO_PLAN.md` — gap register (G1–G9) tying every missing input to
  its `oha-simulation-v2/docs/FORWARD_PLAN.md` phase, with start-now actions.

## Build

```powershell
latexmk -pdf main.tex
```
