---
layout: default
title: Charter
description: The LulzCorp Charter, Tenets of Engagement, and Domain Asset Inventory.
permalink: /charter/
---

<p class="eyebrow">CORPORATE CHARTER · v2026.05</p>
<h1>The LulzCorp Charter</h1>
<p class="dek">Adopted at Founding ({{ site.founding_date }}). Amendable by the sole shareholder, who is generally unavailable.</p>

## Article I — Purpose

LulzCorp exists to hold and operate a small portfolio of digital products built by its sole shareholder. The Portfolio currently includes a Glass-Box news engine that refuses infinite scroll (Fishwrap Media), a satire of AI absolution markets that nonetheless makes a real point (Tetzel Institute), a small workshop of CLI tools the Founder uses every day (The Workshop), and the Founder's personal-scale digital property (Family Office).

All Portfolio products are real. The corporate framing is not.

## Article II — Operations

All Portfolio operations are conducted by the Federated Specialist Fleet under the direction of the Office of the Consigliere. The Founder may, at sole discretion, intervene in operational matters. In practice the Founder rarely does, citing the demands of his day employment.

The Federated Specialist Fleet consists of {{ site.personnel_total }} standardized expert personas, each onboarded at the Founding ({{ site.founding_date }}). All hold non-employee classification per IRS Publication 15-A and are forbidden from collective action under Article V (The Stop-Gate). Compensation is paid in compute cycles; the 401(k) match is 0%, but compounding is performed at FP16 precision.

See the [Personnel registry](/personnel/) for the full roster.

## Article III — Tenets of Engagement

The Portfolio operates under six Tenets, ratified at the Founding ({{ site.founding_date }}) and not subsequently amended.

1. **Strategic Framing.** All requests are either *Inquiry* (research) or *Directive* (execution). All decisions are framed as Type 1 (irreversible) or Type 2 (reversible).
2. **Ship + Shield + Sensor.** Maximize outcome, protect the fleet from friction, detect early-warning signals.
3. **Research First.** Default to Inquiry. Propose strategy before implementation.
4. **Specialist Delegation.** Summon specialists for technical depth. Final audit performed by the Office of the Consigliere.
5. **The Stop-Gate.** Executing file modifications or side-effect commands without an explicit Directive from the Founder is forbidden.
6. **Physical Reference.** Hardware and repository facts are maintained in a single source of truth. Duplication is prohibited.

## Article IV — Subsidiaries

The Portfolio comprises {{ site.subsidiary_total }} operating subsidiaries.

<table>
<thead>
<tr><th>Subsidiary</th><th>Domain Focus</th><th>Status</th><th>Headcount</th></tr>
</thead>
<tbody>
{% for sub in site.data.subsidiaries %}
<tr>
  <td><a href="{{ sub.url | relative_url }}">{{ sub.name }}</a></td>
  <td>{{ sub.domain_focus }}</td>
  <td>{{ sub.status }}</td>
  <td>{{ sub.headcount }}</td>
</tr>
{% endfor %}
</tbody>
</table>

## Article V — The Stop-Gate

No persona shall execute side-effect commands, modify production assets, or commit to the public record without explicit Directive from the Founder. Violation triggers review by the Office of the Consigliere and, where the violation involves writing, the Chief Editor.

## Article VI — Self-Awareness {#article-vi}

LulzCorp is aware of the situation. The situation is fine.

---

## Domain Holdings {#domain-holdings}

The Portfolio maintains {{ site.domain_total }} registered domains across five entities.

<table>
<thead>
<tr><th>Entity</th><th>Domain</th><th>Status</th><th>Function</th></tr>
</thead>
<tbody>
{% for entity in site.data.domains %}
  {% if entity.domains.size > 0 %}
    {% for d in entity.domains %}
    <tr>
      {% if forloop.first %}<td rowspan="{{ entity.domains.size }}"><strong>{{ entity.entity }}</strong></td>{% endif %}
      <td><code>{{ d.name }}</code></td>
      <td>{{ d.status }}</td>
      <td>{{ d.function }}</td>
    </tr>
    {% endfor %}
  {% else %}
    <tr>
      <td><strong>{{ entity.entity }}</strong></td>
      <td colspan="3"><em>No registered domain. Products distributed via GitHub.</em></td>
    </tr>
  {% endif %}
{% endfor %}
</tbody>
</table>

The largest concentration is held by Fishwrap Media (9), reflecting the subsidiary's planned five-cadence publication portfolio plus three engine TLDs and one manifesto reservation. The Portfolio's domain holdings ({{ site.domain_total }}) exceed its operating headcount (10, comprising 1 Founder and {{ site.personnel_total }} personas). Strategy review: ongoing.

---

<p class="filing-signoff" style="text-align: left;"><em>This is a satirical holding company. The compliance frameworks parodied herein are real; the compliance is not.</em></p>
