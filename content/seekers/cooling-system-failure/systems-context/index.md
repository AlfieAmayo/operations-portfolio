---
title: "Systems Context"
---

<div class="inline-title">
  <a href="/operations-portfolio/seekers/cooling-system-failure/" class="parent-title">Cooling System Failure</a>
  <span class="title-slash">/</span>
  <span class="child-title">Systems Context</span>
</div>

<nav class="subpage-nav">
  <a href="/operations-portfolio/seekers/cooling-system-failure/systems-context/" class="snav-item active">Systems Context</a>
  <a href="/operations-portfolio/seekers/cooling-system-failure/discovery-timeline/" class="snav-item">Discovery Timeline</a>
  <a href="/operations-portfolio/seekers/cooling-system-failure/root-cause-analysis/" class="snav-item">Root Cause Analysis</a>
  <a href="/operations-portfolio/seekers/cooling-system-failure/impact-and-response/" class="snav-item">Impact and Response</a>
  <a href="/operations-portfolio/seekers/cooling-system-failure/structural-improvements/" class="snav-item">Structural Improvements</a>
</nav>

## Operations Overview

Seekers Spirits is a craft distillery in Phnom Penh, Cambodia. At the time of this incident, production ran on two stills: a 300L legacy still and a 2000L still installed in early 2023. The 2000L still was the primary asset for larger runs. I owned quality control end to end, from tasting through to final release decisions.

## Still Configuration

The 2000L still was sourced from a European manufacturer and tested in Europe before shipping. Its cooling system was designed to condense vapour back into liquid during distillation. If coolant temperature increased, condensation became less effective and output quality declined.

The system consisted of a main condenser and a pre-cooler, both connected to a shared coolant reservoir. That reservoir had originally been designed for the smaller 300L legacy still and was reused without modification. In Cambodia, ambient temperatures typically range from 28 to 35°C. A pre-cooler had been added to offset this, but its effectiveness dropped as coolant temperature increased. During longer runs, heat entered the system faster than it could be removed.

This led to a gradual rise in coolant temperature during long runs, with no mechanism to detect or record it.

## Observability Gaps

Two gaps defined both the failure and the investigation.

<div class="amber-item">
  <div class="amber-item-label">GAP 1</div>
  <div class="amber-item-title">Display-only sensors with no retention</div>
  <div class="amber-item-body">The 2000L still had sensors measuring liquid output temperature, displayed in real time on a dashboard, but nothing was written to storage. During Batch 50, the dashboard was not checked, as visible condensation was taken as a sign that everything was working. The only recorded temperature for Batch 50 was 61.8°C, noted informally after the run had completed when the distillate felt unusually hot. By then, the batch had already finished. The data was not stored.</div>
</div>

<div class="amber-item">
  <div class="amber-item-label">GAP 2</div>
  <div class="amber-item-title">Coolant reservoir not measured during production</div>
  <div class="amber-item-body">Coolant reservoir temperature was never measured during any production run. The 1 to 2°C per hour drift that caused the failure was only identified after shipment, during post-incident testing. Across all 2000L runs, this accumulation was not visible in the system. There was no reservoir temperature reading to monitor, no threshold to define, and no point of intervention. The data did not exist during production.</div>
</div>

Together, these gaps meant there was no production time data to analyse. The failure could not be observed as it developed. It could only be reconstructed after the fact.

In practice, detection depended on someone checking the system during the run. During Batch 50, that did not happen.
