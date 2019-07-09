---
title: APIs For Monitoring The Performance Of Your APIs
date: 2017-06-07 16:00:00 Z
tags:
- Monitoring
- Performance
- API Evangelist
image: https://s3.amazonaws.com/kinlane-productions/runscope/1-dashboard-test-performance.png
---

<p><a href="https://blog.runscope.com/posts/monitoring-api-performance-new-api-metrics-endpoint"><img src="https://s3.amazonaws.com/kinlane-productions/runscope/1-dashboard-test-performance.png" align="right" width="40%" style="padding: 15px;" /></a></p>[I am a big fan of API providers who also have APIs](http://apievangelist.com/2015/12/15/easier-to-offer-ops-apis-to-your-devs-if-your-api-service-provider-has-apis/). It may sound silly to say, but you would be surprised how many companies are selling services to API providers and do not actually have an API themselves. So, anytime I find a good example of API service providers launching new APIs that help API providers be more successful, I'm all over it with a story.

[Today's example is from my friends over at Runscope with their API Metrics API](https://www.runscope.com/docs/api/metrics) that lets you "retrieve your API tests performance metrics for each individual test, keep a pulse on your API's performance over time, and create custom internal or external dashboards with it". You can filter the request by using 3 different parameters:

* region - The service region you're using to run your tests (e.g. us1, us2, eu1, etc.)
* timeframe - Hour, day, week, or month. Depending on the timeframe you use, the interval between the response times will be different.
* environment_uuid - Filter by a specific environment, such as test, production, etc.

That is a pretty healthy example of everything that is API for me--an API that helps you make sure your APIs are performing as expected. You can not just understand how well your API responds, you can dial that in by region, and paint a clear picture of how well you are doing over time. I like that you can create internal dashboards for communicating this with your organization, but I also like their approach to providing external API performance dashboards so much I am going to add it to my list of building blocks I track on as part of [my API performance research](http://performance.apievangelist.com/#BuildingBlocks).

Aight. That concludes today's showcase of an API service provider making sure they are practicing what they preach and providing APIs for their valuable services. Honestly, I find this to be a fascinating layer of the API sector--the API layer that can orchestrate APIs. I enjoy thinking about what is possible when your APIs have APIs--it makes something like API performance a much more obtainable, scalable, and as Runscope does it, something you can easily communicate with your internal stakeholders and your API community.