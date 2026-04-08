---
title: "Discovery Timeline"
---

## Before the Run

Two runs preceded batch 50. They shaped how I interpreted what happened next.

Batches 48 and 49 were both Orange Liqueur, each running for 7.5 hours and passing QC without issue. During those runs, I observed that the 2000L still ran hotter than the 300L legacy still, with distillate output temperature progressing from cool to warm to hot. The observation was tactile, not instrumented. I noted it and moved on because both batches passed QC and matched the expected flavour. That outcome became the baseline.

The Orange Liqueur runs ended before coolant temperature had drifted far enough to affect flavour, so they passed without exposing the failure mode. Nothing in those runs suggested there was a problem. When the same temperature progression appeared during batch 50, I treated it the same way. I had seen the same temperature progression twice without consequence, so I treated it as normal.

## The Run

Batch 50, Seekers Mekong Dry Gin, ran on 29 May 2023 for 12 hours.

The dashboard was checked during the run, but temperature was not treated as a variable that required action. No threshold was crossed, and no threshold had been defined, and the same temperature progression had already been observed during the Orange Liqueur runs, where it had no impact on quality. Instead, visible condensation was treated as confirmation that the system was operating correctly.

At the end of the run, the output felt unusually hot, and I noted a temperature of 61.8°C from the display. The reading was elevated, but its significance was not understood, so the batch was set to rest pending QC. That value is the only temperature record from the run.

![Coolant temperature divergence from baseline](/operations-portfolio/images/seekers/coolant-temperature-divergence.svg)

*Fig. 1.1: Coolant temperature progression — Batch 50 vs control (Batches 48, 49), showing early and continuous divergence from baseline.*

## Detection

On 12 June 2023, 14 days after production, I tasted batch 50 during routine QC.

The gin did not match the expected standard. I could taste a difference, but it was not yet confirmed, so I asked the production team to taste it independently. They confirmed the same issue, and the batch failed QC.

By 10:30 AM, batch 2 botanicals had been prepared but not yet added to the still. I locked the batch 50 tanks to prevent any downstream movement and halted preparation before that commitment was made. Customer exposure was still zero.

The 14-day gap between production and detection was not a process failure; QC ran on schedule. The failure was that there was no actionable signal during the run.

---

[Back to Cooling System Failure]({{< ref "/seekers/cooling-system-failure/" >}})
