---
title: Reduced-order modelling with PGD
summary: Proper generalized decomposition with synthetic preconditioning for multiscale, parametric phonon transport.
date: 2026-10-01
weight: 40
tags:
  - Reduced-order modelling
  - PGD
image:
  filename: research/pgd.png
  caption: ''
  preview_only: false
---

Engineering design asks the same question many times: *how does the temperature field change when the geometry, the material or the operating point changes?* Running a full kinetic simulation for every parameter value is prohibitive. **Proper generalized decomposition (PGD)** writes the solution as a sum of a few separable modes in space, phonon phase space and the parameters, so that a whole family of problems is solved at once. Pairing it with synthetic preconditioning is designed to keep it efficient in the multiscale regime, where kinetic solvers are slowest.

**Papers**

- J. Liu, W. Su. [Proper generalized decomposition with synthetic preconditioning for multiscale parametric phonon transport](/publication/2026-arxiv-pgd-synthetic-preconditioning/). arXiv:2610.27880 (2026).

<!-- TODO(Jia): add the key result (speed-up, accuracy) and a figure. -->
