---
title: "组内动态 | 张圆教授课题组 | 沈阳建筑大学"
layout: textlay
excerpt: "组内动态 | 张圆教授课题组 | 沈阳建筑大学"
sitemap: false
permalink: /allnews.html
---

# 组内动态

{% for article in site.data.news %}

<p>{{ article.date }} <br>
<em>{{ article.headline }}</em><br>
{{ article.text }}</p>
{% endfor %}
