---
title: "Structural Improvements"
layout: single
---
<div class="inline-title">
  <a href="/operations-portfolio/seekers/juniper-contamination/" class="parent-title">Juniper Contamination</a>
  <span class="title-slash">/</span>
  <span class="child-title">Structural Improvements</span>
</div>

<nav class="subpage-nav">
  <a href="/operations-portfolio/seekers/juniper-contamination/systems-context/" class="snav-item">Systems Context</a>
  <a href="/operations-portfolio/seekers/juniper-contamination/discovery-timeline/" class="snav-item">Discovery Timeline</a>
  <a href="/operations-portfolio/seekers/juniper-contamination/root-cause-analysis/" class="snav-item">Five Whys Analysis</a>
  <a href="/operations-portfolio/seekers/juniper-contamination/impact-and-response/" class="snav-item">Impact and Response</a>
  <a href="/operations-portfolio/seekers/juniper-contamination/structural-improvements/" class="snav-item active">Structural Improvements</a>
</nav>

Two structural changes came out of this incident. Each was designed to close a specific detection gap identified during the investigation.

<div class="amber-item">
  <div class="amber-item-label">Change 1</div>
  <div class="amber-item-title">Incoming lot validation introduced</div>
  <div class="amber-item-body">Every new botanical lot is now tested at intake through single botanical distillation against the house baseline before it enters production. This moved detection upstream to the point where the ingredient could be rejected before use. Lots that match the baseline are approved. Lots that deviate are rejected.</div>
</div>

<div class="amber-item">
  <div class="amber-item-label">Change 2</div>
  <div class="amber-item-title">Fixed reference batch introduced for quality control</div>
  <div class="amber-item-body">Each batch is now compared against a fixed, documented reference batch. Before this, batches were compared against a reference bottle selected from available stock, so the comparison point changed over time. This allowed gradual flavour drift to pass unnoticed across multiple batches.</div>
</div>

---

## Blast Radius Query

The query below traces lot PDI-JNP-220620 through the database from stock receipt to bottled output.

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

<div class="code-caption">Traces lot PDI-JNP-220620 from stock receipt through production to bottled output. Nine bottling runs. Four batches. Three products. 715 bottles quarantined.</div>

The query runs in seconds because batch_ingredients was modelled as a junction table linking stock receipts to batches at the lot level. That makes the blast radius immediately visible. Without it, the same question would have to be answered manually by cross-referencing stock receipts, batch logs, production records, and bottling records under time pressure, with no guarantee of completeness.

---

## Schema

<div class="asset-container">
  <img src="/operations-portfolio/images/seekers/seekers_traceability_chain_ERD.svg" alt="Seekers traceability chain ERD">
</div>
<div class="asset-caption">PostgreSQL 16 schema supporting lot-level trace from supplier receipt to batch output. <a href="/operations-portfolio/images/seekers/seekers_traceability_chain_ERD.svg" class="ext-link" target="_blank" rel="noopener">View full schema →</a></div>

---

## Assumptions That Failed

<div class="amber-item">
  <div class="amber-item-body">I assumed ingredient quality at receipt was good enough and that batch-level quality control would catch any problem later. That assumption delayed detection and allowed a contaminated lot to move across four batches.</div>
</div>

<div class="amber-item">
  <div class="amber-item-body">I also assumed that comparing batches against available stock was sufficient. In practice, this created a shifting standard, allowing small deviations to pass across consecutive batches without triggering a failed check.</div>
</div>
