---
title: "Systems Context"
---

## Operations Overview

Seekers Spirits is a craft distillery in Phnom Penh, Cambodia. At the time of this incident, production ran on two stills: a 300L legacy still and a 2000L still installed in early 2023. The 2000L still was the primary asset for larger runs. I owned quality control end to end, from tasting through to final release decisions.

## Still Configuration

The 2000L still was sourced from a European manufacturer and tested in Europe before shipping. Its cooling system was designed to turn vapour into liquid. If coolant temperature rises, the system becomes less effective at condensing vapour, and output quality degrades.

The system consisted of a main condenser and a pre-cooler, both connected to a shared coolant reservoir. The reservoir had originally been designed for the smaller 300L legacy still and was reused without modification. Cambodia ambient temperatures range from 28 to 35°C. The pre-cooler, added to offset this, became less effective as coolant temperature increased. Under sustained production load, heat entered the system faster than it could be removed.

This created gradual thermal drift during long runs, with no mechanism to detect it.

## Observability Gaps

Two gaps defined both the failure and the investigation.

**Gap 1: Display-only sensors with no retention.** The 2000L still had sensors measuring liquid output temperature, displayed in real time on a dashboard, but nothing was written to storage. During batch 50, the dashboard was not checked, as visible condensation was taken as a sign everything was working. The only recorded temperature for batch 50 is 61.8°C, noted informally after the run completed when the output felt unusually hot. By then, the batch had already finished. The data was not stored.

**Gap 2: Coolant reservoir not measured during production.** Coolant reservoir temperature was never measured during any production run. The 1 to 2°C per hour drift that caused the failure was only identified after shipment, during post-incident testing with the manufacturer. Across all 2000L runs, this accumulation was not visible in the system. There was no signal to monitor, no threshold to define, and no point of intervention. The data did not exist during production.

Together, these gaps meant there was no production-time data to analyse. The failure could not be observed as it developed. It could only be reconstructed after the fact.

In practice, detection came down to someone checking the system during the run. During batch 50, that did not happen.

---

[Back to Cooling System Failure]({{< ref "/seekers/cooling-system-failure/" >}})
