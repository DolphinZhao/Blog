---
layout: page
title: About
description: 简单可依赖！
keywords: DolphinZhao, 大数据
comments: true
menu: 关于
permalink: /about/
---

学而不思则罔，思而不学则殆。

## 联系

{% for website in site.data.social %}
* {{ website.sitename }}：[@{{ website.name }}]({{ website.url }})
{% endfor %}

## Skill Keywords

{% for category in site.data.skills %}
### {{ category.name }}
<div class="btn-inline">
{% for keyword in category.keywords %}
<button class="btn btn-outline" type="button">{{ keyword }}</button>
{% endfor %}
</div>
{% endfor %}
