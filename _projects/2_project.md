---
layout: page
title: "Stochastic Simulation on HPC: Emergent Population Dynamics"
description: Numba JIT-compiled stochastic cellular automaton across a 4D parameter space on the Snellius supercomputer — highest grade in cohort
importance: 2
category: research
---

**Highest grade in cohort.**

This project investigates emergent population dynamics — including the [Hydra effect](https://en.wikipedia.org/wiki/Hydra_effect), the counterintuitive phenomenon where increased predation can *increase* prey population size — using large-scale stochastic cellular automaton simulations.
The computational challenge: a 4D parameter space requiring thousands of replicate trajectories per configuration, feasible only with aggressive optimization and HPC parallelism.

#### Key contributions

- **Numba JIT compilation:** Core simulation loops rewritten with Numba JIT, achieving near-C performance in Python and order-of-magnitude speedups over pure NumPy implementations — essential for sweeping 13,000+ configurations per replicate
- **Snellius HPC cluster:** 5-phase experiment pipeline parallelized across nodes on the Dutch national supercomputer [Snellius](https://www.surf.nl/en/dutch-national-supercomputer-snellius) using joblib; job arrays managed via SLURM
- **O(N) spatial hashing:** Pair correlation functions computed via pre-allocated hash-map buffers with JIT-cached kernels, reducing neighbor-lookup complexity from O(N²) to O(N)
- **Statistical physics analysis:** Cluster size distributions, power-law fitting, and finite-size scaling to characterize phase transitions between extinction and coexistence regimes; identification of critical predation thresholds for the Hydra effect

#### Technical stack

Python · Numba · NumPy · SciPy · Snellius HPC · SLURM · joblib · Statistical physics methods

<!-- Add GitHub link when repository is ready:
[View on GitHub](https://github.com/codegithubka/REPO_NAME)
-->
