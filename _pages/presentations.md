---
layout: archive
title: "Presentations"
permalink: /presentations/
author_profile: true
---
1

{% for post in site.presentations reversed %}
  {% include archive-single.html %}
{% endfor %}
