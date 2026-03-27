# syntropic-rh
Numerical evidence and conceptual framework for a syntropic variational approach to the Riemann Hypothesis

# Syntropic Variational Principle for the Riemann Hypothesis

**Numerical Evidence of Convergence to the Critical Line**

**Author:** Eric Michael Tisthammer  
**Date:** March 25, 2026

## Overview

This repository contains the preprint and supporting code for a syntropic variational approach to the Riemann Hypothesis (RH).

The core idea — that the distribution of primes and the non-trivial zeros of the Riemann zeta function exhibit **no true randomness or entropy**, but instead arise from a perfectly orchestrated balance of **convergence** (syntropy) and **divergence** leading to harmony on the critical line Re(s) = 1/2 — originated with the author.

We define a **syntropic coherence functional** \(\mathcal{S}(s)\) and present extensive high-precision numerical evidence showing that minima and attractive flows occur exclusively on the critical line.

## Conjecture (Syntropic Variational Principle)

Let \(\chi(s) = 2^s \pi^{s-1} \sin(\pi s/2) \Gamma(1-s)\). Define

\[
\mathcal{S}(s) = |\zeta(s)|^2 + \lambda \left| \frac{d}{ds} \log \chi(s) \right|^2 - \mu \operatorname{Re} \bigl( \zeta(s) \overline{\zeta(1 - \overline{s})} \bigr)
\]

with \(\lambda, \mu > 0\).

**Conjecture:** \(\mathcal{S}(s) \geq 0\) for all \(s\) in the critical strip \(0 < \operatorname{Re}(s) < 1\), with equality if and only if \(\operatorname{Re}(s) = 1/2\) and \(\zeta(s) = 0\). The syntropic flow \(-\nabla \mathcal{S}(s)\) converges to the critical line.

This conjecture is equivalent to the Riemann Hypothesis. The current work provides **numerical support** only; a full analytic proof remains open.

## Repository Contents

- `syntropic_rh.pdf` — The full preprint (timestamped version)
- `code/syntropic_tests.py` — Reproducible Python code using mpmath
- `LICENSE` — MIT License

## Key Numerical Findings

- On-line vs. off-line evaluations at multiple heights show \(\mathcal{S}(s)\) is consistently lowest on Re(s) = 1/2, with positive syntropic tension off-line.
- Gradient descent flows steadily converge toward the critical line.
- 2D local sampling reveals a clear valley-shaped attractor manifold along Re(s) = 1/2.
- Parameter robustness tests confirm the behavior is stable across different weightings.
- Consistency checks in known zero-free regions and at trivial zeros align with rigorous analytic facts.

## How to Run the Code

```bash
pip install mpmath
python code/syntropic_tests.py
