---
title: "Root Cause Analysis"
layout: single
---
<div class="inline-title">
  <a href="/operations-portfolio/seekers/juniper-contamination/" class="parent-title">Juniper Contamination</a>
  <span class="title-slash">/</span>
  <span class="child-title">Five Whys Analysis</span>
</div>

<nav class="subpage-nav">
  <a href="/operations-portfolio/seekers/juniper-contamination/systems-context/" class="snav-item">Systems Context</a>
  <a href="/operations-portfolio/seekers/juniper-contamination/discovery-timeline/" class="snav-item">Discovery Timeline</a>
  <a href="/operations-portfolio/seekers/juniper-contamination/root-cause-analysis/" class="snav-item active">Five Whys Analysis</a>
  <a href="/operations-portfolio/seekers/juniper-contamination/impact-and-response/" class="snav-item">Impact and Response</a>
  <a href="/operations-portfolio/seekers/juniper-contamination/structural-improvements/" class="snav-item">Structural Improvements</a>
</nav>

## Root Cause

The immediate cause was a contaminated juniper lot, PDI-JNP-220620, received from a Vietnam-based supplier on 20 June 2022. The more important failure was structural: there was no intake control capable of detecting it before it entered production.

The exact cause of the contamination was never confirmed. Sensory evidence pointed to either microbial activity or oxidative degradation during storage or transit, but no lab analysis was performed. The investigation confirmed the failure was upstream. The juniper arrived compromised. No error was identified in distillery handling, production, or quality control execution.

Lot PDI-JNP-220620 moved through intake, production, and four consecutive QC assessments before the deviation was caught. Detection depended on chance, not design.

## Five Whys

The Five Whys below trace how that detection failure was built into the process.

<div class="amber-item">
  <div class="amber-item-label">WHY 1</div>
  <div class="amber-item-title">Why did contaminated juniper pass quality control across four consecutive batches?</div>
  <div class="amber-item-body">The contamination was subtle. Each batch was assessed against a reference bottle selected at the time from available finished goods, rather than against a fixed baseline. Because the reference batch changed from one assessment to the next, small shifts across consecutive batches were harder to detect.</div>
</div>

<div class="amber-item">
  <div class="amber-item-label">WHY 2</div>
  <div class="amber-item-title">Why was each batch assessed against a changing reference batch rather than a fixed baseline?</div>
  <div class="amber-item-body">The quality control process did not require a fixed reference bottle, so the assessor could choose any reference bottle from finished goods at the time of assessment.</div>
</div>

<div class="amber-item">
  <div class="amber-item-label">WHY 3</div>
  <div class="amber-item-title">Why did the quality control process not require a fixed reference bottle?</div>
  <div class="amber-item-body">The process was built to judge whether a batch was acceptable, not to detect slow drift across batches caused by lot-to-lot ingredient variation. That risk was not part of the control design.</div>
</div>

<div class="amber-item">
  <div class="amber-item-label">WHY 4</div>
  <div class="amber-item-title">Why was ingredient variation not recognised as a risk?</div>
  <div class="amber-item-body">Supplier consistency was assumed rather than verified. Because the supplier had not caused a quality issue before, lot-to-lot variation was not treated as a failure mode. As a result, there was no intake check to test that assumption.</div>
</div>

<div class="amber-item">
  <div class="amber-item-label">WHY 5</div>
  <div class="amber-item-title">Why was there no intake check to test that assumption?</div>
  <div class="amber-item-body">Supplier selection was based on price and availability, not on demonstrated consistency. Because consistency was assumed rather than tested, no intake verification step was ever built into the process.</div>
</div>

## Structural Root Cause

<div class="finding-callout">
  <div class="finding-label">Finding</div>
  <div class="finding-text">Supplier quality and consistency were not treated as reliability requirements. The system relied on an assumption of consistency that was never tested, so no detection step was built into intake. Final QC became the only downstream point where problems could be found, and it was not designed to catch this type of failure.</div>
</div>
