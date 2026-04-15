---
title: "Supply Chain Dashboard"
---

Red Lantern Dining operated a franchise network of 14 sites. I ran a centralised RTD beverage programme for two drinks: Ginger Lime Sparkling and Lychee Yuzu Soda. Across 18 orders, the programme reduced raw material cost for Ginger Lime Sparkling by 29.80% and cut lead time from seven weeks to three.

The data covers Apex Beverage (Factory A), Crest Bottling (Factory B), and seven suppliers. All figures are real. Client and supplier names are fictionalised.

In the early phase, I used a shared Excel file to coordinate across all production nodes while the programme was still being built and stabilised. Partners updated their sections directly where possible, but when something ran late, I often had to chase the relevant supplier and update the tracker myself. As a result, issues sometimes only became visible downstream before I could act on them.

This dashboard reconstructs that programme in a way the Excel tracker could not. OTIF (on time, in full) is the primary delivery metric. COGs is shown order by order, with each inflection point tied to a specific decision. Supplier performance is broken down by where the failure occurred, not just shown as an overall score. The dashboard makes the tradeoffs between cost, reliability, and supplier choice explicit.

## Query Panel

The dashboard includes a query panel built around five operational questions. I built it to show patterns that are not visible order by order: which interventions worked, where the programme was still fragile, and where reliability was chosen over margin. Without that layer, the decisions that shaped Phase 1 stay buried in the order history. With it, they can be carried into later phases. The questions are:

- What changed, and did it actually work?
- Which deliveries succeeded by absorbing a problem, not solving it?
- Where was reliability chosen over margin?
- What does normal look like right now?
- What should be done before the next order goes in?

[Open the live dashboard →](https://kk-dashboard-wine.vercel.app)

[← Red Lantern Dining]({{< ref "/red-lantern/" >}})
