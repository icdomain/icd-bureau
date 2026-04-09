---
layout: default
title: AI時代の情報リテラシー
description: AI時代における情報の見極め方・リテラシーに関するコンテンツ
permalink: /ja/information-discernment/
lang: ja
alt_lang_url: /en/information-discernment/
date: 2026-04-08
last_modified_at: 2026-04-08
author: founder
---

# AI時代の情報リテラシー

{% assign posts = site.posts | where: "lang", "ja" | where_exp: "post", "post.categories contains 'information-discernment'" | sort: "date" | reverse %}
{% for post in posts %}
- <time>{{ post.date | date: "%Y-%m-%d" }}</time> [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
  {{ post.description }}
{% endfor %}
