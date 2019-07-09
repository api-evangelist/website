---
published: true
layout: post
title: >-
  Developing a Microservice to Orchestrate Long Running Background Server-Sent
  Events
date: 2018-01-19T09:00:00.000Z
tags:
  - API Evangelist
  - Real Time
  - Event Architecture
  - Streaming
  - Jobs
  - Orchestration
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/68_174_800_500_0_max_0_-5_-1.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/68_174_800_500_0_max_0_-5_-1.jpg" align="right" width="45%" style="padding: 15px;" /></p>I am working to understand the value that [Streamdata.io](http://apis.how/streamdata) brings to the table, and one of the tools I am developing is a set of APIs to help me measure the difference in data received for normal API calls versus when they are proxied with Streamdata.io using Server-Sent Events (SSE) and JSON Patch. Creating an API to poll any 3rd party API I plug in is pretty easy and straightforward, but setting up a server setup to operate long running Server-Sent Events (SSE), managing for failure and keeping an eye on the results takes a little more consideration. Doing it browser side is easy, but server side removes the human aspect of the equation, which starts and stops the process.

This post is just meant to just outline what I'm looking to build, and act as a set of project requirements for what I'm going to develop--it isn't a guide to building it. This is just my way of working through my projects, while also getting content published on the blog ;-). I just need to work out the details of what I will need to run many different Server-Sent Events (SSE) jobs for long periods of time, or even continuously, and make sure nothing breaks, or at least minimize the breakages. Half of my project will be polling hundreds of APIs, while the other half of it will be proxy those same APIs, and making sure I'm receiving those updates continuously.

I will need some basic APIs to operate each event stream I want to operate:

- **Register** - Register a new API URL I wish to run ongoing stream on.
- **Start** - Kick off a new stream for any single API I'm tracking on.
- **Stop** - Stop a stream from running for any single API I have streaming.

Any API I deem worthy, and have successfully proxied with Streamdata.io will be registered, and operating as a long running background scripts via AWS EC2 instances I have deployed. This is the straightforward part of things. Next, I will need some APIs to monitor these long running scripts, to make sure they are doing what they should be doing.

- **Status** - Check the status of a long running script to make sure it is still running and doing what it is supposed to do.
- **Logs** - View the logs of an event that has been running to see each time it has executed, and what the request and response were.
- **Notify** - Adding a notification API to send a ping to either myself, or someone else response for a long running script to investigate further.

I'm think that set of APIs should give me what I need to run these long running jobs. Each API will be executing command scripts that run in the background on Linux instances. Then I'm going to need a similar set of services to asses the payload, cache, and real time status of each API, keeping in line with [my efforts to break down the value of real time APIs](http://apievangelist.com/2018/01/17/breaking-down-the-value-of-real-time-apis/).

- **Size** - A service that processes each partial API response in the bucket and calculates the size of the response. If nothing changed, there was no JSON Patch response.
- **Change** - A service that determines if a partial API response has changed from the previous response from 60 seconds before, identifying the frequency of change. If nothing changed, there was no JSON Patch response.

I have three goals with long running script microservice. 1) Monitor the real time dimensions of a variety of APIs over time. 2) Understand the efficiencies gained with caching and streaming over polling APIs, and 3) Potentially store the results on Amazon S3, which I will write about in a separate post. I will build an application for each of these purposes on top of these APIs, keeping the microservice doing one thing--processing long run scripts that receive Server-Sent Events (SSE) deliver via Streamdata.io proxies I've sent for APIs I've targeted.

Next, I am going to get to work programming this service. I have a proof of concept in place that will run the long running scripts. I just need to shape it into a set of APIs that allow me to program against the scripts, and deliver these different use case applications I'm envisioning. Once I have done, I will run for a few months in beta, but then probably open it up as a Server-Sent (SSE) events as a service, that allows anyone to execute long running scripts on the server side. Others may not be interested in measuring the performance gains, but I am guessing they will be interested in storing the streams of response.
