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

{% if article.image1 %}
<img src="{{ site.url }}{{ site.baseurl }}/images/newspic/{{ article.image1 }}" alt="News Image" style="width: 100%; height: auto;">
{% endif %}

{% if article.image2 %}
<img src="{{ site.url }}{{ site.baseurl }}/images/newspic/{{ article.image2 }}" alt="News Image" style="width: 100%; height: auto;">
{% endif %}

{% if article.image3 %}
<img src="{{ site.url }}{{ site.baseurl }}/images/newspic/{{ article.image3 }}" alt="News Image" style="width: 100%; height: auto;">
{% endif %}

{% if article.image4 %}
<img src="{{ site.url }}{{ site.baseurl }}/images/newspic/{{ article.image4 }}" alt="News Image" style="width: 100%; height: auto;">
{% endif %}

{% if article.image5 %}
<img src="{{ site.url }}{{ site.baseurl }}/images/newspic/{{ article.image5 }}" alt="News Image" style="width: 100%; height: auto;">
{% endif %}

{% if article.image6 %}
<img src="{{ site.url }}{{ site.baseurl }}/images/newspic/{{ article.image6 }}" alt="News Image" style="width: 100%; height: auto;">
{% endif %}

{% endfor %}
