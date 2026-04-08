---
title: "Systems Context"
layout: "single"
---

## Operations Overview

At the time of this incident, Seekers Spirits produced three core gin SKUs on a single 300L still: Seekers Mekong Dry Gin, Seekers Mekong Gold Gin, and Jason Kong Butterfly Pea Gin. Quality control (QC) was my responsibility end to end, from tasting through to final release decision. The production flow followed a simple sequence: ingredients received and visually inspected, batches produced, product rested, and finished product assessed at post-production QC before release. There were no formal quality gates upstream of production and no automated monitoring between stages. Any failure introduced at the ingredient stage would pass through every production stage before it could be caught.

Production and inventory records were held in spreadsheets at the time of this incident. The database queries referenced across these pages reproduce the investigation using a PostgreSQL schema built after the incident as part of this portfolio. Every query result is reproducible from that schema.


## Ingredient Supply Chain

Juniper berries were sourced from a Vietnam-based botanical supplier. Lot PDI-JNP-220620, 50kg, was received on 20 June 2022 and used across four consecutive batches between July and August 2022. The lot entered production unverified.

## Observability Gaps

Three gaps in the system contributed to late detection.

**No defined standard for incoming inspection.** Incoming inspection for raw material was subjective with no pass/fail criteria, meaning the same lot could be accepted or rejected depending on who conducted the check.

**No flavour baseline for incoming ingredients.** There was no reference point for how raw juniper should taste. Without a baseline, lot-to-lot variation could not be identified before entering production.

**No fixed reference point or cross-batch comparison.** Each batch was assessed against a randomly selected bottle from the warehouse rather than a designated baseline. Comparisons were inconsistent across runs, and there was no way to see whether quality was drifting over time. In this incident, that gap allowed contamination to propagate across four batches before any signal was recognised.

## Detection Architecture

The diagram below shows where the contamination entered the system and where detection occurred. The blast radius was not determined by the severity of the failure. It was determined by how long the detection gap allowed it to run. Detection latency was a system design problem.

<img src="/operations-portfolio/images/seekers/juniper-detection-architecture.svg" alt="Detection architecture diagram" style="width:100%; height:auto; display:block;">

---

*Back to [Juniper Contamination Investigation]({{< ref "/seekers/juniper-contamination/" >}})*
