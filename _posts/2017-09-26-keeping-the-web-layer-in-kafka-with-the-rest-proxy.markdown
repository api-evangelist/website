---
published: true
layout: post
title: Keeping The Web API Layer In Kafka With A REST Proxy
date: 2017-09-26T15:00:00.000Z
tags:
  - API Evangelist
  - Messaging
  - Event Sourcing
  - Proxy
image: >-
  https://s3.amazonaws.com/kinlane-productions/confluent/confluent-kafka-platform.png
---
<p><a href="https://www.confluent.io/"><img src="https://s3.amazonaws.com/kinlane-productions/confluent/confluent-kafka-platform.png" align="right" width="40%" style="padding: 15px;" /></a></p>I'm slowly learning more about [Kafka](https://kafka.apache.org/), and the other messaging and data streaming solutions gaining traction in the API space. If you aren't on the Kafka train yet, "Kafka is used for building real-time data pipelines and streaming apps. It is horizontally scalable, fault-tolerant, wicked fast, and runs in production in thousands of companies." I'm still learning about how Kafka works, and with no real production experience, it is something that is taking time.

As part of my conversations on the subject, I was introduced to [Confluent](https://www.confluent.io/), a platform version of Kafka, which is the quickest way I have seen to get started with real-time data streams. As part of the Confluent offering I noticed they have a REST proxy, which you can find [the API documentation here](https://docs.confluent.io/current/kafka-rest/docs/api.html), and [the code for the Kafka REST proxy on Github](https://github.com/confluentinc/kafka-rest). According to the Github repo, "the Kafka REST Proxy provides a RESTful interface to a Kafka cluster. It makes it easy to produce and consume messages, view the state of the cluster, and perform administrative actions without using the native Kafka protocol or clients."

I've noticed that many of the other messaging and data streaming solutions out of Apache these days have diverted from using REST, which makes sense for speed, and scale, but when it comes to reaching a wider audience I can still see the need to have RESTful API. Delivering a kind of multi-speed solution that allows developers to pick their speed based upon their skills, awareness, and need. I'm feeling like the platform approach of Confluent, combined with a RESTful layer, will give them an advantage over other Kafa service providers, or just deploying the open source solution out of the box.

REST isn't always the most efficient, or scalable solution, but when it comes to reaching a wide audience of developers, and allowing consumers to get up and running quickly, REST is still a sensible approach. Honestly, I don't think it is just REST, it is also about leveraging the web. Not that everyone understand the web, but I think it is what a large number of developers have been exposed to, and have been building on in the last decade. I can see high volume API solutions in the future often having a native protocol and client, but also supporting REST, and gRPC to make their solutions more accessible, performant, scalable, and quickly adopted and integrated alongside existing infrastructure.
