---
# Leave the homepage title empty to use the site title
title: ""
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: "5rem"

sections:
  # ── Hero: avatar, name, bio (from content/authors/admin/_index.md) ──
  - block: resume-biography-3
    content:
      username: admin
      text: ""
      button:
        text: Download CV
        # TODO(Jia): replace static/uploads/resume.pdf with your latest CV (it is still the 2023 version)
        url: uploads/resume.pdf
    design:
      css_class: dark jl-hero
      background:
        color: '#0b1020'
        image:
          # A phonon lattice with heat flowing from hot (left) to cold (right) - see assets/media/
          filename: heat-lattice.svg
          filters:
            brightness: 1.0
          size: cover
          position: center
          parallax: false

  # ── Research themes (custom block: layouts/partials/blox/research-themes.html) ──
  - block: research-themes
    id: research
    content:
      title: Research
      subtitle: Making multiscale heat transfer simulations fast and reliable
      text: |-
        Below a few hundred nanometres, or faster than a few nanoseconds, heat no longer obeys Fourier's law. It is carried by **phonons** (and electrons) that fly, scatter and collide, described by the Boltzmann transport equation. Real devices mix all these regimes at once, which makes simulations painfully slow. I design numerical methods that stay **fast** and **accurate** from the ballistic to the diffusive limit.
      items:
        - title: General synthetic iterative schemes
          kicker: Speed
          icon: bolt
          text: Conventional iterations need thousands of sweeps when phonons scatter often. GSIS couples the kinetic equation with exactly derived macroscopic synthetic equations, so converged solutions come in dozens of iterations, up to three orders of magnitude faster.
          url: project/gsis/
          papers:
            - name: J. Comput. Phys. 2022
              url: publication/2022-jcp-gsis-dual-relaxation/
            - name: arXiv 2026
              url: publication/2026-arxiv-nongray-gsis/
        - title: Coupled electron–phonon transport
          kicker: Physics
          icon: cpu-chip
          text: In metals and semiconductors, hot electrons hand their energy to the lattice through electron–phonon coupling. I extend GSIS to the coupled electron–phonon Boltzmann equations so that both carriers can be simulated quickly across transport regimes.
          url: project/electron-phonon/
          papers:
            - name: Int. J. Heat Mass Transfer 2026
              url: publication/2026-ijhmt-electron-phonon-gsis/
        - title: Simulating thermoreflectance experiments
          kicker: Experiment
          icon: beaker
          text: Frequency-domain thermoreflectance (FDTR) measures thermal properties with a modulated laser. I built a fast-converging, asymptotic-preserving solver for this setting and used it to study how heating frequency changes heat conduction across regimes.
          url: project/fdtr/
          papers:
            - name: Commun. Comput. Phys. 2023
              url: publication/2023-cicp-fdtr/
        - title: Reduced-order modelling
          kicker: Scale
          icon: squares-2x2
          text: Design studies need the same simulation again and again over many parameters. I combine proper generalized decomposition (PGD) with synthetic preconditioning to make multiscale, parametric phonon transport affordable.
          url: project/pgd/
          papers:
            - name: arXiv 2026
              url: publication/2026-arxiv-pgd-synthetic-preconditioning/
      button:
        text: All research projects
        url: projects/

  # ── Interactive toy model (custom block: layouts/partials/blox/phonon-playground.html) ──
  - block: phonon-playground
    id: playground
    content:
      title: Play with phonons
      text: |-
        Drag the slider to change the **Knudsen number** (mean free path ÷ device size). When phonons scatter often (small Kn), the temperature drops linearly, just as Fourier's law predicts. When they fly freely (large Kn), the profile flattens and the temperature *jumps* at the walls. A good solver has to handle both, and everything in between.

  # ── Publications ──
  - block: collection
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - publication
        featured_only: true
    design:
      view: article-grid
      columns: 2
  - block: collection
    content:
      title: All Publications
      text: "Full list on [Google Scholar](https://scholar.google.com/citations?user=FLE72QUAAAAJ)."
      filters:
        folders:
          - publication
        exclude_featured: false
    design:
      view: citation

  # ── Talks ──
  - block: collection
    id: talks
    content:
      title: Talks
      filters:
        folders:
          - event
    design:
      view: date-title-summary

  # ── News (custom block: layouts/partials/blox/news-timeline.html) ──
  - block: news-timeline
    id: news
    content:
      title: News
      # Items after `count` are tucked behind a "Show earlier news" toggle
      count: 5
      items:
        - date: Oct 2026
          icon: document-text
          text: "New preprint: [PGD with synthetic preconditioning for multiscale parametric phonon transport](publication/2026-arxiv-pgd-synthetic-preconditioning/) is on arXiv."
        - date: Aug 2026
          icon: document-text
          text: "Co-authored preprint on a [synthetic iterative scheme for the non-gray phonon BTE](publication/2026-arxiv-nongray-gsis/) is on arXiv."
        # TODO(Jia): add the month the IJHMT paper went online
        - date: '2026'
          icon: newspaper
          text: "Our paper on [GSIS for coupled electron–phonon Boltzmann equations](publication/2026-ijhmt-electron-phonon-gsis/) is published in *International Journal of Heat and Mass Transfer*."
        - date: Apr 2025
          icon: microphone
          text: "Gave an oral presentation at **NETP 2025**, the 1st International Symposium on Non-Equilibrium Transport Phenomena, in Beijing."
        - date: Sep 2024
          icon: academic-cap
          text: "Started my Ph.D. at **HKUST** (EMIA) with Prof. Wei Su and Prof. Yanguang Zhou."
        - date: Jun 2024
          icon: trophy
          text: "Graduated from SUSTech: my M.Sc. thesis was named an **Outstanding Master's Thesis**, and I was named a university-level **Outstanding Graduate**."
        - date: Aug 2023
          icon: newspaper
          text: "[Fast-converging and asymptotic-preserving simulation of FDTR](publication/2023-cicp-fdtr/) is published in *Communications in Computational Physics*."
        - date: Jul 2022
          icon: sparkles
          text: "My first paper is out in *Journal of Computational Physics*, and I gave my first international talk at **RGD32** in Seoul."

  # ── Life teaser (custom block: layouts/partials/blox/beyond-lab.html) ──
  - block: beyond-lab
    id: life
    content:
      title: Beyond the lab
      text: Heat flows from hot to cold. I flow from the lab to the mountains.
      items:
        - emoji: ⛰️
          title: On the trail
          # TODO(Jia): your favourite trail or mountain
          text: Hiking is how I reset. Favourite so far - [trail / mountain].
        - emoji: 📷
          title: '[Hobby 2]'
          text: '[A sentence about it]'
        - emoji: 🎵
          title: '[Hobby 3]'
          text: '[A sentence about it]'
      button:
        text: More about life outside research
        url: life/

  # ── Contact call-to-action ──
  - block: cta-card
    id: contact
    content:
      title: Let's work together
      text: |-
        I will complete my Ph.D. in **mid-2028** and am looking for **postdoctoral positions** in computational heat transfer, kinetic theory and scientific computing. I'm also always happy to talk about collaborations.
      button:
        text: Email me
        url: mailto:jliugh@connect.ust.hk
    design:
      card:
        css_class: "jl-cta"
        css_style: ""
---
