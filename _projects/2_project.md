---
layout: page
title: Large-scale Modeling of NGMA Networks
description: "Unified analytical framework for uplink RSMA, NOMA, and OMA under spatial randomness and discrete rate adaptation."
importance: 2
category: Research
related_publications: false
---

## 1. Research Background & Motivation

### The Shift Toward Next-Generation Multiple Access (NGMA)
To meet the stringent requirements of 6G—such as massive connectivity and ultra-reliability—**Rate-Splitting Multiple Access (RSMA)** has emerged as a powerful paradigm. By splitting messages and employing **Successive Interference Cancellation (SIC)**, RSMA allows receivers to partially decode interference and partially treat it as noise, providing a flexible balance between interference cancellation and resource allocation.

### The Challenge of Uplink Large-Scale Networks
While downlink RSMA is well-studied, the uplink poses distinct modeling challenges:
* **Decentralized Management:** Independent transmissions from spatially distributed users lead to complex inter-cell interference coupling.
* **Channel-Dependent Decoding:** In the uplink, decoding orders are determined by relative channel conditions rather than fixed centralized precoding.
* **Spatial Randomness:** In dense 6G deployments, the inter-cell interference and spatial coupling become highly intensified, requiring tools beyond deterministic single-cell analysis.

---

## 2. Methodology: Stochastic Geometry & Meta Distribution

Our research bridges the gap between theoretical tractability and practical realism by introducing a unified analytical framework based on Stochastic Geometry (SG).

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/RSMA2.png" title="Large-scale Network Stochastic Modeling Framework" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The proposed analytical framework: From large-scale random topology to rate meta-distribution analysis.
</div>

### Bridging Discrete vs. Continuous Rate Models
Most existing SG-based analyses assume continuous rates based on Shannon’s capacity formula. In contrast, our framework integrates finite Modulation and Coding Scheme (MCS)-based rate adaptation. This approach quantifies the performance based on a finite set of Signal-to-Interference-plus-Noise Ratio (SINR) thresholds, which closely represents practical transmission behavior.

### Key Theoretical Contributions
* **Meta Distribution Analysis:** Beyond spatially-averaged metrics, we derive the **meta distribution** of the **Conditional Received Rate (CRR)**. This allows us to characterize not just the mean rate, but also the **user-specific reliability and fairness** (fine-grained statistics) across the entire network.
* **Unified Analytical Foundation:** We provide a generalized model that encompasses **OMA, NOMA, and RSMA** as special cases. This enables a systematic benchmarking of different access paradigms under identical spatial configurations.



---

## 3. Core Insights & Results

The proposed framework provides several new insights into the performance of dense RSMA-enabled networks:
1.  **Interference Dynamics:** We show how discrete rate adaptation reshapes the interference landscape, revealing that continuous-rate models often overestimate practical performance.
2.  **Tractable CRR Expressions:** We derived compact, closed-form expressions for the CRR and its higher-order statistics (moments), facilitating rapid system-level evaluation without exhaustive Monte Carlo simulations.
3.  **Generalization Gains:** Our results demonstrate that RSMA's ability to manage interference flexibly leads to significant gains in spectral efficiency and fairness compared to traditional NOMA and OMA in large-scale uplink deployments.

---

## Technical Highlights
* **Mathematical Tools:** Stochastic Geometry (Point Process Theory), Meta Distribution, Laplace Transforms, and Beta Approximation.
* **Key Metrics:** Conditional Received Rate (CRR), Spatially-averaged Spectral Efficiency (SE), and Rate Meta Distribution.
* **Simulation Environment:** Unified MATLAB/Python frameworks for cross-paradigm (RSMA/NOMA/OMA) benchmarking.

---

## Related Publications

* X. Guo, L. You$^\dagger$, **Q. Liu**$^\dagger$, X. G. Xia, X. Gao, “Uplink RSMA Performance Analysis with Rate Adaptation: A Stochastic Geometry Approach”, *Under Review (Journal)*, 2025.
* X. Guo, **Q. Liu**, S. Wang, L. You, X. Gao, “Stochastic Geometry-Based MCS Adaption Analysis in NGMA Networks”, *IEEE WCNC*, 2025.

($^\dagger$ *Corresponding Author*)
