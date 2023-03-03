---
title: "发表成果 | 张圆教授课题组"
layout: gridlay
excerpt: "发表成果 | 张圆教授课题组"
sitemap: false
permalink: /publications/
---

{% for publi in site.data.publist %}

{{ publi.title }} <br />
<strong>{{ publi.journal }} <br />
<em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
