---
layout: page
width: xsmall
title: Reach Out
permalink: /contact/
---

You can contact me with any questions or comments using the channels below, but with along with each channel I would also like to offer you some advice to help you make sure your messages are received, and get the response you are looking for.

{% for guidance in site.data.contact %}
- [{{ guidance.name }}]({{ guidance.url }}) - {{ guidance.description }}
{% endfor %}

As a one person operation, I do my best to keep up with the channels listed above, but there are some weeks where I'm focused on research, coding, and writing, and may not always be available.

I appreciate your interest, and looking forward to talking more about APIs.

