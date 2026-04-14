---
title: "Programme Overview"
---

## The Programme

Red Lantern Dining is a 14-site food and beverage franchise. No location had the equipment or space to produce drinks to order. I proposed a centralised bottled RTD programme: drinks made externally to a fixed specification, bottled, and distributed to all locations from one warehouse. I owned the programme end to end, from recipe development and factory setup through to logistics, cost optimisation, and delivery.

Two drinks completed the full programme cycle: Ginger Lime Sparkling and Lychee Yuzu Soda. Production moved through seven physical nodes, each dependent on the one before it. A delay or failure at any point reduced the time available to recover downstream and increased the likelihood of failure propagating through the system.

## Supply Chain Structure

Production moved through seven nodes: client sign-off, production at Apex Beverage, bulk transfer, carbonation and bottling at Crest Bottling, return transport, labelling, and delivery to the client warehouse.

![Red Lantern Dining supply chain](/operations-portfolio/images/red-lantern/supply-chain.svg)

## The Visibility Problem

The tracker was an Excel file I maintained and sent by email to the production partners and Red Lantern Dining. State was only visible when I shared it, so between updates nobody else had a live view of what was happening at any node. When something ran late, visibility depended on me updating the tracker or on the next node noticing it was still waiting. By then, the recovery window was already smaller and the delay had already started to move downstream.

The issue was not that signals did not exist. The issue was that they were seen too late. In this system, detection latency came from the way visibility had been set up.

## Pilot Before Rollout

Before scaling to all 14 locations, I ran production and delivery to a single franchise location to test the production and logistics flow and get real sales feedback. Two drinks were cut because they did not sell. The two that remained had their recipes iterated based on real sales and taste feedback before scaling.

Rollout then happened in stages, not all at once: from 1 to 2 locations, then to 5, before full expansion. That kept the feedback loop active and kept the blast radius of unknowns small throughout the rollout.

## The Dashboard

The dashboard reconstructs the Phase 1 operating history for both drinks: 18 orders in total, with Ginger Lime Sparkling at 10 (GLS-001 to GLS-010) and Lychee Yuzu Soda at 8 (LYS-001 to LYS-008).

It shows COGS movement, supplier reliability, and five investigation queries. These queries are designed to surface patterns that are not visible in the order-level view: hidden fragility, margin erosion, and future supply chain risk. OTIF (on time, in full) is the main delivery metric throughout. The dashboard is live on Vercel as a permanent, queryable record of Phase 1.

[← Red Lantern Dining]({{< ref "/red-lantern/" >}})
