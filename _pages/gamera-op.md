---
layout: archive
title: "Codes"
permalink: /codes/
author_profile: true
description: "Research software and teaching codes developed and used by the PSEM Group, including GAMERA, GAMERA-YinYang, GAMERA-OP, and MATLAB learning resources."
excerpt: "Research software, numerical solvers, and teaching codes from the PSEM Group."
redirect_from:
  - /gamera-op/
  - /gamera-op/index.html
  - /talks/
  - /talks/2012-03-01-talk-1
  - /talkmap.html
---

<div class="codes-intro">
  <p class="codes-kicker">PSEM Group software</p>
  <p class="codes-lead">Models, solvers, and learning tools for planetary plasma physics. This page brings together the research codes we develop and use, alongside compact teaching versions that make the numerical ideas easier to explore.</p>
  <div class="action-row">
    <a class="btn btn--primary" href="https://github.com/ijmhd">Browse GitHub projects</a>
    <a class="btn" href="/teaching/">Teaching &amp; learning</a>
  </div>
</div>

<div class="codes-grid">
  <article id="gamera-op" class="code-card code-card--featured">
    <header class="code-card__header">
      <p class="code-card__eyebrow">Research code</p>
      <span class="code-status code-status--published">Published</span>
    </header>
    <h2>GAMERA-OP</h2>
    <p class="code-card__subtitle">High-order MHD on orthogonal curvilinear grids</p>
    <p>A modular three-dimensional finite-volume solver for planetary, space, and astrophysical plasma simulations. Its geometry-aware formulation supports accurate and conservative calculations on Cartesian, cylindrical, spherical, and other orthogonal grids.</p>
    <ul class="code-tags" aria-label="GAMERA-OP topics">
      <li>C</li>
      <li>Finite volume</li>
      <li>Global MHD</li>
    </ul>
    <div class="code-card__links">
      <a href="#gamera-op-details">Technical overview</a>
      <a href="https://doi.org/10.3847/1538-4365/ae7344">Journal article</a>
      <a href="https://arxiv.org/abs/2602.12307">arXiv</a>
    </div>
  </article>

  <article id="gamera-yinyang" class="code-card">
    <header class="code-card__header">
      <p class="code-card__eyebrow">Research code</p>
      <span class="code-status code-status--development">In development</span>
    </header>
    <h2>GAMERA-YinYang</h2>
    <p class="code-card__subtitle">Global plasma modeling on a Yin–Yang grid</p>
    <p>A GAMERA framework for global spherical simulations using overlapping grid patches, designed for efficient treatment of planetary systems without a polar coordinate singularity.</p>
    <ul class="code-tags" aria-label="GAMERA-YinYang topics">
      <li>Yin–Yang grid</li>
      <li>Global models</li>
      <li>Planetary plasma</li>
    </ul>
    <p class="code-card__note">Project notes, publications, and access information will be added as the code develops.</p>
  </article>

  <article id="gamera" class="code-card">
    <header class="code-card__header">
      <p class="code-card__eyebrow">Research code</p>
      <span class="code-status">Core framework</span>
    </header>
    <h2>GAMERA</h2>
    <p class="code-card__subtitle">MHD on non-orthogonal curvilinear grids</p>
    <p>The original high-order finite-volume framework for three-dimensional magnetohydrodynamics on distorted grids, built for accurate large-scale space and astrophysical plasma simulations.</p>
    <ul class="code-tags" aria-label="GAMERA topics">
      <li>Curvilinear grids</li>
      <li>High-order methods</li>
      <li>HPC</li>
    </ul>
    <div class="code-card__links">
      <a href="https://scholar.google.com/scholar?q=GAMERA+three-dimensional+finite-volume+MHD+solver+non-orthogonal+curvilinear+geometries">Find the reference</a>
    </div>
  </article>

  <article id="matlab-teaching" class="code-card code-card--teaching">
    <header class="code-card__header">
      <p class="code-card__eyebrow">Teaching code</p>
      <span class="code-status code-status--planned">Planned release</span>
    </header>
    <h2>MATLAB Teaching Codes</h2>
    <p class="code-card__subtitle">Small models for learning by experimenting</p>
    <p>Compact, readable examples for teaching numerical modeling, data analysis, MHD, and plasma dynamics. Future downloads will connect directly to course notes and guided exercises.</p>
    <ul class="code-tags" aria-label="MATLAB teaching code topics">
      <li>MATLAB</li>
      <li>Course exercises</li>
      <li>Interactive learning</li>
    </ul>
    <div class="code-card__links">
      <a href="/teaching/">Explore the courses</a>
    </div>
  </article>
</div>

<section id="gamera-op-details" class="code-detail" aria-labelledby="gamera-op-title">
  <header class="code-detail__header">
    <div>
      <p class="codes-kicker">Featured technical overview</p>
      <h2 id="gamera-op-title">Inside GAMERA-OP</h2>
    </div>
    <a class="btn" href="https://github.com/ijmhd">GitHub projects</a>
  </header>

  <div class="research-grid research-grid--compact">
    <article class="research-card">
      <h3>Geometry-aware numerics</h3>
      <p>High-order finite-volume reconstruction on Cartesian, cylindrical, spherical, and other orthogonal curvilinear grids.</p>
    </article>
    <article class="research-card">
      <h3>Divergence control</h3>
      <p>Constrained transport preserves the solenoidal magnetic-field condition to machine precision.</p>
    </article>
    <article class="research-card">
      <h3>Rotating systems</h3>
      <p>Angular momentum is conserved to round-off in cylindrical and spherical coordinates, supporting rapidly rotating planetary systems.</p>
    </article>
    <article class="research-card">
      <h3>Extended physics</h3>
      <p>Options include ring averaging near the axis, semi-relativistic correction, background-field splitting, and anisotropic MHD.</p>
    </article>
  </div>

  <figure class="code-detail__figure">
    <img class="gamera-grid" src="/images/gamera-op-grid.png" alt="GAMERA-OP curvilinear grid and field-variable arrangement" loading="lazy">
    <figcaption>Grid geometry and field-variable arrangement in GAMERA-OP.</figcaption>
  </figure>

  <p>The solver combines geometry-consistent high-order reconstruction with flexible numerical fluxes and time integrators. Its modular architecture is designed to simplify case setup, the addition of new physics, and coupling to other first-principles models.</p>

  <div class="code-reference">
    <p class="codes-kicker">Reference</p>
    <p>H. Luo, B. Zhang, J. Tian, J. Cai, J. Chen, E. Feng, Z. Zheng, S. Xi, and J. G. Lyon (2026), “GAMERA-OP: A Three-dimensional Finite-volume Magnetohydrodynamic Solver for Orthogonal Curvilinear Geometries,” <em>The Astrophysical Journal Supplement Series</em>, <strong>285</strong>(1), 15. <a href="https://doi.org/10.3847/1538-4365/ae7344">https://doi.org/10.3847/1538-4365/ae7344</a></p>
  </div>
</section>
