---
title: 'Fast-converging and asymptotic-preserving simulation of frequency domain thermoreflectance'
authors:
  - admin
  - Lei Wu
author_notes:
  - ''
  - 'Corresponding author'
date: '2023-08-14T00:00:00Z'
doi: '10.4208/cicp.OA-2023-0053'
publication_types: ['article-journal']
publication: '*Communications in Computational Physics*, 34(1), 65–93'
publication_short: ''

# TODO(Jia): paste your abstract here if you would like it shown on this page
abstract: ''
summary: 'A GSIS-based solver for phonon transport under fast periodic heating, as in frequency-domain thermoreflectance experiments: it converges within dozens of iterations and stays accurate on coarse meshes (asymptotic preserving).'

tags:
  - GSIS
  - Thermoreflectance
featured: false

url_pdf: ''

image:
  filename: research/fdtr.png
  caption: ''
  focal_point: ''
  preview_only: true

projects:
  - fdtr
---

Frequency-domain thermoreflectance heats a sample with a modulated laser, so the phonon Boltzmann equation has two spatial Knudsen numbers (normal and resistive scattering) and a temporal one set by the heating frequency. This paper builds a GSIS solver that is **fast-converging** across a wide range of Knudsen numbers and frequencies and **asymptotic-preserving**, so that cells can be much larger than the phonon mean free path in the bulk. It then examines how the heating frequency changes heat conduction in different transport regimes.
