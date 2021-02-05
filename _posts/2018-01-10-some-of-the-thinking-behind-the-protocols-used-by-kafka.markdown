---
published: true
layout: post
title: Some Of The Thinking Behind The Protocols Used By Kafka
date: 2018-01-10T10:00:00.000Z
tags:
  - API Evangelist
  - Event-Architecture
  - Real Time
  - Messaging
  - Protocols
image: 'https://s3.amazonaws.com/kinlane-productions/kafka/kafka-protocol-guide.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/kafka/kafka-protocol-guide.png" align="right" width="45%" style="padding: 15px;" /></p>[I've been studying the overall Apache Stack a lot lately](http://apievangelist.com/2017/10/03/looking-at-the-37-apached-data-projects/), with an emphasis on [Kafka](https://kafka.apache.org/). I'm trying to understand what the future of APIs will hold, and where the leading edge of real time, event-driven architecture is at these days. I'm going through the protocol page for Kafka, learning about exactly how they move data around, and found their answers behind the decisions they've made along the way in deciding what protocols they chose to use were very interesting.

[All the way at the bottom of the Kafka protocol page you can find the following "Some Common Philosophical Questions"](https://kafka.apache.org/protocol), providing some interesting backstory on the decisions behind the very popular platform.

_Some people have asked why we don't use HTTP. There are a number of reasons, the best is that client implementors can make use of some of the more advanced TCP features--the ability to multiplex requests, the ability to simultaneously poll many connections, etc. We have also found HTTP libraries in many languages to be surprisingly shabby._

_Others have asked if maybe we shouldn't support many different protocols. Prior experience with this was that it makes it very hard to add and test new features if they have to be ported across many protocol implementations. Our feeling is that most users don't really see multiple protocols as a feature, they just want a good reliable client in the language of their choice._

_Another question is why we don't adopt XMPP, STOMP, AMQP or an existing protocol. The answer to this varies by protocol, but in general the problem is that the protocol does determine large parts of the implementation and we couldn't do what we are doing if we didn't have control over the protocol. Our belief is that it is possible to do better than existing messaging systems have in providing a truly distributed messaging system, and to do this we need to build something that works differently._

_A final question is why we don't use a system like Protocol Buffers or Thrift to define our request messages. These packages excel at helping you to managing lots and lots of serialized messages. However we have only a few messages. Support across languages is somewhat spotty (depending on the package). Finally the mapping between binary log format and wire protocol is something we manage somewhat carefully and this would not be possible with these systems. Finally we prefer the style of versioning APIs explicitly and checking this to inferring new values as nulls as it allows more nuanced control of compatibility._

It paints an interesting story about the team, technology, and I think the other directions the API sector is taking, when it comes to which protocols they are using. I don't know enough about how Kafka works to take any stance on their decisions. I'm just looking to just take a snapshot of their stance, so that I can come back to it at some point in the future, when I do.

[I published my diverse toolbox diagram a couple weeks back](http://apievangelist.com/2018/01/02/my-evolving-definition-of-a-robust-and-diverse-api-toolbox/), which includes Kafka. As I continue to develop my understanding of the Apache Stack, and Kafka, I will further dial-in the story that my API toolbox visual tells. The answers above further muddy the water for me about where it fits into the bigger picture, but I'm hoping it is something that will clear up with more awarness of what Kafka delivers.
