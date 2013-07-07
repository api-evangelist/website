---
layout: post
title: 'API Metrics and Analytics'
url: 'http://apievangelist.com2011/03/31/api-metrics-and-analytics/'
image: ''
---
{% include JB/setup %}
<img src="http://kinlane-productions.s3.amazonaws.com/google-analytics.png"  width="300" align="right" />I document a lot of the <a title="Common Building Blocks Used By API Providers" href="http://blog.apievangelist.com/2011/03/07/api-area-common-building-blocks/">common building blocks used by API providers</a>. These are common tools used across many industries and types of APIs to build their ecosystem.
I hesitate to ever say any of these common building blocks are essential, because every API potentially has different requirements.
However, one building block that is essential for every API, is metrics and analytics.
API owners should me measuring every aspect of their API and its community, and be constantly reassessing their strategy based upon what is going on in real-time.
API analytics is what service providers like <a title="Mashery" href="http://www.mashery.com">Mashery</a>, <a title="Apigee" href="http://www.apigee.com">Apigee</a> and <a href="http://www.3scale.net">3Scale</a> bring to the table. Mashery and Apigee proxy your API to deliver analytics, while 3Scale provides a plug to gather data for reporting on.
All three of these providers charge you per transaction for this service. <img src="http://kinlane-productions.s3.amazonaws.com/Google-Analytics-Charts-Stack.png"  width="150" align="right" /> To my knowledge there is no provider of an API analytics tool that is free, and plug and play.
With the current explosion of APIs being deployed, there is a huge opportunity for someone to provide a free API analytics service that gathers and measures API usage.
Think Google Analytics for APIs. A single line of server side code, with a variety of language kits, that will measure all requests on an API, its community, and provide a rich set of reports for API owners.
This could probably be done with the <a title="Google Analytics API" href="http://code.google.com/apis/analytics/docs/tracking/home.html">Google Analytics API</a>, I will have to play with more.
