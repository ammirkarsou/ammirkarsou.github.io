---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D. in Earth and Ocean Dynamics, Fluminense Federal University (UFF), 2023 – present  
  * Thesis (in progress): Pseudospectral anisotropic RTM/FWI.
* M.Sc. in Earth and Ocean Dynamics, Fluminense Federal University (UFF), 2018 – 2020  
  * Thesis: GPU acceleration with OpenACC for modeling/FWI.
* B.Sc. in Geophysics, Fluminense Federal University (UFF), 2012 – 2017  
  * Thesis: Viscoacoustic & AVO data modeling using the Zoeppritz equation and its approximations.

Work experience
======
* Jan 2021 – present: Researcher, Seismic Inversion and Imaging Group (GISIS) — Rio de Janeiro, Brazil
  * Developing 2D/3D seismic modeling and FWI/RTM software; contributed to a UFF patent filing (2024).
  * Implemented inverse scattering imaging conditions (ISIC) that improved stacked images and interpretation confidence.
  * Built angle-domain common image gathers (ADCIGs) to QC velocity models and analyze azimuthal/angle-dependent reflectivity.
  * Added amplitude compensation that yields true-amplitude RTM images and ADCIGs, enabling noise-attenuated reflectivity when combined with ISIC.
  * Generated illumination maps from acquisition geometry to disambiguate refraction versus reflection energy and guide data selection for FWI.
  * Applied advanced processing (noise, ghost, bubble, signature removal) to novel circular OBN datasets prepared for FWI.
  
Skills
======
* Programming: C/C++, Python, CUDA, Git.
* Imaging & HPC: Full waveform inversion, reverse time migration, high-performance computing, parallel programming.
* Processing & Interpretation: Seismic processing, velocity model building, angle gathers/QC, wave propagation.

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
