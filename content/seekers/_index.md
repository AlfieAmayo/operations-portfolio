---
title: "Seekers Spirits"
layout: "single"
---
Seekers Spirits is a craft distillery I co-owned and operated in Phnom Penh, Cambodia. Both incidents documented here share the same structural problem: by the time a failure was detected, the system had no upstream mechanism to surface it. In the juniper contamination, a compromised ingredient lot passed through production undetected for 56 days, affecting 715 bottles. In the cooling failure, live sensor readings were display-only with no data retention, meaning the failure could only be reconstructed after the fact, not caught in real time. The postmortems below document what happened, how far they propagated, and what changed.

The investigations are backed by a PostgreSQL database built retrospectively from production records. The schema, data, and investigation queries are available on GitHub.

[View the database repository →](https://github.com/AlfieAmayo/seekers-db)

<hr>

[Juniper Contamination]({{< ref "/seekers/juniper-contamination/" >}})

[Cooling System Failure]({{< ref "/seekers/cooling-system-failure/" >}})
