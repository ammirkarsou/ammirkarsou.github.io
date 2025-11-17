---
title: "Aceleração dos algoritmos de modelagem acústica e elástica e da inversão do campo de onda completo (FWI) em GPU utilizando OpenACC"
collection: "publications"
category: "thesis"
permalink: "/publication/aceleracao-dos-algoritmos-de-modelagem-acustica-e-elastica-e-da-inversao-do-camp/"
date: "2020-01-01"
venue: "MSc Thesis — Federal Fluminense University (UFF)"
paperurl: "https://app.uff.br/riuff/handle/1/24811"
citation: "<strong>Ammir Ayman Karsou</strong> (2020). Aceleração dos algoritmos de modelagem acústica e elástica e da inversão do campo de onda completo (FWI) em GPU utilizando OpenACC. MSc Thesis — Federal Fluminense University (UFF). Advisor: Marco Antonio Cetale Santos."
excerpt: "Develops acoustic/elastic modeling and FWI kernels on GPUs with OpenACC to achieve high performance without hardware lock-in, reporting major speedups and analyzing communication/memory trade-offs."
---

<strong>Authors:</strong> <strong>Ammir Ayman Karsou</strong>

<strong>Advisor:</strong> Marco Antonio Cetale Santos

<strong>Program:</strong> PPGDOT — Graduate Program in Ocean and Earth Dynamics

Develops and accelerates <strong>acoustic and elastic modeling</strong> plus <strong>FWI</strong> on <strong>GPUs</strong> using <strong>OpenACC</strong>, targeting high performance with minimal hardware lock-in. Reports significant speedups and examines communication/memory costs and parallelization choices that drive scalability.

<strong>Highlights</strong>
- Portability through <strong>OpenACC</strong>, requiring less effort than CUDA for classic kernels.
- Acceleration of <strong>FWI</strong> and wave propagators with detailed bottleneck analysis (memory vs. FLOPs).
- Reproducible results supported by benchmarks on both synthetic and field-inspired cases.
