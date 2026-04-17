---
title: "Programme Overview"
---

<div class="inline-title">
  <a href="/red-lantern/" class="parent-title">Red Lantern Dining</a>
  <span class="title-slash">/</span>
  <span class="child-title">Programme Overview</span>
</div>

<div class="signals-2x2">
  <div class="signal-cell">
    <div class="signal-label">Lead time</div>
    <div class="signal-value-sm">7 → 3 weeks</div>
    <div class="signal-sub">Phase 1 reduction</div>
  </div>
  <div class="signal-cell">
    <div class="signal-label">Cost reduction</div>
    <div class="signal-value">29.80%</div>
    <div class="signal-sub">GLS raw material</div>
  </div>
  <div class="signal-cell">
    <div class="signal-label">Orders placed</div>
    <div class="signal-value">18</div>
    <div class="signal-sub">GLS ×10 · LYS ×8</div>
  </div>
  <div class="signal-cell">
    <div class="signal-label">Phase 1 duration</div>
    <div class="signal-value-sm">13 months</div>
    <div class="signal-sub">Mar 2024 – Apr 2025</div>
  </div>
</div>

## The Programme

Red Lantern Dining is a 14-site food and beverage franchise. No location had the space or equipment to produce drinks on site, so I built a centralised bottled RTD programme: drinks made externally to a fixed specification, bottled, and distributed to all locations from one warehouse. I owned the programme end to end, from recipe development and factory setup through to logistics, cost optimisation, and delivery.

Two drinks completed the full programme cycle: Ginger Lime Sparkling and Lychee Yuzu Soda. The programme moved through seven physical nodes, each dependent on the one before it. A delay or failure at any point reduced the time available to recover downstream and increased the chance of the problem propagating through the system.

## Supply Chain Structure

The supply chain  moved through seven nodes: client sign-off, production at Apex Beverage, bulk transfer, carbonation and bottling at Crest Bottling, return transport, labelling, and delivery to the client warehouse.

<div class="asset-container">
  <img src="/images/red-lantern/supply-chain.svg" alt="Supply chain structure — seven nodes from R&D sign-off to client warehouse">
</div>

## The Visibility Problem

The tracker was an Excel file I maintained and emailed to the production partners and Red Lantern Dining. State was only visible when I shared it, so between updates nobody else had a live view of what was happening at any node. When something ran late, visibility depended either on me updating the tracker or on the next node noticing it was still waiting. By then, the recovery window was already smaller and the delay had already started to move downstream.

The issue was not that signals did not exist. It was that they were seen too late. In this system, detection latency came from the way visibility had been set up.

## Pilot Before Rollout

Before scaling to all 14 locations, I ran production and delivery to a single franchise location to test the production and logistics flow and gather real sales feedback. Two drinks were cut because they did not sell. The two that remained had their recipes adjusted based on real sales and taste feedback before scaling.

Rollout then happened in stages rather than all at once: from 1 to 2 locations, then to 5, before full expansion. That kept the feedback loop active and the blast radius of unknowns small throughout the rollout.

## The Dashboard

The dashboard reconstructs the Phase 1 operating history for both drinks: 18 orders in total, with Ginger Lime Sparkling at 10 and Lychee Yuzu Soda at 8.

It shows COGS movement, supplier reliability, and five investigation queries designed to surface patterns not visible in the order-level view: hidden fragility, margin erosion, and future supply chain risk. OTIF (on time, in full) is the main delivery metric throughout. The dashboard is live on Vercel as a permanent, queryable record of Phase 1.

<a href="/red-lantern/dashboard/" class="ext-link">View Supply Chain Dashboard →</a>
