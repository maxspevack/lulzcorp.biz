---
layout: default
title: Filings
description: All corporate filings issued by LulzCorp Holdings.
permalink: /filings/
---

<p class="eyebrow">PUBLIC RECORD</p>
<h1>Filings</h1>
<p class="dek">All corporate filings issued by LulzCorp Holdings, in reverse chronological order. Filings record real events, in the corporate-formal register, with appropriate dryness.</p>

{% if site.posts.size == 0 %}
<p><em>No filings have been issued. The Office of the Consigliere reports nothing further at this time.</em></p>
{% else %}
<ul class="filings-list">
  {% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}" class="filing-link">{{ post.title }}</a>
    <time datetime="{{ post.date | date_to_xmlschema }}">
      Filed {{ post.date | date: "%Y-%m-%d" }}
      {% if post.filing_number %} · No. {{ post.filing_number }}{% endif %}
    </time>
  </li>
  {% endfor %}
</ul>
{% endif %}

---

<p style="font-family: 'Courier Prime', monospace; font-size: 0.85em; color: var(--muted);"><em>To the Founder, sole shareholder: there is nothing further to report. — Office of the Consigliere</em></p>
