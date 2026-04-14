---
title: "Root Cause Analysis"
---

## Mechanism of Failure

The 2000L still was connected to a cooling reservoir designed for the 300L legacy still. Under sustained load, coolant returned to the reservoir faster than heat could be dissipated. Temperature increased at approximately 1 to 2°C per hour, rising from around 30°C to around 54°C over 12 hours.

As coolant temperature increased, the system became less effective at condensing vapour back into liquid. More vapour passed through without being properly captured. Distillate output temperature rose, less of the intended flavour was retained, and the final profile no longer matched the expected standard. The temperature did not spike at a single point. It rose steadily across the full run.

The system behaved the same way in every batch. The difference was duration. During the 7.5 hour Orange Liqueur batches, temperature increased but stayed within a range that did not affect flavour. The gin batch ran for an additional 4.5 hours. That extra time allowed heat to keep building across the run until it affected output quality.

## Failed Assumptions

The failure followed directly from the system configuration and the conditions it was run under. Three assumptions made it both likely to occur and late to detect.

**1. Cooling performance was assumed to be independent of water temperature**

The manufacturer asked detailed questions about the operating environment and recommended a pre-cooler for Cambodia’s climate. That reinforced the view that the thermal constraints had been addressed.

What neither I nor the manufacturer modelled was that the pre-cooler depended on city water temperature. In European installations, this was typically around 20°C. In Cambodia, it was closer to 30 to 35°C. The pre-cooler was not treated as an input-dependent component. Its effectiveness was assumed rather than validated under local conditions.

**2. Short runs were treated as representative of sustained operation**

The two 7.5-hour Orange Liqueur runs showed the same temperature drift and passed quality control. I took that as a sign that the system was operating normally. When the same pattern appeared in the gin batch, I expected the outcome to be the same. That held true at 7.5 hours, but the gin batch ran for 12. Over that time, heat continued to build until it affected flavour.

**3. System scaling was treated as linear**

The move from 300L to 2000L was treated as a scale increase, not a change in the system. In practice, the reservoir was sized for a 300L still and could not dissipate heat during sustained 2000L runs.

## Why the Root Cause Was Confirmed Late

The system was not tested under the conditions where the failure occurred. Test runs were shorter, took place in lower ambient temperatures, and were focused on whether the recipe and process worked as expected, not on how the system behaved over longer runs.

Coolant reservoir temperature was not measured during production, and no thresholds were set to show when cooling performance was degrading. The pre-cooler was treated as a fixed solution, and its dependence on water temperature was not validated under local conditions.

The root cause could only be confirmed later, through controlled testing after shipment, because the conditions that caused the failure were not measured during production.

---

[Back to Cooling System Failure]({{< ref "/seekers/cooling-system-failure/" >}})
