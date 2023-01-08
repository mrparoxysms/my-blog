---
date: 2022-09-01 1:00:00
title: Markata Blog Starter
published: True
tags:
  - home
  - meta

---

Hello. This is my blog. On it, I write things. From it, you and I will read things. Carry on.

## Pages tagged 'learn'

Below are pages that have been tagged 'learn'. These are notes I have written that are designed to help me learn.

{% for post in markata.map('post', sort='date', filter='post.get("published", False)==True and date<=today and "learn" in post.get("tags", [])', reverse=False) %}
!!! note "[{{ post['title'] }}]({{ post['slug'] }})"
    {{post['description']}}...
{% endfor %}

