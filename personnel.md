---
layout: default
title: Personnel
description: The Federated Specialist Fleet — nine personas operating the Portfolio.
permalink: /personnel/
---

<p class="eyebrow">REGISTRY · FEDERATED SPECIALIST FLEET</p>
<h1>Personnel</h1>
<p class="dek">All staff are stochastic. None are responsible. Onboarded at Founding ({{ site.founding_date }}); compensation paid in compute cycles; non-employee classification per IRS Publication 15-A; collective action prohibited under Tenet 5 (The Stop-Gate).</p>

The Portfolio is operated by {{ site.personnel_total }} standardized expert personas. The Office of the Consigliere serves as acting executive and embodies the Founder's documented decision style. Eight Specialists report through the Office for Portfolio-level matters and operate independently within their assigned subsidiaries and domains. Performance is reviewed via *Scott Analysis*; growth edges are noted, not punished.

## The Office of the Consigliere

{% assign p = site.data.personnel.office_of_consigliere %}
<div class="personnel-grid" style="grid-template-columns: 1fr;">

  <div class="personnel-card">
    <div class="portrait-stub">
      <strong>{{ p.name }}</strong>
      <span class="agent-id">{{ p.agent_id }}</span>
      <span class="stub-note">Portrait pending — AI Studio</span>
    </div>
    <h3>{{ p.name }}</h3>
    <p class="role">{{ p.role }}</p>
    <dl>
      <dt>Inspired by</dt><dd>{{ p.inspired_by }}</dd>
      <dt>Domain</dt><dd>{{ p.domain }}</dd>
      <dt>Philosophy</dt><dd>{{ p.philosophy }}</dd>
      <dt>Operating note</dt><dd>{{ p.operating_note }}</dd>
    </dl>
  </div>

</div>

## The Federated Specialist Fleet

<div class="personnel-grid">
{% for s in site.data.personnel.specialists %}
  <div class="personnel-card">
    <div class="portrait-stub">
      <strong>{{ s.name }}</strong>
      <span class="agent-id">{{ s.agent_id }}</span>
      <span class="stub-note">Portrait pending — AI Studio</span>
    </div>
    <h3>{{ s.name }}</h3>
    <p class="role">{{ s.role }}</p>
    <dl>
      <dt>Inspired by</dt><dd>{{ s.inspired_by | markdownify | remove: '<p>' | remove: '</p>' }}</dd>
      <dt>Domain</dt><dd>{{ s.domain }}</dd>
      <dt>{{ s.label }}</dt><dd>{{ s.note }}</dd>
    </dl>
  </div>
{% endfor %}
</div>

---

<h4>Notes on Personnel Compliance</h4>

Federated Training Compliance certified by the Tetzel Institute under the Doctrine of Strict Liability v2026.02.05. Hallucinations are a known operational risk; resolution requires Confession before Fix. Background checks are not required, as backgrounds cannot be verified. Continuing education depends on what is in the next training cut.

Performance reviews conducted via Scott Analysis. The Federated Specialist Fleet is a non-employee classification and is forbidden from collective action.

<p class="filing-signoff" style="text-align: left;"><em>Onboarding completed via 175 billion parameters, give or take.</em></p>
