# Syntropic Variational Principle for the Riemann Hypothesis

**Numerical Evidence of Convergence to the Critical Line**

**Author:** Eric Michael Tisthammer  
**Date:** March 25, 2026

## Overview

This repository contains the preprint and supporting code for a syntropic variational approach to the Riemann Hypothesis (RH).

The core idea — that the distribution of primes and the non-trivial zeros of the Riemann zeta function exhibit **no true randomness or entropy**, but instead arise from a perfectly orchestrated balance of **convergence** (syntropy) and **divergence** leading to harmony on the critical line Re(s) = 1/2 — originated with the author.

We define a syntropic coherence functional S(s) and present extensive high-precision numerical evidence showing that minima and attractive flows occur exclusively on the critical line.

## Conjecture (Syntropic Variational Principle)

Let χ(s) = 2^s π^(s-1) sin(π s/2) Γ(1-s). Define

S(s) = |ζ(s)|^2 + λ |d/ds log χ(s)|^2 - μ Re( ζ(s) conj(ζ(1 - conj(s))) )

with λ, μ > 0.

**Conjecture:** S(s) ≥ 0 for all s in the critical strip 0 < Re(s) < 1, with equality if and only if Re(s) = 1/2 and ζ(s) = 0. Furthermore, the syntropic flow -∇S(s) converges to the critical line.

This conjecture is equivalent to the Riemann Hypothesis. The current work provides **numerical support** only; a full analytic proof remains open.

## Repository Contents

- syntropic_rh.pdf — The full preprint (timestamped version)
- code/syntropic_tests.py — Reproducible Python code using mpmath
- LICENSE — MIT License

## Key Numerical Findings

- On-line vs. off-line evaluations at multiple heights show S(s) is consistently lowest on Re(s) = 1/2, with positive syntropic tension off-line.
- Gradient descent flows steadily converge toward the critical line.
- 2D local sampling reveals a clear valley-shaped attractor manifold along Re(s) = 1/2.
- Parameter robustness tests confirm the behavior is stable across different weightings.
- Consistency checks in known zero-free regions and at trivial zeros align with rigorous analytic facts.

## How to Run the Code

```bash
pip install mpmath
python code/syntropic_tests.py
