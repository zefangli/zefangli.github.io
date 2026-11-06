---
title: "Tools"
permalink: /projects/
layout: single
author_profile: true
classes: wide
---

Applied, computational, and quantitative work — the numerical, optimization, and machine-learning toolkit behind my research, used to build and ship concrete tools. Several projects are still in progress.

### 3D printing

#### Multi-Material Print Path Planning

A Rural Postman Problem solver that plans continuous toolpaths covering every edge of a lattice while minimizing non-printing "jump" travel, achieving up to **18% printing-time reduction** for multi-material structures. Handles per-material nozzle offsets and exports G-code for direct printing. Utilizing Python, NetworkX, NumPy, SciPy.
[details](https://github.com/JHU-Mueller-Lab/Print-Path-Planning-for-Multimaterial-Structures)


#### Customized Prusa MK3S/MK3S+ Firmware with PT1000 Hotend Sensor for Higher Temperatures

An unofficial fork of Prusa-Firmware 3.14.1 that reads a PT1000 hotend sensor on the stock thermistor port, enabling nozzle temperatures up to 400 °C (MAXTEMP 420 °C) with MINTEMP/MAXTEMP protection working for this sensor. [code](https://github.com/zefangli/MK3S-PT1000-firmware)

#### Differentiable Thermal Simulation & Learned Surrogates

Building a differentiable thermal-simulation framework for metal additive manufacturing and learned surrogate models that accelerate it, turning slow forward solves into fast, gradient-enabled tools for inverse process design and optimization. _Work in progress; details to follow upon publication._


### Quant

#### Cross-Sectional Equity Alpha Research

An auditable, point-in-time CRSP research pipeline (US equities, 2005–2025) testing whether six interpretable price and volume signals forecast 20-trading-day cross-sectional returns well enough to trade after costs. Every hypothesis was pre-registered, and the 2024–2025 holdout was sealed and opened exactly once against a frozen specification. The frozen five-factor composite reached a **1.43 gross / 1.06 net Sharpe** at 10 bp on the holdout, reported alongside its wide confidence interval and the many nulls: no single factor is tradable, and fitted models (OLS, Ridge, gradient boosting) never beat a flat composite net of costs. [code](https://github.com/zefangli/cross-sectional-alpha-research)

#### Neural Operators for Option Pricing: Learning Implied Volatility, Not Prices

A 2-D Fourier Neural Operator encodes the market state (implied-volatility surface, SPX history, or VIX history), and a per-contract head (MLP or DeepONet) predicts implied volatility, which is decoded through a differentiable closed-form Black–Scholes pricer. Trained on SPX options from OptionMetrics/WRDS (2015–2025), it reaches R² ≈ 0.99 on log-normalized prices, and Greeks come from autograd through the same analytical decoder. Built in PyTorch. [code](https://github.com/zefangli/Neural-Operators-for-Option-Pricing)

#### Physics-Informed Neural Operators for Option Pricing

Learned solution operators for European option pricing under the Black–Scholes PDE. Benchmarks a Fourier Neural Operator against deep, convolutional, and vanilla neural-operator baselines, with a physics-informed loss that bakes the governing PDE into training. Includes feasibility studies, hyperparameter and loss-weight ablations, and evaluation on real market data from WRDS. Built in PyTorch. [code](https://github.com/zefangli/Physics-Informed-Neural-Operators-for-Option-Pricing)

