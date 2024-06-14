---
title: Subjects
layout: page
permalink: /subjects.html
---
{% assign topics = site.data.rlg1000-subject-metadata | where_exp: 'i','i.parentid == nil' %}
## Topics

{% for s in topics %}
- [{{ s.title }}]({{ '/items/' | relative_url }}{{ s.objectid }}.html) {% assign children = site.data.rlg1000-subject-metadata | where_exp: 'i','i.parentid == s.objectid' %}{% for c in children %}
    - {{ c.title }}{% endfor %}
{% endfor %}
