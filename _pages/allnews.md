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

{% if article.image %}
<img src="{{ site.url }}{{ site.baseurl }}/images/newspic/{{ article.image }}" alt="News Image" style="width: 100%; height: auto;">
{% endif %}

{% if article.image2 %}
<img src="{{ site.url }}{{ site.baseurl }}/images/newspic/{{ article.image2 }}" alt="News Image" style="width: 100%; height: auto;">
{% endif %}

{% endfor %}
