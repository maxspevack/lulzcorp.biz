---
layout: default
title: The Portfolio
description: Holding company for the Spevack/Gemini ecosystem. Four operating subsidiaries; sixteen registered domains; nine personnel.
permalink: /
---

{% assign latest = site.posts | first %}
{% if latest %}
<section class="latest-filing">
  <p class="eyebrow">LATEST FILING</p>
  <a href="{{ latest.url | relative_url }}" class="latest-filing-title">{{ latest.title }}</a>
  <p class="latest-filing-excerpt">{{ latest.excerpt | strip_html | truncatewords: 40 }}</p>
  <p class="latest-filing-meta">
    Filed {{ latest.date | date: "%Y-%m-%d" }}
    {% if latest.filing_number %} · No. {{ latest.filing_number }}{% endif %}
  </p>
</section>
{% endif %}

## The Portfolio

LulzCorp holds and operates {{ site.subsidiary_total }} subsidiaries.

<div class="estate-grid">
{% for sub in site.data.subsidiaries %}
  <a href="{{ sub.url | relative_url }}" class="estate-card">
    <div class="seal-stub">{{ sub.card_label_html }}</div>
    <h3>{{ sub.name }}</h3>
    <p class="estate-tagline">{{ sub.tagline }}</p>
    <ul>
    {% for item in sub.card_items %}<li>{{ item }}</li>{% endfor %}
    </ul>
  </a>
{% endfor %}
</div>

## Governance

LulzCorp is managed via the [Tenets of Engagement](/charter/) (ratified {{ site.founding_date }}). Day-to-day operations are conducted by the [Federated Specialist Fleet](/personnel/) under the direction of the Office of the Consigliere. The Founder maintains a non-operational role.

The Portfolio currently holds **{{ site.domain_total }} registered domains** across five entities. See the [Charter](/charter/#domain-holdings) for the full inventory.

[About the Founder →](/about/)
