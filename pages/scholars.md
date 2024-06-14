---
title: Scholars
layout: page
permalink: /scholars.html
---

## Scholars

{% for s in site.data.rlg1000-scholar-metadata %}
- [{{ s.title }}]({{ '/items/' | relative_url }}{{ s.objectid }}.html){% endfor %}