---
layout: page
permalink: /publications/
title: Publications
class: pubs
---

{:.hidden}
# Publications

<!-- <input id="ft-search" type="search" placeholder="Search papers..." /> -->

{% assign pubyears = site.data.publications | group_by:"year" %}
{% for year in pubyears %}
## {{ year.name }}
{:#y{{ year.name }} .year}
{% for pub in year.items %}
  {% include publication.html pub=pub %}
{% endfor %}
{% endfor %}

