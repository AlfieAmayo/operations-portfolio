---
title: "Seekers Spirits"
layout: "single"
---
<p class="location-stamp">PHNOM PENH, CAMBODIA</p>
<h1 class="page-title">Seekers Spirits</h1>

<p>Seekers Spirits is a craft distillery I helped build, operate, and grow in Phnom Penh, Cambodia.</p>

<p>The two incidents documented here shared the same underlying problem: by the time failure was detected, the system had no way to catch it earlier.</p>

<p>The postmortems below show what happened, how each incident spread, and what changed.</p>

<div class="incident-grid">
  <a href="/seekers/juniper-contamination/" class="incident-row">
    <div class="incident-content">
      <div class="incident-num">/0.1</div>
      <div class="incident-title">Juniper Contamination</div>
      <div class="incident-desc">A compromised botanical lot moved through four consecutive batches undetected for 56 days. Detection was accidental. 715 bottles quarantined.</div>
    </div>
    <div class="incident-meta">
      <div class="meta-chip">lag <span class="meta-val">56 days</span></div>
      <div class="meta-chip">radius <span class="meta-val">715 bottles</span></div>
      <div class="meta-chip">batches <span class="meta-val">19–22</span></div>
    </div>
  </a>
  <a href="/seekers/cooling-system-failure/" class="incident-row">
    <div class="incident-content">
      <div class="incident-num">/0.2</div>
      <div class="incident-title">Cooling System Failure</div>
      <div class="incident-desc">Thermal drift of 1–2°C per hour developed across a 12-hour run. Display-only sensors retained no data. The failure was reconstructed afterward from a single manual reading.</div>
    </div>
    <div class="incident-meta">
      <div class="meta-chip">drift <span class="meta-val">1–2°C/hr</span></div>
      <div class="meta-chip">retained <span class="meta-val">1 reading</span></div>
      <div class="meta-chip">batch <span class="meta-val">50</span></div>
    </div>
  </a>
</div>

<div class="db-note">
  <a href="https://github.com/AlfieAmayo/seekers-db" class="ext-link" target="_blank">GitHub →</a>  
  <span class="db-note-text">PostgreSQL database built retrospectively from production records.</span>
</div>
