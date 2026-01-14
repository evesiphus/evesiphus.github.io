---
layout: page
title: AI/ML for High-Speed Softwarized Networks
description: "(2022 - Present) A framework for non-intrusive performance intelligence and drift-resilient MLOps in NFV data planes."
img: assets/img/publication_preview/MLOpsIpm.png
importance: 1
category: Research
related_publications: true
---

## 1. Research Background & Motivation

### The Performance Gap in Network Softwarization
The shift from monolithic hardware appliances to **Network Function Virtualization (NFV)** and **Software-Defined Networking (SDN)** has been accelerated by high-speed I/O technologies such as **DPDK, eBPF, and netmap**. While these stacks allow commodity off-the-shelf (COTS) servers to reach 10/40/100 Gbps regimes, they introduce intrinsic obstacles. Unlike dedicated circuits, software data planes are susceptible to performance impairments due to the shared nature of the underlying virtual infrastructure.

### Resource Contention in COTS Servers
Modern COTS servers rely on multi-socket NUMA (Non-Uniform Memory Access) architectures with hierarchical cache designs (L1/L2/L3). Our research focuses on the intricate interactions and contentions within these subsystems:
* **Cache Contention:** Concurrent VNFs compete for the **Last-level Cache (LLC)**. Even with Intel® CAT, "leaky DMA" issues in technologies like Intel® DDIO can saturate the cache.
* **Memory & I/O Bottlenecks:** Low-level cache misses often lead to memory bandwidth saturation, while cross-node traffic triggers QPI (QuickPath Interconnect) contention, severely degrading throughput and latency.



---

## 2. Challenges in Existing Solutions
Despite the growth of ML-based analytics, traditional approaches face significant hurdles:
1. **Instrumentation Overhead:** Direct feature collection (e.g., packet mirroring) incurs a high resource footprint, often damaging both data fidelity and network performance.
2. **Heterogeneity:** Customizing code for VNFs from different vendors is operationally burdensome.
3. **Model Decay:** The data-driven nature of ML leads to model decay as network systems evolve, making it strenuous to sustain accuracy under continuous data drift.

---

## 3. Proposed Framework: Non-Intrusive Performance Intelligence

We propose a novel framework that leverages **low-level hardware features** (e.g., CPU pipeline cycles, LLC misses, RAM bandwidth) acquired through standard profiling tools. This approach provides "side-channel" visibility into the runtime state without touching the high-speed data plane.

### Core Components
* **Non-intrusive Analytics:** Leveraging ubiquitous hardware telemetry to derive actionable insights with negligible overhead.
* **MLOps Pipeline with DRST:** We implement a Drift Resilient and Self-Tuning (DRST) capability. This enables the system to detect when the underlying data distribution shifts and trigger adaptive retraining to maintain long-term accuracy.


### Performance Diagnosis & Orchestration
Our framework goes beyond singleton VNFs, analyzing complex **Service Function Chains (SFCs)** and **Directed Acyclic Graphs (DAGs)**. By predicting performance impairments (e.g., micro-bursts, packet drops), the system can proactively trigger VNF redeployment and traffic rerouting.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/MLOpsIpm.png" title="MLOps Pipeline" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The end-to-end MLOps pipeline featuring non-intrusive measurement and self-tuning capabilities.
</div>

---

## Related Publications

* **Q. Liu**, J. Lin, T. Zhang, L. Linguaglossa, “Non-Intrusive MLOps-Driven Performance Intelligence in Software Data Planes”, *Computer Networks*, 2025 (Under Revision).
* **Q. Liu**, T. Zhang, M. Hemmatpour, et al, ”Operationalizing AI/ML in Future Networks: A Bird’s Eye View from the System Perspective”, *IEEE Communications Magazine*, 2024.
* **Q. Liu**, T. Zhang, L. Linguaglossa, ”Non-invasive Performance Diagnosis of Virtual Network Functions with Limited Knowledge”, *IEEE INFOCOM*, 2024.
* **Q. Liu**, T. Zhang, W. Cerroni, L. Linguaglossa, ”Proactive VNF Redeployment and Traffic Routing for Modern Telco Networks,” *IEEE NetSoft*, 2024.
