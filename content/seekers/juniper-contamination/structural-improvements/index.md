---
title: "Structural Improvements"
layout: single
---

## Changes Introduced

Two structural changes came out of this incident.

The first was incoming lot validation. Every new botanical lot is tested at intake by distilling it on its own and comparing the result to the house baseline before it enters production. This ensures the ingredient tastes as expected before it is used in a full batch. Distillation isolates the flavour, making differences easier to detect. If the flavour is in line with the baseline, the lot is approved for use in recipes. If it deviates, it is rejected.

The second was a change to the quality control process. Each batch is now compared against a fixed, documented reference batch, a known good standard. Before this, batches were compared against a reference bottle selected from available stock, which meant each comparison used a different reference, allowing flavour to drift. A small, consistent change in flavour could move with it and pass unnoticed across multiple batches.

---

## Blast Radius Query

The query below traces lot PDI-JNP-220620 through the database: from stock receipt through production to bottled output.

```sql
SELECT sr.supplier_lot_reference, b.batch_id, b.batch_date,
       b.product_name, bo.sku, bo.bottles_filled
FROM stock_receipts sr
JOIN batch_ingredients bi ON sr.receipt_id = bi.receipt_id
JOIN batches b ON bi.batch_id = b.batch_id
JOIN batch_outputs bo ON b.batch_id = bo.batch_id
WHERE sr.supplier_lot_reference = 'PDI-JNP-220620'
ORDER BY b.batch_id, bo.sku;
```

<div style="overflow-x: auto;">

| supplier_lot_reference | batch_id | batch_date | product_name | sku | bottles_filled |
|---|---|---|---|---|---|
| PDI-JNP-220620 | 19 | 2022-07-11 | Seekers Mekong Gold Gin | SMGG200 | 60 |
| PDI-JNP-220620 | 19 | 2022-07-11 | Seekers Mekong Gold Gin | SMGG700 | 100 |
| PDI-JNP-220620 | 20 | 2022-07-18 | Seekers Mekong Dry Gin | SMDG200 | 55 |
| PDI-JNP-220620 | 20 | 2022-07-18 | Seekers Mekong Dry Gin | SMDG700 | 90 |
| PDI-JNP-220620 | 21 | 2022-07-25 | Jason Kong Butterfly Pea Gin | JKBG200 | 50 |
| PDI-JNP-220620 | 21 | 2022-07-25 | Jason Kong Butterfly Pea Gin | JKBG700 | 105 |
| PDI-JNP-220620 | 22 | 2022-08-08 | Seekers Mekong Dry Gin | SMDG050 | 100 |
| PDI-JNP-220620 | 22 | 2022-08-08 | Seekers Mekong Dry Gin | SMDG200 | 60 |
| PDI-JNP-220620 | 22 | 2022-08-08 | Seekers Mekong Dry Gin | SMDG700 | 95 |

</div>

Nine bottling runs. Four batches. Three products. 715 bottles quarantined.

The query runs in seconds because batch_ingredients was modelled as a junction table linking stock receipts to batches at the lot level. That schema decision makes the blast radius immediately visible. Without it, the same question requires manual cross-referencing of stock receipts, batch logs, production records, and bottling records. Under time pressure, against paper records, with no guarantee of completeness.

---

## Schema

![Ingredient Traceability Schema](/operations-portfolio/images/seekers/seekers_traceability_chain_ERD.svg)

*PostgreSQL 16 schema supporting lot-level trace from supplier receipt to batch output.*

---

## What I Would Do Differently

I assumed ingredient quality could be trusted at receipt and verified later through batch-level quality control. That assumption delayed detection, allowing a contaminated lot to enter production and propagate across four batches before it was identified.

I also assumed that comparing batches against available stock was sufficient. In practice, this created a shifting standard, allowing small deviations to persist and compound across consecutive batches without ever triggering a failed check.

---

[Back to Juniper Contamination]({{< ref "/seekers/juniper-contamination/" >}})
