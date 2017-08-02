---
published: true
layout: post
title: Understanding Global API Performance At The Multi-Cloud Level
date: 2017-08-02T16:00:00.000Z
tags:
  - API Evangelist
  - Performance
  - Monitoring
image: >-
  https://s3.amazonaws.com/kinlane-productions/api-metrics/apimetrics-cloud-location-performance-map.png
---
[APIMetrics has a pretty addictive map showing the performance of API calls between multiple cloud providers, spanning many global regions](http://apimetrics.io/google-location-map/). The cloud location latency map "shows relative performance of a standard, reference GET request made to servers running on all the Google locations and via the Google global load balancer. Calls are made from AWS, Azure, IBM and Google clouds and data is stored for all steps of the API call process and the key percentiles under consideration."

<p><a href="http://apimetrics.io/google-location-map/"><img src="https://s3.amazonaws.com/kinlane-productions/api-metrics/apimetrics-cloud-location-performance-map.png" align="center" width="80%" style="padding: 15px;" /></a></p>

It is interesting to play with the destination of the API calls, changing the region, and visualizing how API calls begin to degrade to different regions. It really sets the stage for how we should start thinking about the deployment, monitoring, and testing of our APIs. Region, by region, getting to know where our consumers are, and making sure APIs are deployed within the cloud infrastructure that delivers the best possible performance. It's not just testing your APIs in a single location from many locations, it is also rethinking where your APIs are deployed, leveraging a multi-cloud reality and using all the top cloud provider, while also making API deployment by region a priority.

I'm a big fan of what APIMetrics is doing with the API performance visualizations and mapping. However, I think their approach to using HTTPbin is a significant part of this approach to monitoring and visualizing API performance at the multi-cloud level, while also making much of the process and data behind it all public. I want to put some more thought into how they are using HTTPbin behind this approach to multi-cloud API performance monitoring. I feel like there is potential her for applying this beyond just API performance, and think about other testing, security, and critical aspects of reliability and doing business online with APIs today.

After thinking where else this HTTPbin approach to data gathering could be applied, I want to think more about how the data behind APIMetrics cloud location latency map can be injected into other conversations, when it comes where we are deploying APIs, and running our API tests. Eventually I would like to see this type of multi-cloud API performance data alongside data for security and privacy compliance data, and even the regulations of each country as they apply to specific industries. Think about a time when we can deploy our APIs exactly where we want them based upon performance, privacy, security, regulations, and other critical aspects of doing business in the Internet age.
