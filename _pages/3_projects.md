---
title: "Applied projects"
permalink: /projects/
layout: single
author_profile: true
---

Applied, computational, and quantitative work — the numerical, optimization, and machine-learning toolkit behind my research, used to build and ship concrete tools. Several projects are still in progress.

#### Physics-Informed Neural Operators for Option Pricing

Learned solution operators for European option pricing under the Black–Scholes PDE. Benchmarks a Fourier Neural Operator against deep, convolutional, and vanilla neural-operator baselines, with a physics-informed loss that bakes the governing PDE into training. Includes feasibility studies, hyperparameter and loss-weight ablations, and evaluation on real market data from WRDS. Built in PyTorch. [code](https://github.com/zefangli/Physics-Informed-Neural-Operators-for-Option-Pricing)  _Work in progress;A second option-pricing model is currently under construction._

#### Multi-Material Print Path Planning

A Rural Postman Problem solver that plans continuous toolpaths covering every edge of a lattice while minimizing non-printing "jump" travel, achieving up to **18% printing-time reduction** for multi-material structures. Handles per-material nozzle offsets and exports G-code for direct printing. Utilizing Python, NetworkX, NumPy, SciPy.
[details](https://github.com/JHU-Mueller-Lab/Print-Path-Planning-for-Multimaterial-Structures)

#### Differentiable Thermal Simulation & Learned Surrogates

Building a differentiable thermal-simulation framework for metal additive manufacturing and learned surrogate models that accelerate it, turning slow forward solves into fast, gradient-enabled tools for inverse process design and optimization. _Work in progress; details to follow upon publication._

#### Technical Skills

- **Programming:** Python (NumPy, Pandas, Scikit-learn, PyTorch), MATLAB, C++
- **Mathematics:** Partial differential equations, finite element analysis, numerical methods, optimization, stochastic & time-series modeling