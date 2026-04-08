---
title: "Root Cause Analysis"
---

## Mechanism of Failure

The 2000L still was connected to a cooling reservoir designed for Mae, the 300L legacy still. Under sustained load, coolant returned to the reservoir faster than heat could be dissipated. Temperature increased at approximately 1 to 2°C per hour, rising from ~30°C to ~54°C over 12 hours.

As coolant temperature increased, the system became less effective at condensing vapour back into liquid, so more vapour passed through without being properly captured. Distillate output temperature rose, less of the intended flavour was retained, and the final profile no longer matched the expected standard. The temperature did not spike at a single point. It rose steadily across the full run.

The system behaved the same way in every batch. The difference was duration. During the 7.5-hour Orange Liqueur batches, temperature increased but stayed within a range that did not affect flavour. The gin batch ran for an additional 4.5 hours. That additional time allowed heat to accumulate to the point where the system failed.

## Failed Assumptions

The failure followed directly from system configuration and operating conditions. Three assumptions made it both likely and late to detect.


### Cooling performance was assumed to be independent of water temperature

The manufacturer asked detailed questions about the operating environment and recommended a pre-cooler for Cambodia's climate. That process reinforced the view that thermal constraints had been addressed.

What neither I nor the manufacturer modelled was that the pre-cooler depended on city water temperature. In European installations, this was typically around 20°C. In Cambodia, it was closer to 30 to 35°C. The pre-cooler was not treated as an input-dependent component. Its effectiveness was assumed rather than validated under local conditions.


### Short runs were treated as representative of sustained operation.

Two 7.5-hour Orange Liqueur runs showed the same temperature drift but passed quality control. I took that as a sign the drift was not affecting flavour. When the same temperature pattern appeared in the gin batch, I made the same assumption and expected the outcome to be unchanged. This was only true at shorter run times. At 7.5 hours, the temperature stayed within a range that did not affect flavour. The gin batch ran for 12 hours. Over that time, heat continued to build until it affected flavour.


### System scaling was treated as linear

The move from 300L to 2000L was treated as a scale increase, not a change in the system. In practice, the reservoir was sized for a 300L system and could not dissipate heat during sustained 2000L runs.

## Why the Root Cause Was Confirmed Late

The system was not tested under the conditions where the failure occurred. Test runs were shorter, carried out in lower ambient temperatures, and focused on whether the recipe and process worked as expected, not on how the system behaved over longer runs.

Coolant reservoir temperature was not measured during production, and no thresholds were set to indicate when cooling performance was degrading. The pre-cooler was treated as a fixed solution, and its dependence on water temperature was not measured or tested.

Root cause could not be confirmed during production because the conditions that caused the failure were not measured. It was identified later through controlled testing after shipment.

---

[Back to Cooling System Failure]({{< ref "/seekers/cooling-system-failure/" >}})
