---
title: "发表成果 | 张圆教授课题组 | 沈阳建筑大学"
layout: gridlay
excerpt: "发表成果 | 张圆教授课题组 | 沈阳建筑大学"
sitemap: false
permalink: /publications/
---

# 文章列表

U = 本科生; M = 硕士生; D = 博士生; 数字 = 入学年

{% for publi in site.data.publist %}
{{ forloop.index }}. {{ publi.title }}, <em><strong>{{ publi.journal }}</strong></em>, {{ publi.year }} <br />
{{ publi.authors }}
<br />
{% endfor %}
