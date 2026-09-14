# Tension_Go

Core codebase for evaluating strategic tension in the game of Go.

## Authors
Adamo Cerioli, Vito D. P. Servedio, Gabriele Cerioli, Antonio Villani, Carlo Metta*

---

## Overview

This repository provides the core computational pipeline to calculate **strategic tension** in the game of Go from matches stored in Smart Game Format (`.sgf`). 

By coupling KataGo's policy and territory ownership predictions with spatial clustering (identifying stone groups and contested territorial zones), the framework constructs spatial interaction matrices and extracts spectral tension loads. In our study, we applied this metric to systematically **compare human and AI play**, analyzing how strategic complexity:
* **Scales with player proficiency**, from amateur ranks ($18\text{k} \to 9\text{d}$) to professional mastery.
* **Evolves across historical eras**, capturing the paradigm shift in professional human strategy before and after the 2016 AI revolution.
* **Behaves in artificial agents**, contrasting deep neural engines (KataGo, Leela Zero) against human baselines and asymmetric matchups.
## Datasets & Sources

The empirical and synthetic ensembles analyzed in this project are drawn from publicly available SGF archives:

* **Elite Human Professionals (1980–2026):** Major international tournaments (e.g., Chunlan Cup, LG Cup, Samsung Cup, Ing Cup) and premier Japanese title matches (Kisei, Meijin, Honinbo, etc.) under deep, multi-hour time controls, retrieved from the [AEB Go Games Archive](https://homepages.cwi.nl/~aeb/go/games).
* **Mixed AI Benchmark:** 200 matches from the [UEC Computer Go Championship](https://uec-go.com/), featuring algorithmic asymmetries across classical heuristics, Monte Carlo tree search, and deep neural networks.
* **Rank-Stratified Human Progression ($18\text{k} \to 9\text{d}$):** Even games (non-handicap, max. 2-rank difference) spanning the full human skill spectrum, sourced from the [featurecat/go-dataset repository](https://github.com/featurecat/go-dataset).
* **AlphaGo vs. Human Professionals:** 73 landmark games documenting the transition to superhuman AI play (including the 2016 Lee Sedol challenge), compiled by [Go Magic](https://gomagic.org/download/alphago-sgf-pack-70-games/).

## Repository Contents

* `Code_Adamo_Cerioli_Tension_Go.ipynb`: Main execution script for KataGo subprocess management, SGF parsing, stone group/zone clustering, dependency matrix construction, and strategic tension calculation.

## Reuse & License

All code and processed data in this repository are freely available for academic, research, and educational use.
