---
layout: default
title: publications
permalink: /publications/
years: [2020, 2019, 2018, 2017, 2016, 2015]
---

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
