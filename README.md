# Tension_Go

Code and analysis pipelines for measuring strategic tension, spatial networks, and phase-space dynamics in Go (Weiqi / Baduk).

## Authors
Adamo Cerioli, Vito D. P. Servedio, Gabriele Cerioli, Antonio Villani, Carlo Metta*

---

## Overview

This repository contains the computational framework used to extract spatial interaction networks and quantify strategic tension from Go games in Smart Game Format (`.sgf`). The pipeline supports evaluations across human skill ranks ($18\text{k} \to 9\text{d}$), historical cohorts (1980–2026), and neural engines (KataGo, Leela Zero) under varying MCTS visit budgets and noise perturbation policies.

## Repository Structure

* `src/` (or main scripts): Python scripts for SGF parsing, move-to-move spatial distance calculations, material attrition tracking (captured stones), and spectral tension load integration.
* `data/`: Processed ensemble averages and tension metrics (e.g., `phase_space_all_ensembles.csv`).
* `figures/`: Scripts and output assets for phase-space projections and visual trajectory analyses.

## Reuse & License

All code and processed data in this repository are freely available for academic, research, and educational purposes.
