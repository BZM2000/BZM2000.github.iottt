---
title: "新闻动态 | 张圆教授课题组 | 沈阳建筑大学"
layout: textlay
excerpt: "新闻动态 | 张圆教授课题组 | 沈阳建筑大学"
sitemap: false
permalink: /allnews.html
---

# 新闻动态

{% for article in site.data.news %}

<h3>{{ article.headline }}</h3>
<p><em>{{ article.date }}</em><br>
{{ article.text }}<br></p>
{% endfor %}
