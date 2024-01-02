---
title: "发表成果 | 张圆教授课题组 | 沈阳建筑大学"
layout: gridlay
excerpt: "发表成果 | 张圆教授课题组 | 沈阳建筑大学"
sitemap: false
permalink: /publications/
---

# 文章列表

{% assign counter = 0 %}
{% for publi in site.data.publist %}
  {% assign counter = counter | plus: 1 %}
  {{ counter }}. {{ publi.title }}, <em><strong>{{ publi.journal }}</strong></em>, {{ publi.year }} <br />
  {{ publi.authors }} <br />
  {% if publi.link.url %}
    <a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
  {% endif %}
  <br />
{% endfor %}
