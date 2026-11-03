---
title: 'A fast-converging scheme for the phonon Boltzmann equation with dual relaxation times'
authors:
  - admin
  - Chuang Zhang
  - Haizhuan Yuan
  - Wei Su
  - Lei Wu
author_notes:
  - ''
  - ''
  - ''
  - 'Corresponding author'
  - 'Corresponding author'
date: '2022-07-03T00:00:00Z'
doi: '10.1016/j.jcp.2022.111436'
publication_types: ['article-journal']
publication: '*Journal of Computational Physics*, 467, 111436'
publication_short: ''

# TODO(Jia): paste your abstract here if you would like it shown on this page
abstract: ''
summary: 'A general synthetic iterative scheme (GSIS) for the Callaway dual-relaxation-time model of phonon transport, with up to three orders of magnitude fewer iterations than the conventional iterative scheme in the diffusive and hydrodynamic regimes.'

tags:
  - GSIS
  - Phonon Boltzmann equation
featured: true

links:
  - name: arXiv
    url: https://arxiv.org/abs/2107.06688
url_pdf: ''
url_code: ''

image:
  filename: research/gsis.png
  caption: ''
  focal_point: ''
  preview_only: true

projects:
  - gsis
---

Steady-state phonon transport with Callaway's dual relaxation times (normal and resistive scattering) converges quickly with the conventional iterative scheme in the ballistic regime, but needs thousands of iterations when phonons scatter often. This paper introduces a **general synthetic iterative scheme (GSIS)**: macroscopic synthetic equations, derived exactly from the kinetic equation, guide the evolution of the equilibrium distributions, while the kinetic equation supplies their closures. A Fourier stability analysis explains why it converges fast, and numerical tests from the ballistic to the diffusive/hydrodynamic regime show up to three orders of magnitude of acceleration.
