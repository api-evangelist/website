---
published: true
layout: post
title: >-
  Serverless, Like Microservices Is About Understanding Our Dependencies And
  Constraints
date: 2018-03-05T13:00:00.000Z
tags:
  - API Evangelist
  - Serverless
  - Deployment
  - Microservices
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/death-valley-national-park_dali_three_just_road.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/death-valley-national-park_dali_three_just_road.jpg" align="right" width="45%" style="padding: 15px;" /></p>I am not buying into all the hype around the recent serverless evolution in compute. However, like most trends I study, I am seeing some interesting aspects of how people are doing it, and some positive outcomes for teams who are doing it sensibly. I am not going all in on serverless when it comes to deploying or integrating with APIs, but I am using it for some projects, when it makes sense. I find AWS Lambda to be a great way to get in between the AWS API Gateway and backend resources, in order to conduct a little transformation. Keeping serverless as just one of many tools in my API deployment and integration toolbox, yet never going overboard with any single solution.

I put serverless into the same section of my toolbox as I do microservices. Serverless is all about decoupling how I deploy my APIs, helping me keep things doing small, meaningful things behind each of my API paths. Serverless forces me to think through how I am decoupling my backend, and pushes me to identify dependencies, acknowledge constraints, and get more creative in how I write code in this environment. To do one thing, and do it well, I need an intimate understanding of where my data and other backend resources are, and how I can distill a unit of compute down to the smallest unit as I possibly can. Identifying, reducing, and being honest about what my dependencies are is essential to serverless working or not working for me.

The challenge I'm having with serverless at the moment is that it can be easy to ignore many of the benefits I get from dependencies, while just assuming all dependencies are bad. Specifically around the frameworks I deploy as part of my API solutions. When coupled with AWS API Gateway this isn't much of a problem, but all by itself, AWS Lambda doesn't have all fo the other HTTP, transformation, header, request, and response goodness I enjoy from the API frameworks I've historically depend on. Showing me that understanding our dependencies is important, both good and bad. Not all dependencies are bad, as long as I am aware of them, have a knowledge of what they bring to the table, and it is a stable, healthy, and regularly evaluated relationships. This is a challenge I also come across regularly in microservices as well as serverless journeys, that we just throw things out for the sake of size, without thinking deeply about why we are doing something, and whether or not it is worth it.

I can see plenty of scenarios where I will be thinking that a serverless approach is good, but after careful evaluation of dependencies and constraints, I abandon this path as an option. I'm guessing we'll see a goldilocks style of serverless emerge that helps us find this sweet spot. Similar to what we are finding with the microservices evolution, in that micro isn't always about small--it is often just about finding the sweet spot between big and small, hot and cold, dependent and independent. Being sensible about how we use the tools in our API toolbox, and realizing most of these approaches are more about the journey, than they are about the actual tool.
