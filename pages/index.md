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

This blog was built using markata, and I am writing up these markdown files in yaml.

yaml is a markdown language designed for intuitive readibility based on indentation

markata is a static site generator built on python and designed for flexible alteration using not-python. I don't exactly know how to alter it without python yet, aside from changing the markdown files <thumbs_up>

{% for post in markata.map('post', sort='date', filter='post.get("published", False)==True and date<=today and "learn" in post.get("tags", [])', reverse=False) %}
!!! note "[{{ post['title'] }}]({{ post['slug'] }})"
    {{post['description']}}...
{% endfor %}

