---
title: General synthetic iterative schemes for phonon transport
summary: Converged solutions in dozens of iterations instead of thousands, from the ballistic to the diffusive regime.
date: 2022-07-03
weight: 10
tags:
  - GSIS
  - Phonon Boltzmann equation
image:
  filename: research/gsis.png
  caption: ''
  preview_only: false
---

When phonons scatter often (small Knudsen number), the conventional iterative scheme passes information across the domain only one mean free path per iteration, so thousands of iterations are needed. The **general synthetic iterative scheme (GSIS)** solves the kinetic equation together with macroscopic *synthetic* equations that are derived exactly from it. The macroscopic equations spread information quickly and pin down the equilibrium, while the kinetic equation provides the non-equilibrium closures. The result is fast convergence at any Knudsen number, without sacrificing kinetic accuracy.

**What I did**

- Proposed a GSIS for the phonon Boltzmann equation with Callaway's dual relaxation times (normal and resistive scattering), with up to three orders of magnitude fewer iterations than the conventional scheme.
- Analysed its convergence with Fourier stability analysis.
- Extended synthetic acceleration to the non-gray (frequency-dependent) phonon BTE with dual relaxation times (with D. Shen and W. Su).

**Papers**

- J. Liu, C. Zhang, H. Yuan, W. Su, L. Wu. [A fast-converging scheme for the phonon Boltzmann equation with dual relaxation times](/publication/2022-jcp-gsis-dual-relaxation/). *J. Comput. Phys.* 467, 111436 (2022).
- D. Shen, J. Liu, W. Su. [A synthetic iterative scheme for non-gray phonon Boltzmann transport equation with dual relaxation times](/publication/2026-arxiv-nongray-gsis/). arXiv:2608.28101 (2026).

<!-- TODO(Jia): add a key figure, e.g. a convergence history (GSIS vs CIS). Put `convergence.png` in this folder and add:
{{< figure src="convergence.png" caption="Iterations to convergence: GSIS vs conventional scheme" >}} -->
