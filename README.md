# 🌐 CRUX: Advanced RF Analytics & Traffic Intelligence Engine

## 🚀 Executive Summary

**CRUX** is an enterprise-grade Radio Access Network (RAN) analytics platform designed to solve one of the most complex challenges in telecommunications: **deterministic network optimization.** 

Traditional network optimization relies on static distance rules, generic coverage footprints, and reactive manual analysis. **CRUX** revolutionizes this by combining **3D geospatial physics** with **live subscriber mobility traffic**. 

The engine operates in three continuous phases:
1. **Intelligent Neighbor Discovery:** Mathematically defining the physical environment to predict where handovers *should* happen.
2. **Handover (HO) Verification:** Using live network traffic to *prove* if a theoretical neighbor is a valid relation or a false anomaly (e.g., an overshooter).
3. **Coverage Integrity (Timing Advance):** Continuously tracking the physical footprint of the cell to guarantee it is serving its intended area and detecting critical hardware anomalies like cross-sectors.

By automating these highly complex evaluations, CRUX eliminates false handovers, prevents revenue-impacting coverage bleeds, and dramatically reduces optimization OPEX.

---

## 🌍 Phase 1: Intelligent Neighbor Discovery (Geospatial Engine)

Before looking at live traffic, CRUX builds a mathematically pure, physics-aware model of the real world. It abandons traditional "fixed-radius" guessing and dynamically discovers potential neighbors based on topography and physical line-of-sight.

* **Topological Intelligence (Log-Space Island Engine):** Rather than using hardcoded distance limits, CRUX uses statistical variance to detect natural geographical breaks (e.g., urban density vs. rural isolation, lakes, deserts). It groups sites into logical "Islands," allowing the terrain to dictate the network structure.
* **Physics-Aware Line-of-Sight (Shadowing Engine):** CRUX actively detects physical blockages between towers. It applies angular diffraction models for dense cities and strict geometric corridors for rural areas, stripping away blocked paths before they waste computational power.
* **3D Terrain Evaluation:** Moving beyond flat maps, CRUX integrates high-fidelity satellite surface data (Digital Surface Models) to calculate the exact altitude differences between towers and the ground. It immediately flags high-risk topologies like sheer drop-offs, major hills, or clear valleys that risk signal overshoot.
* **Hardware Alignment Verification:** The engine calculates the exact azimuths and beamwidths of antennas to guarantee that Target and Candidate towers are physically "facing" each other, preventing poor-quality handovers from side or back lobes.

---

## 🚦 Phase 2: Handover Traffic Verification & Anomaly Detection

Geometry provides the theory; live traffic provides the reality. Once CRUX establishes a physically viable neighbor, it cross-references that relation against millions of real-world User Equipment (UE) handover attempts to confirm its validity.

* **The 1000-Point Hybrid Matrix:** CRUX unifies Phase 1 geometry with Phase 2 traffic into a single, deterministic **Confidence Score**. It grades relations on volume, geometric overlap, boresight alignment, and clear line-of-sight. Neighbors are automatically classified as *Anchor*, *Verified*, *Marginal*, or *Fake*.
* **Dual-Track Traffic Intelligence:** The engine evaluates both the raw volume of handovers and the percentage share of traffic. It actively protects vital rural links while automatically flagging heavily utilized but physically illogical paths as "Possible Overshooters."
* **Chronological Swap Detection:** CRUX deploys a continuous 14-day sliding window to detect unauthorized traffic shifts. If a cell suddenly loses traffic ("Bleed") while another surges, the engine mathematically proves the correlation, instantly alerting engineering teams to suspected hardware outages, dead neighbors, or cross-sector swaps.

---

## 📡 Phase 3: Coverage Integrity & Spatial Tracking (Timing Advance)

A cell may have verified neighbors, but is it actually serving the right neighborhood? Antennas can be physically bumped, tilted incorrectly, or miswired. CRUX utilizes Timing Advance (TA) propagation delays to continuously monitor the actual "breathing" footprint of the cell.

* **Continuous Spatial Tracking:** CRUX translates signal delay into physical distance, tracking the cell's **Core (Near users)**, **Median (Mid-range users)**, and **Edge (Fringe users)**. 
* **The State Machine:** The engine tracks these boundaries over time. If a coverage shift is detected, CRUX requires strict chronological proof over several days before moving the anomaly from "Developing" to "Confirmed," eliminating false alarms caused by natural network breathing or seasonal holidays.
* **Plain-English Anomaly Classification:** By analyzing how the core and edge of the network move, CRUX automatically categorizes complex RF degradation for management and field teams:
  * **Cross-Sector / Severe Core Loss:** The edge of the cell extends, but the near-tower traffic vanishes completely (indicating crossed wires or physical blockage).
  * **Critical Overshooter:** The center of mass shifts kilometers outward, absorbing traffic meant for other sites.
  * **Edge Shrinkage / Collapse:** The cell is losing its fringe users, indicating a drop in transmit power or a severe downtilt issue.

---

## ⚡ The Engine Beneath: Enterprise Scale

CRUX is built to handle the massive data payloads of modern telecommunications networks without failing. 
* **Out-of-Core Processing:** CRUX bypasses traditional memory limitations by utilizing a high-speed, serverless analytical database structure. It chunks, streams, and aggregates billions of rows of traffic data natively on disk.
* **Automated & Self-Healing:** By completely automating the extraction, aggregation, and scoring phases, CRUX frees elite engineering teams from manual spreadsheet analysis, allowing them to focus entirely on decisive network action.

***CRUX: Translating the laws of RF physics and live mobility data into deterministic, automated network excellence.***
