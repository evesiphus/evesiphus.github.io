---
layout: page
title: AI/ML for High-Speed Softwarized Networks
description: Predictive models and MLOps platform for high-performance NFV data planes.
img: assets/img/publication_preview/MLOpsIpm.png
importance: 1
category: Research
related_publications: true
---

This project focuses on operationalizing AI/ML to enhance the performance, diagnosis, and sustainability of modern softwarized networks.

### 1. Non-intrusive Network Measurement
Instead of traditional packet-level feature collection, we leverage low-level hardware features available in commodity servers (e.g., **CPU cores, multi-level caches, memory subsystems, and PCIe buses**). This approach ensures minimal impact on normal network operations while providing deep insights into system behavior.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/MLOpsIpm.png" title="Measurement Framework" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Overview of the non-intrusive measurement framework and MLOps components.
</div>

### 2. Performance Diagnosis & Bottleneck Detection
We develop advanced predictive models to:
* **Infer performance impairments** in high-speed NFV data planes.
* **Deduce associated bottlenecks** (e.g., CPU contention, cache misses).
* Enable proactive management of virtualized network functions (VNF).

### 3. Operationalizing AI & MLOps Platform
To replace traditional "one-shot" ML models, we developed a continuous, trigger-based system:
* **MLOps Platform:** Components designed for continuous performance prediction and anomaly detection.
* **Sustainability:** Reducing overhead and enhancing the long-term reliability of AI models in production environments.

---

### Key Technical Aspects
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/publication_preview/arch.jpg" title="System Architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    System architecture for proactive VNF redeployment and traffic routing.
</div>

> You can find more details in the [Publications](/publications/) section, specifically under the "Operationalizing AI" and "Proactive VNF Redeployment" papers.
