---
title: "Systems Context"
layout: "single"
---

<div class="inline-title">
  <a href="/seekers/juniper-contamination/" class="parent-title">Juniper Contamination</a>
  <span class="title-slash">/</span>
  <span class="child-title">Systems Context</span>
</div>

<nav class="subpage-nav">
  <a href="/seekers/juniper-contamination/systems-context/" class="snav-item active">Systems Context</a>
  <a href="/seekers/juniper-contamination/discovery-timeline/" class="snav-item">Discovery Timeline</a>
  <a href="/seekers/juniper-contamination/root-cause-analysis/" class="snav-item">Five Whys Analysis</a>
  <a href="/seekers/juniper-contamination/impact-and-response/" class="snav-item">Impact and Response</a>
  <a href="/seekers/juniper-contamination/structural-improvements/" class="snav-item">Structural Improvements</a>
</nav>

## Operations Overview

At the time of this incident, Seekers Spirits produced three core gin SKUs on a single 300L still: Seekers Mekong Dry Gin, Seekers Mekong Gold Gin, and Jason Kong Butterfly Pea Gin. Quality control (QC) was my responsibility end-to-end, from tasting through to final release decisions.

The production flow had no formal quality gates upstream of production and no automated monitoring between stages. Ingredients were received and visually inspected, batches were produced, and finished product was assessed at post-production QC before release. Any failure introduced at ingredient receipt had an unobstructed path through every stage before it could be caught.

## Ingredient Supply Chain

Juniper berries were sourced from a Vietnam-based supplier. Lot PDI-JNP-220620, 50kg, was received on 20 June 2022 and used across four consecutive batches between July and August 2022. The lot entered production without any formal intake check.

At the time, production and inventory records were held in spreadsheets. The database queries shown across these pages reproduce the investigation using a PostgreSQL schema built retrospectively for this portfolio.

## Observability Gaps

Three gaps in the system contributed to late detection.

<div class="amber-item">
  <div class="amber-item-label">GAP 1</div>
  <div class="amber-item-title">No defined standard for incoming ingredient quality</div>
  <div class="amber-item-body">Incoming lots were checked visually for obvious defects, but there were no pass or fail criteria for flavour, aroma, or other less visible quality issues. A contaminated lot could pass receipt and enter production without challenge.</div>
</div>
<div class="amber-item">
  <div class="amber-item-label">GAP 2</div>
  <div class="amber-item-title">No flavour baseline for incoming ingredients</div>
  <div class="amber-item-body">There was no reference point for how raw juniper should taste at receipt. Without a baseline, lot-to-lot variation could not be identified before entering production.</div>
</div>
<div class="amber-item">
  <div class="amber-item-label">GAP 3</div>
  <div class="amber-item-title">No fixed reference point or cross-batch comparison</div>
  <div class="amber-item-body">Each batch was compared against a bottle pulled from warehouse stock, so the reference point changed over time. That made it hard to spot gradual drift in flavour. In this incident, contamination moved through four batches before any signal was recognised. Without a fixed reference, there was nothing to measure the drift against.</div>
</div>

## Detection Architecture

The diagram below shows where contamination entered the system and where detection finally occurred.

<img src="/images/seekers/juniper-detection-architecture.svg" alt="Detection architecture diagram" style="width:100%; height:auto; display:block;">
