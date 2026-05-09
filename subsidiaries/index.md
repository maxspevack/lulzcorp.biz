---
layout: default
title: Subsidiaries
description: The four operating subsidiaries of the Portfolio.
permalink: /subsidiaries/
---

<p class="eyebrow">OPERATING SUBSIDIARIES</p>
<h1>The Portfolio</h1>
<p class="dek">LulzCorp owns and operates {{ site.subsidiary_total }} subsidiaries. Each is real. Each operates with substantial autonomy under the relevant Specialist or Founder.</p>

{% for sub in site.data.subsidiaries %}
## [{{ sub.name }}]({{ sub.url | relative_url }})

**Domain focus**: {{ sub.domain_focus }}.
**Headcount**: {{ sub.headcount }}.
**Operating status**: {{ sub.status }}.
**Domain holdings**: {{ sub.domain_count }}.

{{ sub.short_summary }}

{% endfor %}

---

For domain-by-domain inventory, see the [Charter](/charter/#domain-holdings).
