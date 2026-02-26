---
layout: page
title: Optimal Trade Execution under Regime-Switching Liquidity
description: Regime-switching market simulator with jump-diffusion price dynamics and CIR liquidity — extended Almgren–Chriss with dynamic urgency recalibration
importance: 1
category: research
---

Classical optimal execution models (Almgren–Chriss and variants) treat market impact and liquidity as static parameters.
In practice, markets alternate between distinct regimes — low-volatility trending conditions and high-volatility stress periods — and execution strategies that ignore this structure incur avoidable costs.
This project builds a regime-aware execution framework that adapts in real time to estimated market state.

#### Model components

- **Regime-switching dynamics:** Market state modeled as a continuous-time Markov chain (CTMC) with estimated transition rates between liquidity regimes; execution urgency and impact parameters are state-dependent
- **Jump-diffusion price process:** Asset mid-price follows a jump-diffusion (Merton) process, capturing both continuous Brownian motion and discrete sentiment-driven jumps
- **CIR liquidity process:** Bid-ask spread and market depth modeled via Cox–Ingersoll–Ross processes, ensuring mean-reversion and non-negativity
- **Dynamic urgency recalibration:** Extended Almgren–Chriss framework recalibrates the execution urgency parameter at each regime transition, rebalancing the trade-off between market impact and timing risk
- **Monte Carlo validation:** Execution strategies benchmarked against TWAP across 10,000+ simulated paths per regime configuration; regime-adaptive strategy achieves statistically significant cost savings (p < 0.01) under simulated stress conditions

#### Technical stack

Python · NumPy · SciPy · Monte Carlo simulation · Stochastic differential equations · Continuous-time Markov chains

<!-- Add GitHub link when repository is ready:
[View on GitHub](https://github.com/codegithubka/REPO_NAME)
-->
