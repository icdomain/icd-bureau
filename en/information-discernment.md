---
layout: default
title: Information Discernment in the Age of AI
description: Information literacy and discernment resources for the age of AI
permalink: /en/information-discernment/
lang: en
alt_lang_url: /ja/information-discernment/
date: 2026-04-08
last_modified_at: 2026-04-08
author: founder
---

# Information Discernment in the Age of AI

{% assign posts = site.posts | where: "lang", "en" | where_exp: "post", "post.categories contains 'information-discernment'" | sort: "date" | reverse %}
{% for post in posts %}
- <time>{{ post.date | date: "%Y-%m-%d" }}</time> [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
  {{ post.description }}
{% endfor %}
