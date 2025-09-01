---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 2
---


For the most up to date list, see all my publications on ADS
[here](https://ui.adsabs.harvard.edu/search/q=author%3A%22Rowland%2C%20Lucie%20E.%22%20&sort=date%20desc%2C%20bibcode%20desc&p_=0).

{% include bib_search.liquid %}

## First-author papers
<div class="publications">
  {% bibliography --query @*[firstauthor=yes] %}
</div>

## Co-author papers
<div class="publications">
  {% bibliography --query @*[firstauthor!=yes] %}
</div>

