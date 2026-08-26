---
layout: archive
title: "GAMERA-OP"
permalink: /gamera-op/
author_profile: true
description: "GAMERA-OP is a high-order finite-volume MHD solver for orthogonal curvilinear geometries and planetary plasma applications."
excerpt: "A high-order finite-volume MHD solver for orthogonal curvilinear geometries."
redirect_from:
  - /talks/
  - /talks/2012-03-01-talk-1
  - /talkmap.html
---

<img class="gamera-hero" src="/images/gamera.png" alt="GAMERA code mascot over a curvilinear computational grid">

GAMERA-OP (Orthogonal-Plus) is a three-dimensional finite-volume magnetohydrodynamics solver for orthogonal curvilinear geometries. Rewritten in C with a modular design, it provides a practical framework for planetary, space, and astrophysical plasma simulations that require high-order accuracy and robust treatment of curved coordinates.

<div class="action-row">
  <a class="btn btn--primary" href="https://doi.org/10.3847/1538-4365/ae7344">Journal article</a>
  <a class="btn" href="https://arxiv.org/abs/2602.12307">arXiv preprint</a>
  <a class="btn" href="https://github.com/ijmhd">GitHub projects</a>
</div>

## Core capabilities

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

## Numerical design

![GAMERA-OP grid and field-variable arrangement](/images/gamera-op-grid.png){: .gamera-grid }

The solver combines geometry-consistent high-order reconstruction with flexible numerical fluxes and time integrators. Its architecture is designed to simplify case setup, addition of new physics, and coupling to other first-principles models. Standard benchmarks across multiple geometries demonstrate accuracy, low numerical diffusion, and robust treatment of coordinate singularities and rotating flows.

## Reference

H. Luo, B. Zhang, J. Tian, J. Cai, J. Chen, E. Feng, Z. Zheng, S. Xi, and J. G. Lyon (2026), “GAMERA-OP: A Three-dimensional Finite-volume Magnetohydrodynamic Solver for Orthogonal Curvilinear Geometries,” *The Astrophysical Journal Supplement Series*, **285**(1), 15. [https://doi.org/10.3847/1538-4365/ae7344](https://doi.org/10.3847/1538-4365/ae7344)
