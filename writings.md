---
layout: default
title: Writings
---

{% assign grouped = site.writings | group_by_exp:"post","post.date | date: '%Y'" %}

{% for year in grouped %}
## {{ year.name }}

{% for post in year.items %}
- <a href="{{ post.url }}">{{ post.title }}</a>
  <div class="tags">
  {% for tag in post.tags %}
    <a class="tag" href="/tags/{{ tag }}">#{{ tag }}</a>
  {% endfor %}
  </div>
{% endfor %}

{% endfor %}
