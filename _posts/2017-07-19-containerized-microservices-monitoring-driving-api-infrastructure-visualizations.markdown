---
published: true
layout: post
title: >-
  Containerized Microservices Monitoring Driving API Infrastructure
  Visualizations
date: 2017-07-19T09:00:00.000Z
tags:
  - API Evangelist
  - Monitoring
  - Microservices
  - Visualizations
  - Deployment
  - Containers
image: >-
  https://s3.amazonaws.com/kinlane-productions/netsil/1-P8w_-2-oCz0QfV6OENawJQ.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/netsil/1-P8w_-2-oCz0QfV6OENawJQ.png" align="right" width="40%" style="padding: 15px" /></p>While I track on what is going on with visualizations generated from data, I haven't seen much when it comes to API driven visualizations, or specifically visualization about API infrastructure, that is new and interesting. [This week I came across an interesting example in a post from Netsil about mapping microservices so that you can monitor them](https://blog.netsil.com/kubernetes-monitoring-needs-maps-6ef673d840c7). They are a pretty basic visualization of each database, API, and DNS element for your stack, but it does provide solid example of visualizing not just the deployment of database and API resources, but also DNS, and other protocols in your stack.

Netsil microservices visualization is focused on monitoring, but I can see this type of visualization also being applied to design, deployment, management, logging, testing, and any other stop along the API lifecycle. I can see API lifecycle visualization tooling like this becoming more common place, and play more of a role in making API infrastructure more observable. Visualizations are an important of the storytelling around API operations that moves things from just IT and dev team monitoring, making it more observable by all stakeholders.

I'm glad to see service providers moving the needle with helping visualize API infrastructure. I'd like to see more embeddable solutions deployed to Github emerge as part of API life cycle monitoring. I'd like to see what full life cycle solutions are possible when it comes to my partners like deployment visualizations from [Tyk](http://apis.how/zflfesymzk) and [Dreamfactory APIs](http://apis.how/bgdteovduo), and [management visualizations with 3Scale APIs](https://s3.amazonaws.com/kinlane-productions/partners/3scale-red-hat-logo.png), and monitoring and testing visualizations using [Runscope](http://apis.how/8nlsropidv). I'll play around with pulling data from these provides, and publishing to Github as YAML, which I can then easily make available as JSON or CSV for use in some basic visualizations.

If you think about it, thee really should be a wealth of open source dashboard visualizations that could be embedded on any public or private Github repository, for every API service provider out there. API providers should be able to easily map out their API infrastructure, using any of the API service providers they are using already using to operate their APIs. Think of some of the embeddable API status pages we see out there already, and what Netsil is offering for mapping out infrastructure, but something for ever stop along the API life cycle, helping deliver visualizations of API infrastructure no matter which stop you find yourself at.
