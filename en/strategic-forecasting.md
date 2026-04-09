---
layout: default
title: Strategic Forecasting
description: Strategic forecasting reports and analyses from the Independent Compute Domain
permalink: /en/strategic-forecasting/
lang: en
alt_lang_url: /ja/strategic-forecasting/
date: 2026-04-08
last_modified_at: 2026-04-08
author: founder
---

# Strategic Forecasting

{% assign posts = site.posts | where: "lang", "en" | where_exp: "post", "post.categories contains 'strategic-forecasting'" | sort: "date" | reverse %}
{% for post in posts %}
- <time>{{ post.date | date: "%Y-%m-%d" }}</time> [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
  {{ post.description }}
{% endfor %}
