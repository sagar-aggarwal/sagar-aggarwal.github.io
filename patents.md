---
layout: page
permalink: /patents/
title: Patents
class: pubs
---

{:.hidden}
# Publications


{% assign pubyears = site.data.patent | group_by:"year" %}
{% for year in pubyears %}
## {{ year.name }}
{:#y{{ year.name }} .year}
{% for pub in year.items %}
  {% include patent.html pub=pub %}
{% endfor %}
{% endfor %}

