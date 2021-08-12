---
title: "The GAMERA MHD code"
excerpt: "High resolving power numerical methods for MHD<br/>"
collection: portfolio
---

## The GAMERA MHD code

Yes Gamera is a giant Japanese turtle, for us it's just a piece of elegant code that solves the equations of magnetohydrodynamics (MHD) in non-orthogonal, curvilinear grids. Gamera stands for "Grid Agnostic MHD for Extended Research Applications" Here's the "official" design of the Gamera logo by artist at the Johns Hopkins University (JHU/APL).

<img src='../gamera.png'>

Gamera is a new magnetohydrodynamic (MHD) code for simulation of diverse magnetized plasma environments. It is a full rewrite of the high-heritage Lyon-Fedder-Mobarry (LFM) model. Gamera is a flexible, portable, user-friendly and exascale-capable code designed to take advantage of supercomputer architectures of the future.

## A brief history of the LFM code

* Do you know what's the order of spatial differencing used in the first LFM paper published in Phys. Rev. Lett. in 1982?
  * It's twentieth-order. Yes it sounds crazy but it did get the job done: with 40x50 computational cells, Professor John Lyon and colleagues were able to resolve the structure of the Earth's magnetosphere including the bow shock, the magnetopause and the magnetotail, even created a numerical substorm. This is called "state-of-art". Here is a not-so-complete list of the development of the LFM code in the past three decades:
  
The LFM code has some quite unique numerics to handle magnetospheric problems (basically hitting a beta<1e-5 plasma in a dipole field with a Mach 10 flow):

- Non-orthogonal finite volume for (singular) curvilinear grids;
- High-order (8th-order) spatial reconstruction;
- Very low numerical diffusion (3-D grid Reynolds number > 1e6);
- High-order, non-orthogonal constraint transport for divB = 0.
- and more...

The code still runs quite well on existing architectures (right now it's the NCAR Cheyenne super computer system). However the code was written almost 40 years ago and speed and portability on future supercomputers become an issue with time. Also the majority of the community does not have access to the code and cannot adapt the LFM code to their own research applications easily. Therefore we re-envisaged the LFM to be Gamera. 

## What's new about GAMERA?

Gamera is a new magnetohydrodynamic (MHD) simulation tool building and improving upon the high-heritage Lyon-Fedder-Mobarry (LFM) code. Gamera has been written completely from scratch in modern Fortran and provides a flexible, portable, and exascale-capable MHD code. Gamera features multiple improvements over LFM including: minimal external library dependence, high degree of optimization, OpenMP parallelism allowing the use of heterogeneous architectures, and multiple numerics upgrades. Thus, while preserving all key numerical algorithms underlying the LFM code, Gamera provides a robust and user-friendly solution for sustainable future.

Well the name is originally from Professor John Lyon, given that the name "Lyon-Fedder-Mobarry" did not come from himself, it's fair that he got the chance to name his terrific and extraordinary contribution to the group and the space physics community.
