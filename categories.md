---
layout: page
title: Categories
permalink: /tags/
---

{% assign all_tags = "" %}

{% assign posts = site.posts %}
{% for post in posts %}

    {{ post.title }}

    {% for tag in post.tags %}
        
        {% assign already = 0 %}

        {{ tag }}

    {% endfor %}

{% endfor %}
