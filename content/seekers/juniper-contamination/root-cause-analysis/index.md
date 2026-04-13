---
title: "Root Cause Analysis"
layout: single
---
## Root Cause

The root cause was a contaminated juniper lot, PDI-JNP-220620, received from a Vietnam-based supplier on 20 June 2022. The specific nature of the contamination was not determined. The sensory signature pointed to either microbial activity or oxidative degradation during storage or transit. No lab analysis was conducted to distinguish between the two. The investigation confirmed that the failure was upstream. The juniper arrived compromised. No error was identified in distillery handling, production, or quality control (QC) execution.

The main failure was not the contamination itself, but the lack of detection at intake. PDI-JNP-220620 moved through intake, production, and QC across four batches before the deviation was caught. There was no mechanism to intercept it earlier. Detection depended on chance, not design.

## Five Whys

**1. Why did contaminated juniper pass QC across four consecutive batches?**

The contamination was subtle. Each batch was assessed against a reference bottle selected at the time from available finished goods, rather than against a fixed baseline. Because the reference batch changed from one assessment to the next, small shifts across consecutive batches were harder to detect.

**2. Why was each batch assessed against a changing reference batch rather than a fixed baseline?**

The quality control process did not require a fixed reference bottle, so the assessor could choose any reference bottle from finished goods at the time of assessment.

**3. Why did the quality control process not require a fixed reference bottle?**

The process was built to judge whether a batch was acceptable, not to detect slow drift across batches caused by lot-to-lot ingredient variation. That risk was not part of the control design.

**4. Why was ingredient variation not recognised as a risk?**

Supplier consistency was assumed rather than verified. Because the supplier had not caused a quality issue before, lot-to-lot variation was not treated as a failure mode. As a result, there was no intake check to test that assumption.

**5. Why was there no intake check to test that assumption?**

Supplier selection was based on price and availability. Quality and consistency were not formally assessed, and there was no requirement to verify them at intake or during the relationship. As a result, no detection step was built into the intake process.

## Structural Root Cause

Supplier quality and consistency were not treated as reliability requirements. The system relied on an assumption of consistency that was never tested, so no detection step was built into intake. Final QC became the only point where problems could be found, and it was not designed to catch this type of failure.

---

[← Back to Juniper Contamination]({{< ref "/seekers/juniper-contamination/" >}})
