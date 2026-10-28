# Tension_Go

[![arXiv](https://img.shields.io/badge/arXiv-2610.33323-b31b1b.svg)](https://arxiv.org/abs/2610.33323)
[![DOI](https://zenodo.org/badge/DOI/ZENODO_DOI.svg)](https://doi.org/ZENODO_DOI)

Core codebase for evaluating strategic tension in the game of Go, accompanying the preprint:

> A. Cerioli, V. D. P. Servedio, G. Cerioli, A. Villani, C. Metta, **AI Teaches Humans to Handle Complexity in the Game of Go**, arXiv:2610.33323 (2026). [https://arxiv.org/abs/2610.33323](https://arxiv.org/abs/2610.33323)

## Authors
Adamo Cerioli, Vito D. P. Servedio, Gabriele Cerioli, Antonio Villani, Carlo Metta*

\*Corresponding author: carlo.metta@isti.cnr.it

---

## Overview

This repository provides the core computational pipeline to calculate **strategic tension** in the game of Go from matches stored in Smart Game Format (`.sgf`).

By coupling KataGo's policy and territory ownership predictions with spatial clustering (identifying stone groups and contested territorial zones), the framework constructs spatial interaction matrices and extracts spectral tension loads. In our study, we applied this metric to systematically **compare human and AI play**, analyzing how strategic complexity:
* **Scales with player proficiency**, from amateur ranks (18k → 9d) to professional mastery.
* **Evolves across historical eras**, capturing the paradigm shift in professional human strategy before and after the 2016 AI revolution.
* **Behaves in artificial agents**, contrasting deep neural engines (KataGo, Leela Zero) against human baselines and asymmetric matchups.

## Data Availability

The SGF records of all games analyzed in the study are archived on Zenodo:

**[https://doi.org/ZENODO_DOI](https://doi.org/ZENODO_DOI)**

The Zenodo record contains the exact sets of games used in each analysis, so that every figure in the paper can be reproduced with the code in this repository.

## Datasets & Sources

The empirical ensembles analyzed in this project are drawn from publicly available SGF archives:

* **Elite Human Professionals (1980–2026):** Major international tournaments (e.g., Chunlan Cup, LG Cup, Samsung Cup, Ing Cup) and premier Japanese title matches (Kisei, Meijin, Honinbo, etc.) under deep, multi-hour time controls, retrieved from the [AEB Go Games Archive](https://homepages.cwi.nl/~aeb/go/games).
* **Mixed AI Benchmark:** 200 matches from the [UEC Computer Go Championship](https://uec-go.com/), featuring algorithmic asymmetries across classical heuristics, Monte Carlo tree search, and deep neural networks.
* **Rank-Stratified Human Progression (18k → 9d):** Even games (non-handicap, max. 2-rank difference) spanning the full human skill spectrum, sourced from the [featurecat/go-dataset repository](https://github.com/featurecat/go-dataset).
* **AlphaGo vs. Human Professionals:** 73 landmark games documenting the transition to superhuman AI play (including the 2016 Lee Sedol challenge), compiled by [Go Magic](https://gomagic.org/download/alphago-sgf-pack-70-games/).

## Repository Contents

* `Code_Adamo_Cerioli_Tension_Go.ipynb`: Main execution script for KataGo subprocess management, SGF parsing, stone group/zone clustering, dependency matrix construction, and strategic tension calculation.

## Citation

If you use this code or data in your work, please cite the arXiv preprint:

```bibtex
@misc{cerioli2026go,
  title         = {AI Teaches Humans to Handle Complexity in the Game of Go},
  author        = {Cerioli, Adamo and Servedio, Vito D. P. and Cerioli, Gabriele and Villani, Antonio and Metta, Carlo},
  year          = {2026},
  eprint        = {2610.33323},
  archivePrefix = {arXiv},
  primaryClass  = {cs.AI},
  doi           = {10.48550/arXiv.2610.33323},
  url           = {https://arxiv.org/abs/2610.33323}
}
```

## Reuse & License

All code in this repository and all data in the Zenodo record are freely available for academic, research, and educational use. If you use them, please cite the preprint as indicated above.
