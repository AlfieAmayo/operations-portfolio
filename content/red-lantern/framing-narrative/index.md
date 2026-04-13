---
title: "Programme Review"
---

## The Programme

Red Lantern Dining is a 14-site food and beverage franchise. No site had the equipment or space to produce drinks to order. I proposed a centralised bottled RTD programme: drinks made externally to a fixed spec, bottled, and distributed to all locations from one warehouse. I owned the programme end to end: recipe development, factory setup, logistics, cost optimisation, and delivery.

Two drinks completed the full programme cycle: Ginger Lime Sparkling and Lychee Yuzu Soda. Production moved through seven physical nodes. Each node depended on the last. A delay or failure at any point reduced the time available to recover downstream and increased the likelihood of failure propagating through the system.

## Supply Chain Structure

Production moved through seven nodes: client sign-off, production at Apex Beverage, bulk transfer, carbonation and bottling at Crest Bottling, return transport, labelling, and delivery to the client warehouse.

![Red Lantern Dining supply chain](/operations-portfolio/images/red-lantern/supply-chain.svg)

## The Visibility Problem

The tracker was an Excel file I maintained and sent by email to the production partners and Red Lantern Dining. The state was only visible when I shared it, so between updates nobody else had a live view of what was happening at any node. When something ran late, visibility depended on me updating the tracker or on the next node realising it was still waiting. By then, the recovery window was already smaller, and the delay had already started to propagate downstream.

The issue was not that signals did not exist. It was that the system surfaced them too late. In this system, detection latency is a design problem, not an operational one.

## The Agile Reasoning

I applied Agile reasoning without explicitly calling it that. Each phase had a defined output that had to be stable before the next phase committed resources. Before scaling to all 14 sites, I ran production and delivery to a single franchise location to validate the production and logistics flow and generate real sales feedback. Drinks that did not sell were cut. Only products with clear demand were scaled.

This single-location trial was the core feedback loop, keeping the blast radius of unknowns small before committing to full rollout.

## The Dashboard

The dashboard reconstructs the full order history across both drinks: 18 orders, with Ginger Lime Sparkling at 10 (GLS-001 to GLS-010) and Lychee Yuzu Soda at 8 (LYS-001 to LYS-008).

It covers COGS trajectory, supplier reliability, and five investigation queries. OTIF is the primary delivery metric throughout. The dashboard is deployed live on Vercel as a permanent, queryable record of the programme.


Back to [Red Lantern Dining]({{< ref "/red-lantern/" >}})
