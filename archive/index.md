---
layout: page
title: API Evangelist Archives
---

<p>Here is the complete list of everything I have written on API Evangelist since I started, back in 2010. If you want to browse by topic I recommend visiting each individual research area, and anything I've written on the topic should be there.</p>
{% for post in site.posts  %}

    {% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
    {% capture this_month %}{{ post.date | date: "%B" }}{% endcapture %}
    {% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %}
    {% capture next_month %}{{ post.previous.date | date: "%B" }}{% endcapture %}

    {% if forloop.first %}
    ## {{ this_month }} {{this_year}}
    {% endif %}

    - {{ post.date | date: '%e %B, %Y' }}

    {% if forloop.last %}
    {% else %}
        {% if this_year != next_year %}
        <h3 id="{{ next_year }}-{{ next_month }}-ref">{{ next_month }} {{next_year}}</h3>
        {% else %}
            {% if this_month != next_month %}
            <h3 id="{{ this_year }}-{{ next_month }}-ref">{{ next_month }} {{next_year}}</h3>
            {% endif %}
        {% endif %}

    {% endif %}

{% endfor %}
