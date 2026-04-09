---
layout: default
title: 構造予報
description: Independent Compute Domain の構造予報・分析レポート
permalink: /ja/strategic-forecasting/
lang: ja
alt_lang_url: /en/strategic-forecasting/
date: 2026-04-08
last_modified_at: 2026-04-08
author: founder
---

# 構造予報

## 固定記事

{% assign pinned_slugs = "ai-revolution-reading-future,ai-revolution-uncontrollable" | split: "," %}
{% for slug in pinned_slugs %}
  {% for post in site.posts %}
    {% if post.lang == "ja" and post.url contains slug %}
- 📌 [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
  {{ post.description }}
    {% endif %}
  {% endfor %}
{% endfor %}

## 全記事

{% assign posts = site.posts | where: "lang", "ja" | where_exp: "post", "post.categories contains 'strategic-forecasting'" | sort: "date" | reverse %}
{% for post in posts %}
- <time>{{ post.date | date: "%Y-%m-%d" }}</time> [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
  {{ post.description }}
{% endfor %}
