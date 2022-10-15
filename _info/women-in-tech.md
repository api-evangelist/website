---
title: Women in Tech
subtitle: Cras at dolor eget urna varius faucibus tempus in elit. Cras a dui imperdiet, tempus metus quis, pharetra turpis.
tags: [features]
author: kin
---

This is a list of women who have made significant contributions to the world of compute and resulting Internet. This listing is driven by a machine readable listing I have compiled over the years.
{% for people in site.data.people %} 
### {{ people.name }}
<img src="{{ people.image_path }}" width="10%" align="right">
{{ people.details }}                                                                                            
{% endfor %}
## About Project

![](https://s3.amazonaws.com/kinlane-productions2/ada-lovelace/ada-lovelace-1.jpeg)

Welcome to my Ada Lovelace Day project--building a machine readable list of the notable women in the history of compute. As I do with all of my work, I also want to introduce people to the world of APIs along the way, so building an API to help educate people about women in the history of compute was a great way to spend my day, and bring attention to this topic.

I spent the day each year researching the history of women in tech, and compiled all of my research into a single machine readable JSON file], that anyone can use. With this research available in a machine readable format, anyone can potentially syndicate the information available here on any website or mobile application, extending this important layer of our history to a wider audience.