---
title: "Structural Improvements"
layout: single
---

Two structural changes came out of this incident.

The first was incoming lot validation. Every new botanical lot is now tested at intake through single botanical distillation against the house baseline before it enters production. This moved detection upstream to the point where the ingredient could be rejected before entering production. Lots that match the baseline are approved for use. Lots that deviate are rejected.

The second was a change to the quality control process. Each batch is now compared against a fixed, documented reference batch. Before this, batches were compared against a reference bottle selected from available stock, so the comparison point changed over time. This allowed gradual flavour drift to pass unnoticed across multiple batches.

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

The query runs in seconds because batch_ingredients was modelled as a junction table linking stock receipts to batches at the lot level. That schema decision makes the blast radius immediately visible. Without it, the same question would have to be answered manually by cross-referencing stock receipts, batch logs, production records, and bottling records under time pressure, against paper records, with no guarantee of completeness.

---

## Schema

![Ingredient Traceability Schema](/operations-portfolio/images/seekers/seekers_traceability_chain_ERD.svg)

*PostgreSQL 16 schema supporting lot-level trace from supplier receipt to batch output.*

---

## Assumptions That Failed

I assumed ingredient quality at receipt was good enough and that batch-level quality control would catch any problem later. That assumption delayed detection and allowed a contaminated lot to propagate across four batches.

I also assumed that comparing batches against available stock was sufficient. In practice, this created a shifting standard, so small deviations could pass across consecutive batches without triggering a failed check.

---

[Back to Juniper Contamination]({{< ref "/seekers/juniper-contamination/" >}})
