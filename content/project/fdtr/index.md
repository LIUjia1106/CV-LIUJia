---
title: Simulating thermoreflectance experiments
summary: Fast, asymptotic-preserving kinetic simulation of frequency-domain thermoreflectance (FDTR).
date: 2023-08-14
weight: 30
tags:
  - Thermoreflectance
  - GSIS
image:
  filename: research/fdtr.png
  caption: ''
  preview_only: false
---

Frequency-domain thermoreflectance (FDTR) measures thermal properties by heating a sample with a modulated pump laser and reading the surface temperature with a probe laser. When the heating is fast or the structures are small, heat conduction is no longer diffusive, and interpreting the measurement needs the phonon Boltzmann equation, with two spatial Knudsen numbers and a temporal one set by the modulation frequency.

**What I did**

- Built a GSIS solver for this time-periodic problem that converges within dozens of iterations over a wide range of Knudsen numbers and frequencies.
- Made it asymptotic-preserving: accurate even when bulk cells are much larger than the phonon mean free path.
- Studied how the heating frequency changes heat conduction in different transport regimes.

**Papers**

- J. Liu, L. Wu. [Fast-converging and asymptotic-preserving simulation of frequency domain thermoreflectance](/publication/2023-cicp-fdtr/). *Commun. Comput. Phys.* 34(1), 65–93 (2023).
