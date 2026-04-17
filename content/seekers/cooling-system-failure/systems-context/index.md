---
title: "Systems Context"
---

<div class="inline-title">
  <a href="/seekers/cooling-system-failure/" class="parent-title">Cooling System Failure</a>
  <span class="title-slash">/</span>
  <span class="child-title">Systems Context</span>
</div>

<nav class="subpage-nav">
  <a href="/seekers/cooling-system-failure/systems-context/" class="snav-item active">Systems Context</a>
  <a href="/seekers/cooling-system-failure/discovery-timeline/" class="snav-item">Discovery Timeline</a>
  <a href="/seekers/cooling-system-failure/root-cause-analysis/" class="snav-item">Root Cause Analysis</a>
  <a href="/seekers/cooling-system-failure/impact-and-response/" class="snav-item">Impact and Response</a>
  <a href="/seekers/cooling-system-failure/structural-improvements/" class="snav-item">Structural Improvements</a>
</nav>

## Operations Overview

Seekers Spirits is a craft distillery in Phnom Penh, Cambodia. At the time of this incident, production ran on two stills: a 300L legacy still and a 2000L still installed in early 2023. The 300L still had a stable, established operating pattern. The 2000L still handled larger runs, but its cooling system depended on a reservoir originally sized for the smaller equipment. I owned quality control end-to-end, from tasting through to final release decisions.

## Still Configuration

The 2000L still used a main condenser and pre-cooler connected to a shared coolant reservoir. That reservoir had originally been designed for the smaller 300L still and was reused without modification. In Cambodia, ambient temperatures typically range from 28 to 35°C, which reduced cooling efficiency. During longer runs, heat entered the system faster than it could be removed.

This created a gradual rise in coolant temperature during long runs, with no mechanism to detect or record it.

## Observability Gaps

Two observability gaps defined both the failure and the investigation.

<div class="amber-item">
  <div class="amber-item-label">GAP 1</div>
  <div class="amber-item-title">Display-only sensors with no retention</div>
  <div class="amber-item-body">The 2000L still displayed liquid output temperature in real time, but nothing was written to storage. During Batch 50, the dashboard was not checked because visible condensation was taken as a sign that everything was working. The only recorded temperature was 61.8°C, noted after the run had already finished when the distillate felt unusually hot. By then, the batch was complete and the data had not been retained.</div>
</div>

<div class="amber-item">
  <div class="amber-item-label">GAP 2</div>
  <div class="amber-item-title">Coolant reservoir not measured during production</div>
  <div class="amber-item-body">Coolant reservoir temperature was never measured during production. The 1 to 2°C per hour drift that caused the failure was only identified later through post-incident testing. During Batch 50, there was no reservoir reading to monitor, no threshold to define, and no intervention point. The data did not exist.</div>
</div>

Together, these gaps meant there was no production-time record to analyse. The failure could not be observed as it developed and had to be reconstructed after the fact.

In practice, detection depended on someone checking the system during the run. During Batch 50, that did not happen.
