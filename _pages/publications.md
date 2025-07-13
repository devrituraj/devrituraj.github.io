---
layout: page
permalink: /publications/
title: Publications
nav: Publications
years: [2021, 2020, 2019, 2018, 2017, 2016, 2015]
---
This page is not getting updated. Please visit the <a href="https://scholar.google.co.in/citations?hl=en&user=Wj8zIVUAAAAJ&view_op=list_works&sortby=pubdate" target="_blank">Google Scholar</a> profile.

<br/>
{% for y in page.years %}
  <div class="row m-0 p-0" style="border-top: 1px solid #ddd; flex-direction: row-reverse;">
    <div class="col-sm-1 mt-2 p-0 pr-1">
      <h3 class="bibliography-year">{{y}}</h3>
    </div>
    <div class="col-sm-11 p-0">
      {% bibliography -f papers -q @*[year={{y}}]* %}
    </div>
  </div>
{% endfor %}
