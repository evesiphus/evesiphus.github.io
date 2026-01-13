---
layout: page
title: Large-scale Network Modeling (RSMA/NGMA)
description: Analytical frameworks for RSMA, NOMA, and OMA under discrete rate adaptation.
img: assets/img/publication_preview/RSMA.jpg
importance: 2
category: Research
related_publications: true
---

This research introduces a unified analytical framework based on **Stochastic Geometry (SG)** to evaluate Next-Generation Multiple Access (NGMA) techniques, specifically focusing on the practical constraints of **Modulation and Coding Scheme (MCS)** adaptation.

### 1. Unified Analytical Framework
While traditional models often assume continuous Shannon rates, our work bridges the gap between theory and practice by integrating **discrete rate adaptation**. We model the uplink cellular network with Poisson-distributed Base Stations (BS) and User Equipments (UE), capturing the spatial interference coupling inherent in large-scale deployments.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/RSMA.jpg" title="RSMA Performance Analysis" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Spatial interference modeling and rate adaptation in dense RSMA-enabled networks.
</div>

### 2. Key Contributions
* **MCS Adaptation Modeling:** We define the conditional received rate by quantizing the channel quality (SIR) using sets of thresholds. Higher SIR levels trigger higher-order modulation, leading to increased received rates.
* **Meta Distribution Analysis:** We derive tractable expressions for the **meta distribution** of the conditional received rate, allowing us to quantify not just the average performance, but also the user-specific reliability and fairness (fine-grained statistics).
* **Performance Metrics:** The framework provides closed-form expressions and Beta approximations for:
    * Spatially-average Spectral Efficiency (SE).
    * Variance of the SE.
    * CRR (Conditional Received Rate) statistics.

### 3. Comparing OMA, NOMA, and RSMA
Our results show how discrete rate adaptation reshapes interference dynamics. The unified framework generalizes existing NOMA and OMA analyses, providing new insights into interference management and spectral efficiency in dense 6G-ready networks.

---

### Technical Highlights
* **Tools:** Stochastic Geometry, Point Process Theory, Meta Distribution, MATLAB/Python Simulations.
* **Key Parameters:** UE activity factor, uplink power control coefficients, and SIR thresholds.



> Related Publications:
> * *Uplink RSMA Performance Analysis with Rate Adaptation*, arXiv:2512.20883.
> * *Stochastic Geometry-Based MCS Adaption Analysis*, IEEE WCNC 2025.
