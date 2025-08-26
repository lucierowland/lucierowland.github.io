---
layout: page
permalink: /publications/
title: Publications
description: Publications
nav: true
nav_order: 2
---

## Latest on ADS
For the most up to date list, see all my publications on ADS
<a href="YOUR_ADS_URL" target="_blank" rel="noopener">here</a>.

## First-author papers
<div class="publications">
  {% bibliography --query '@*[firstauthor=yes]' %}
</div>

## Co-author papers
<div class="publications">
  {% bibliography --query '@*[firstauthor!=yes and author~="Rowland, Lucie"]' %}
</div>
