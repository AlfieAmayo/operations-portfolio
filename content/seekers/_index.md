---
title: "Seekers Spirits"
layout: "single"
---
Seekers Spirits is a craft distillery I helped build, operate, and grow in Phnom Penh, Cambodia. Both incidents documented here share the same problem: by the time the failure was detected, the system had no way to catch it earlier. In the juniper contamination, a compromised ingredient lot moved through production undetected for 56 days, affecting 715 bottles. In the cooling failure, the system showed live readings during production but retained none of them, so the failure could only be reconstructed after the fact, not caught in real time. The postmortems below document what happened, how far each incident spread, and what changed.

The investigations are supported by a PostgreSQL database built retrospectively from production records. The schema, data, and investigation queries are available on GitHub.


[View the database repository →](https://github.com/AlfieAmayo/seekers-db)

<hr>

[Juniper Contamination]({{< ref "/seekers/juniper-contamination/" >}})

[Cooling System Failure]({{< ref "/seekers/cooling-system-failure/" >}})
