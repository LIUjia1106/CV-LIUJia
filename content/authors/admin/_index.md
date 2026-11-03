---
# Display name
title: Jia Liu

# Name pronunciation (optional) - shown above the name
name_pronunciation: 刘佳

# Full name (for SEO)
first_name: Jia
last_name: Liu

# Status emoji (shown on the avatar)
status:
  icon: 🌡️

# Is this the primary user of the site?
superuser: true

# Highlight the author in author lists? (true/false)
highlight_name: true

# Role/position/tagline
role: Ph.D. Student · Multiscale Heat Transfer

# Organizations/Affiliations to display in Biography blox
organizations:
  - name: EMIA, The Hong Kong University of Science and Technology
    url: https://hkust.edu.hk/

# Social network links
# Need to use another icon? Simply download the SVG icon to your `assets/media/icons/` folder.
profiles:
  - icon: at-symbol
    url: 'mailto:jliugh@connect.ust.hk'
    label: E-mail Me
  - icon: academicons/google-scholar
    url: https://scholar.google.com/citations?user=FLE72QUAAAAJ
    label: Google Scholar
  - icon: academicons/orcid
    url: https://orcid.org/0000-0001-9171-4022
    label: ORCID
  - icon: brands/github
    url: https://github.com/LIUjia1106
    label: GitHub
  - icon: brands/linkedin
    url: https://www.linkedin.com/in/jialiu00
    label: LinkedIn
  - icon: brands/x
    url: https://x.com/jia_liu00
    label: X
  - icon: brands/instagram
    url: https://www.instagram.com/jialiu00
    label: Instagram

interests:
  - Multiscale heat transfer
  - Phonon & electron–phonon Boltzmann transport
  - Fast iterative & asymptotic-preserving solvers
  - Reduced-order modelling

education:
  - area: Ph.D., Individualized Interdisciplinary Program (EMIA)
    institution: The Hong Kong University of Science and Technology
    date_start: 2024-09-02
    date_end: 2028-06-30
    summary: |
      Expected June 2028. Advisors: [Prof. Wei Su](https://weisu-mae.github.io/) and Prof. Yanguang Zhou (co-advisor).

      Tentative dissertation: _General Synthetic Iterative Scheme and Proper Generalized Decomposition for Efficient Boltzmann Transport Solvers_.

      CGA 3.80 / 4.30 · Selected coursework: Advanced Numerical Methods I (A+) & II (A), Mathematical Methods in Science and Engineering I (A−), Statistical Machine Learning (A−).
  - area: M.Sc. in Mechanics
    institution: Southern University of Science and Technology (SUSTech)
    date_start: 2021-09-01
    date_end: 2024-06-30
    summary: |
      Advisor: Prof. Lei Wu. Thesis: _General Synthetic Iterative Scheme for Phonon Boltzmann Equation_ - awarded **SUSTech Outstanding Master's Thesis**.

      University-level Outstanding Graduate (2024).
  - area: B.Sc. in Information and Computational Science
    institution: Xiangtan University
    date_start: 2017-09-01
    date_end: 2021-06-30
    summary: |
      GPA 3.69 / 4.0 · Ranked 3 / 116 · First Class Scholarship (four times).

work:
  - position: Graduate Researcher
    company_name: HKUST - Division of Emerging Interdisciplinary Areas
    company_url: ''
    company_logo: ''
    date_start: 2024-09-02
    date_end: ''
    summary: |2-
      Fast solvers for multiscale phonon and electron transport, with Prof. Wei Su and Prof. Yanguang Zhou.
      - General synthetic iterative scheme (GSIS) for the coupled electron–phonon Boltzmann equations
      - Synthetic iterative scheme for the non-gray phonon BTE with dual relaxation times
      - Proper generalized decomposition with synthetic preconditioning for parametric phonon transport
  - position: Teaching Assistant
    company_name: HKUST
    company_url: ''
    company_logo: ''
    # TODO(Jia): replace with the real term of your first HKUST TA duty
    date_start: 2024-09-02
    date_end: ''
    summary: |2-
      Two courses during my Ph.D. study (class size: 30).
  - position: Graduate Researcher
    company_name: SUSTech - Department of Mechanics and Aerospace Engineering
    company_url: ''
    company_logo: ''
    date_start: 2021-09-01
    date_end: 2024-06-30
    summary: |2-
      Kinetic theory and multiscale heat transfer, with Prof. Lei Wu.
      - Proposed a GSIS for the phonon Boltzmann equation with dual relaxation times - up to three orders of magnitude fewer iterations than the conventional scheme
      - Developed a fast-converging, asymptotic-preserving method for simulating frequency-domain thermoreflectance (FDTR)
      - SUSTech Climbing Plan (2022): acceleration algorithms and a high-performance solver for multiscale rarefied gas flows
  - position: Teaching Assistant
    company_name: SUSTech
    company_url: ''
    company_logo: ''
    date_start: 2022-03-01
    date_end: 2022-07-31
    summary: |2-
      2-credit postgraduate course, 62 students. Awarded **Outstanding Graduate Teaching Assistant**.
  - position: Undergraduate Researcher
    company_name: Xiangtan University
    company_url: ''
    company_logo: ''
    date_start: 2019-01-01
    date_end: 2019-12-31
    summary: |2-
      National College Students' Innovation and Entrepreneurship Training Program: kinetic Boltzmann models and numerical methods for magnetic-field fluidized bed problems.

# Skills
# Icons: hero icons (e.g. `fire`), `devicon/<name>` or `hb/<name>`; or add your own SVG to `assets/media/icons/`.
skills:
  - name: Research toolkit
    items:
      - name: Synthetic iterative acceleration (GSIS)
        description: 'Fast convergence from ballistic to diffusive regimes'
        icon: bolt
      - name: Asymptotic-preserving schemes
        description: 'Accurate on coarse meshes in the diffusive limit'
        icon: variable
      - name: Reduced-order modelling (PGD)
        description: 'Fast parametric studies of phonon transport'
        icon: squares-2x2
      - name: C++ & Fortran
        description: 'Developing, verifying and optimizing kinetic solvers'
        icon: devicon/cplusplus
      - name: MATLAB & LaTeX
        description: 'Prototyping, post-processing and writing'
        icon: devicon/matlab
  - name: Off the clock
    color: '#eeac02'
    color_border: '#f0bf23'
    items:
      - name: Travel & hiking
        description: 'Mountain trails, new cities and local food'
        icon: hb/person-simple-walk
      # TODO(Jia): fill in your music taste
      - name: Music
        description: '[What you listen to or play]'
        icon: musical-note
      - name: Writing
        description: 'Notes on Ph.D. life, research and travel'
        icon: pencil-square

# Awards (newest first). `date_start` is used for sorting, `date` for display.
awards:
  - title: Outstanding Master's Thesis
    awarder: Southern University of Science and Technology
    date: '2024-06-30'
    date_start: '2024-06-30'
    summary: |
      For the thesis _General Synthetic Iterative Scheme for Phonon Boltzmann Equation_.
  - title: Outstanding Graduate (university level)
    awarder: Southern University of Science and Technology
    date: '2024-06-29'
    date_start: '2024-06-29'
    summary: ''
  - title: Outstanding Graduate Teaching Assistant
    awarder: Southern University of Science and Technology
    date: '2022-07-31'
    date_start: '2022-07-31'
    summary: ''
  - title: Second Prize (Hunan Division)
    awarder: China Undergraduate Mathematical Contest in Modeling
    date: '2019-12-01'
    date_start: '2019-12-01'
    summary: ''
  - title: First Class Scholarship · Merit Student
    awarder: Xiangtan University
    date: '2021-06-01'
    date_start: '2021-06-01'
    summary: |
      Top 5%, awarded four times each (2017–2021).
---

I'm **Jia Liu (刘佳)**, a Ph.D. student at the Hong Kong University of Science and Technology. I study how heat moves when things get small or fast, down to the scale where Fourier's law breaks down. At that scale, heat is carried by phonons and electrons that have to be tracked with the Boltzmann transport equation.

Those equations are notoriously expensive to solve, especially when a single device mixes ballistic and diffusive transport. My work is about making them **fast and reliable**. I develop general synthetic iterative schemes (GSIS) that reach converged solutions in dozens of iterations instead of thousands, asymptotic-preserving methods that stay accurate on coarse meshes, and reduced-order models for parametric studies. I work with [Prof. Wei Su](https://weisu-mae.github.io/) and Prof. Yanguang Zhou; before HKUST I did my M.Sc. with Prof. Lei Wu at SUSTech.

When I'm not iterating, I'm usually travelling: hiking a mountain trail or hunting down good local food. 🥾

**I will finish my Ph.D. in mid-2028 and am open to postdoctoral opportunities.** [Let's talk](mailto:jliugh@connect.ust.hk). · [中文简历 (PDF)](/uploads/resume-zh.pdf)
