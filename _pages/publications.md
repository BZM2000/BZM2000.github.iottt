---
title: "发表成果 | 张圆教授课题组 | 沈阳建筑大学"
layout: gridlay
excerpt: "发表成果 | 张圆教授课题组 | 沈阳建筑大学"
sitemap: false
permalink: /publications/
---

# 文章列表

<style>
    .reverse-ol {
        list-style-type: none;
        counter-reset: item-counter;
    }
    .reverse-ol li {
        counter-increment: item-counter;
    }
    .reverse-ol li::before {
        content: counter(item-counter) " ";
        border: 2px solid black;
        border-radius: 50%;
        width: 1.5em;
        height: 1.5em;
        text-align: center;
        display: inline-block;
        margin-right: 10px;
    }
</style>

<ol class="reverse-ol">
{% for publi in site.data.publist reversed %}
    <li>
        {{ publi.title }} <br />
        <em><strong>{{ publi.journal }}</strong></em>, {{ publi.year }} <br />
        {{ publi.authors }} <br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
    </li>
{% endfor %}
</ol>
