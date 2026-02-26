---
layout: page
title: Real-Time Multi-Agent Simulation
description: KD-Tree spatial indexing achieving 17.8× speedup over naive O(n²) neighbor search — 500+ interacting agents at 60 FPS
importance: 3
category: research
---

Simulating large numbers of interacting agents in real time requires efficient spatial data structures.
Naive O(n²) pairwise neighbor search becomes the bottleneck long before reaching interesting emergent behaviors.
This project replaces brute-force neighbor lookup with a KD-Tree index, making real-time simulation of 500+ agents tractable on consumer hardware.

#### Key contributions

- **KD-Tree spatial indexing:** Nearest-neighbor queries restructured using a KD-Tree, reducing per-timestep neighbor search from O(n²) to O(n log n); measured **17.8× speedup** over the baseline implementation
- **Real-time performance:** 500+ concurrently interacting agents simulated at a stable 60 FPS, enabling interactive visualization and parameter exploration
- **Agent interaction model:** Agents follow local behavioral rules (alignment, separation, cohesion) producing emergent flocking and swarming dynamics; interaction radius and behavioral weights configurable at runtime

#### Technical stack

Python · NumPy · SciPy (KD-Tree) · Matplotlib / real-time rendering

<!-- Add GitHub link when repository is ready:
[View on GitHub](https://github.com/codegithubka/REPO_NAME)
-->
