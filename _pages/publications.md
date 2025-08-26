---
layout: page
permalink: /publications/
title: Publications
description: Publications by year
nav: true
nav_order: 2
---

{% include bib_search.liquid %}

## Latest on ADS
For the most up to date list, see all my publications on ADS
[here](https://ui.adsabs.harvard.edu/search/q=author%3A%22Rowland%2C%20Lucie%20E.%22%20&sort=date%20desc%2C%20bibcode%20desc&p_=0).

## First-author papers
<div class="publications">
  {% bibliography filter: '@*[author ^= "^Rowland"]' %}
</div>

## Co-author papers
<div class="publications">
  {% bibliography filter: '@*[author ^= "^(?!Rowland).*Rowland"]' %}
</div>
