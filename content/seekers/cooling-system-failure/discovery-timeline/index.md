---
title: "Discovery Timeline"
---

<div class="inline-title">
  <a href="/seekers/cooling-system-failure/" class="parent-title">Cooling System Failure</a>
  <span class="title-slash">/</span>
  <span class="child-title">Discovery Timeline</span>
</div>

<nav class="subpage-nav">
  <a href="/seekers/cooling-system-failure/systems-context/" class="snav-item">Systems Context</a>
  <a href="/seekers/cooling-system-failure/discovery-timeline/" class="snav-item active">Discovery Timeline</a>
  <a href="/seekers/cooling-system-failure/root-cause-analysis/" class="snav-item">Root Cause Analysis</a>
  <a href="/seekers/cooling-system-failure/impact-and-response/" class="snav-item">Impact and Response</a>
  <a href="/seekers/cooling-system-failure/structural-improvements/" class="snav-item">Structural Improvements</a>
</nav>

## Before the Run

Two runs preceded Batch 50 and shaped how I interpreted the outcome. Batches 48 and 49 were both Orange Liqueur, each running for 7.5 hours and passed quality control (QC) without issue.

During those runs, I observed that the 2000L still ran hotter than the 300L legacy still, with distillate output temperature progressing from cool to warm to hot. The observation was tactile, not instrumented. I noted it but did not return to review it because both batches passed QC and matched the expected flavour.

Those two runs became the reference point for how I interpreted Batch 50. Because the same pattern had already appeared without any quality issue, I treated it as normal.

## The Run

Batch 50, Seekers Mekong Dry Gin, ran on 29 May 2023 for 12 hours.

The dashboard was checked during the run, but the elevated temperature was not treated as actionable. No threshold had been defined, and a similar pattern had already been seen on the Orange Liqueur runs, where it had not affected quality. Visible condensation was treated as confirmation that the system was operating correctly.

At the end of the run, the distillate felt unusually hot, and I noted a dashboard reading of 61.8°C. The reading was elevated, but its significance was not understood, so the batch was left to rest pending quality control. It remains the only retained temperature reading from the run.

## Temperature Reconstruction

Post-incident reconstruction showed that Batch 50 diverged from the control runs early and continuously, even before the final threshold crossing.

<div class="asset-container">
  <img src="/images/seekers/coolant-temperature-divergence.svg" alt="Coolant temperature divergence chart">
</div>
<div class="asset-caption">Fig. 1.1: Coolant temperature progression — Batch 50 vs control (Batches 48, 49), showing early and continuous divergence from baseline. All data reconstructed post-incident.</div>

## Detection

On 12 June 2023, fourteen days after production, I tasted Batch 50 during routine QC. The gin did not match the expected standard. I asked the production team to taste it independently, and they confirmed the same issue. The batch failed QC.

By 10:30 AM, botanicals for Batch 51 had been prepared but not yet added to the still. I locked the Batch 50 tanks and halted preparation before the next run began. That contained the issue to a single batch and kept customer exposure at zero.

<div class="finding-callout">
  <div class="finding-label">Finding</div>
  <div class="finding-text">The 14-day gap between production and detection was not a process failure. QC ran on schedule. The failure was that there was no actionable signal during the run.</div>
</div>
