---
published: true
layout: post
title: 'Relationship Between OpenAPI Path, Summary, Tags and AysncAPI Topics'
date: 2018-02-20T11:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - AsyncAPI
  - OpenAPI
  - Topics
  - Semantics
image: >-
  http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/23_160_800_500_0_max_0_-5_-1.jpg
---
<p><img src="http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/23_160_800_500_0_max_0_-5_-1.jpg" align="right" width="45%" style="padding: 15px;" /></p>I'm working my way through several hundred OpenAPI definitions that I have forked from [APIs.guru](https://apis.guru/), [Any API](https://any-api.com/), and have automagically generated from API documentation scrape scripts I have developed over time. Anytime I evolve a new OpenAPI definition, I first make sure the summary, description, and tags are as meaningful as they possibly can. Sadly this work is also constrained by how much time I have to spend with each API, as well as how well designed their API is in the first place. I have a number of APIs that help me enrich this automatically, by mining the API path, applying regular expressions, but often times it takes a manual review to add tags, polish summaries, and make the OpenAPI details as meaningful as I possibly can, in regards to what an API does.

As I'm taking a break from this work, I'm studying up on [AsyncAPI](https://www.asyncapi.com/), trying to get my head around how I can be crafting API definitions for the message-based, event-driven, streaming APIs I'm profiling alongside my regular API research. One of the areas the AsyncAPI team is pushing forward is around the concept of a topic--_"to create a definition that suites most use cases and establish the foundation for community tooling and better interoperability between products when using AsyncAPI."_ or to elaborate further, _"a topic is a string representing where an AsyncAPI can publish or subscribe. For the sake of comparison they are like URLs in a REST API."_ Now I'm thinking about the relationships between the API design elements I'm wrestling with in my API definitions, and how the path, summary, and tags reflect what Async is trying to articulate with their topics discussion.

**{organization}.{group}.{version}.{type}.{resources}.{event}**

- **organization** - the name of the organization or company.
- **group** - the service, team or department in charge of managing the message..
- **version** - the version of the message for the given service. This version number should remain the same unless changes in the messages are NOT backward compatible.
- **type** - the type of the message, e.g., is it a command or an event?. This value should always be event unless you're trying to explicitly execute a command in another service, i.e., when using RPC.
- **resources** - resources and sub-resources, in a word (or words) describing the resource the message refers to. For instance, if you're sending a message to notify a user has just signed up, the resource should be user. But, if you want to send a message to notify a user has just changed her full name, you could name it as user.full_name.
- **event** - an event or command name, in case message type is event, this should be a verb in past tense describing what happened to the resource, and in case message type is command, this should be a verb in infinitive form describing what operation you want to perform.

**Example(s):**

- hitch.accounts.1.event.user.signedup
- hitch.email.1.command.user.welcome.send

As I'm crafting OpenAPI definitions, and publishing them to Github, I'm using Jekyll to give me access to the large numbers of OpenAPI definitions I've published, and indexed using APIs.json, as Liquid objects. For each site. I can references APIs path using a dotted notation, such as site.twilio.send-sms-get. I haven't polished my naming conventions, and simply taking the path, stripping out everything but the alpha, numeric characters for the file names, but it got me thinking about how I might want to get more structured in how I name the individual units of compute I'm publishing using OpenAPI, and often times as Postman Collections. 

As I publish these API definitions to Github, as part of my API profiling for inclusion in the Streamdata.io API, I'm looking to establish a map of the surface area, that I can potentially turn into webhooks, streamings, and other approaches to real time message delivery. This is why I'm looking to understand AsyncAPI, to help quantify the result of this work. After I map out the surface area of the APIs, and quantify the topics at play, and obtain an API key, I need a way to then map out the real time streams of messages that will get passed around. To do this, I will need a way to turn each potential API response and its resulting request into a topic definition into a well defined, measurable input or output--AsyncAPI is going to help me do this.
