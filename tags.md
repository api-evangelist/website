---
layout: page
title: Tags
permalink: /tags/
---
{% assign all_tags = "" %}
{% assign posts = site.posts %}
{% for post in posts %}
    {% for tag in post.tags %}        
        {% assign already = 0 %}
        {% if tag != empty %}
            {% if tag != '' %}
              {% assign tag = tag | append: "" %}
              {% assign all_tags = all_tags | append: "" %}
                all_tags: {{ all_tags }}   
                tag: {{ tag }}   

                {% if all_tags contains tag %}
                    {% assign already = 1 %}
                {% endif %}    

            {% endif %}           
        {% endif %}   
    {% endfor %}
{% endfor %}