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

## Pinned

{% assign pinned_slugs = "ai-revolution-reading-future,ai-revolution-uncontrollable" | split: "," %}
{% for slug in pinned_slugs %}
  {% for post in site.posts %}
    {% if post.lang == "en" and post.url contains slug %}
- 📌 [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
  {{ post.description }}
    {% endif %}
  {% endfor %}
{% endfor %}

## All posts

{% assign posts = site.posts | where: "lang", "en" | where_exp: "post", "post.categories contains 'strategic-forecasting'" | sort: "date" | reverse %}
{% for post in posts %}
- <time>{{ post.date | date: "%Y-%m-%d" }}</time> [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
  {{ post.description }}
{% endfor %}
