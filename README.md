## Aerospace Optimization Challenge
### Author: Lipika Parida | IIT Jodhpur

### Overview
A 4-part optimization challenge applying mathematical optimization techniques to an aerospace engineering problem — minimizing the cost function for Thrust (T) and Wing Area (W) of an aircraft under real-world constraints.

Gradient Descent is implemented from scratch (no ML libraries), then validated against SciPy's BFGS optimizer.

## Parts

### Part 1 — Wind Tunnel Analysis (Data Generation & Visualization)
- Generated 1,000 simulated aerodynamic data points using NumPy
- Added Gaussian noise to simulate real-world sensor data
- Visualized Thrust vs Cost and Wing Area vs Cost relationships
- Identified cost minimum near T=12, W=8

### Part 2 — Smart Autopilot (Gradient Descent with Backtracking)
- Implemented Gradient Descent **from scratch** with Backtracking Line Search
- Dynamically adjusts step size (α) to guarantee cost reduction at every iteration
- Converges smoothly to optimal values: T=12, W=8, Final Cost=100
- Plotted cost history showing clean convergence curve

### Part 3 — Fleet Operations (Mini-Batch GD + SciPy Validation)
- Scaled optimization to 1,000-record dataset using Mini-Batch Gradient Descent
- Batch size: 64, Learning rate: 0.01, Epochs: 50
- Validated results using SciPy's BFGS optimizer — both methods confirm same optimum
- Demonstrated stochastic noise behavior in mini-batch cost curve

### Part 4 — Constrained Optimization (Feasible Region Analysis)
- Added real-world constraint: T + W ≤ 15
- Unconstrained optimum (12, 8) lies outside feasible region
- Constrained optimum found at (9.5, 5.5) on the boundary T + W = 15
- Verified Geometric Optimality Condition — no feasible descent direction exists at constrained optimum


## Key Concepts Demonstrated

- Gradient computation and manual backpropagation of gradients
- Backtracking Line Search for adaptive learning rate
- Mini-Batch Gradient Descent for large-scale optimization
- Constrained vs unconstrained optimization
- Feasible region analysis and boundary conditions
- SciPy BFGS validation of custom implementations


## Tech Stack

1. Python, NumPy, Matplotlib
2. SciPy (optimize.minimize — BFGS)
3. Google Colab

## Results Summary

| Method | Optimized T | Optimized W | Final Cost |
|--------|-------------|-------------|------------|
| Gradient Descent (Backtracking) | 12.0000 | 8.0000 | 100.0000 |
| Mini-Batch GD | ~12.0 | ~8.0 | ~100.0 |
| SciPy BFGS | 12.0000 | 8.0000 | 100.0000 |

All three methods converge to the same unconstrained optimum, confirming correctness.

## Files

```
├── Aerospace_Optimization_Challenge.ipynb   ← Full notebook with all 4 parts
└── README.md
```

### Part of my data science & AI portfolio. Completed as part of Optimization Algorithms coursework at IIT Jodhpur.
