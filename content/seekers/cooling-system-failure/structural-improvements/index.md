---
title: "Structural Improvements"
---

<div class="inline-title">
  <a href="/seekers/cooling-system-failure/" class="parent-title">Cooling System Failure</a>
  <span class="title-slash">/</span>
  <span class="child-title">Structural Improvements</span>
</div>

<nav class="subpage-nav">
  <a href="/seekers/cooling-system-failure/systems-context/" class="snav-item">Systems Context</a>
  <a href="/seekers/cooling-system-failure/discovery-timeline/" class="snav-item">Discovery Timeline</a>
  <a href="/seekers/cooling-system-failure/root-cause-analysis/" class="snav-item">Root Cause Analysis</a>
  <a href="/seekers/cooling-system-failure/impact-and-response/" class="snav-item">Impact and Response</a>
  <a href="/seekers/cooling-system-failure/structural-improvements/" class="snav-item active">Structural Improvements</a>
</nav>

Four changes followed the incident. Each was designed to close a specific failure mode exposed by the investigation.

## Detection

<div class="amber-item">
  <div class="amber-item-label">Change 1</div>
  <div class="amber-item-title">Coolant reservoir temperature instrumented and monitored</div>
  <div class="amber-item-body">A <span class="stat">50°C</span> threshold is now used for coolant reservoir temperature across all batches. It was set from the highest recorded temperature on the 300L still, which consistently produces spirit that passes quality control. Above that level, cooling becomes less effective and product quality begins to drop. Any breach now triggers immediate investigation while the batch is still active, including checking reservoir temperature and confirming the chiller is operating as expected.</div>
</div>

---

## Decision Constraints

<div class="amber-item">
  <div class="amber-item-label">Change 2</div>
  <div class="amber-item-title">Hard stop on weak signals before raw material commitment</div>
  <div class="amber-item-body">Any weak signal, sensory or operational, is now enough to halt production before raw materials enter the still. Once added, the batch is committed and cannot be recovered. The stop is now a fixed rule, not a judgement call. This delays irreversible commitments until the issue is understood, while action is still possible.</div>
</div>

<div class="amber-item">
  <div class="amber-item-label">Change 3</div>
  <div class="amber-item-title">Explicit escalation trigger for threshold breaches</div>
  <div class="amber-item-body">One person still has authority to halt production, but the trigger for review is now fixed rather than decided in the moment. Any threshold breach requires a documented review before the run continues. When one person both sees the signal and makes the decision, weak signals are easier to dismiss. The documented review removes that reliance.</div>
</div>

---

## Execution Controls

<div class="amber-item">
  <div class="amber-item-label">Change 4</div>
  <div class="amber-item-title">SOP versioning with explicit update loop</div>
  <div class="amber-item-body">When a batch requires a workaround or exposes ambiguity, the SOP is updated before the next batch and the previous version is archived. During the incident, key assumptions, including the belief that visible condensation was a reliable quality signal, were being held in memory rather than written down. SOP versioning records these changes and reduces the risk of reverting to outdated practice.</div>
</div>
