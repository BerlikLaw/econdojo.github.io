---
layout: page
permalink: /research/bayes/
title: Research
description: A growing collection of academic papers.
topics: [Bayesian Econometrics]
nav: false
---

<div class="publications">

{% for y in page.topics %}
  <h2 class="topic">{{y}}</h2>
  
  {% bibliography -f papers -q @*[topic={{y}}]* %}
{% endfor %}

</div>
