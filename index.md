---
layout: default
title: Articles
---

{% assign articles = site.pages | where_exp: "p", "p.dir == '/posts/'" | sort: "path" | reverse %}
{% for p in articles %}- [{{ p.title }}]({{ p.url | relative_url }})
{% endfor %}
