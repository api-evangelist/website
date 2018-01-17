---
published: true
layout: post
title: Breaking Down The Value Of Real Time APIs
date: 2018-01-17T09:00:00.000Z
tags:
  - API Evangelist
  - Real Time
  - Data
  - Streaming
  - Event Architecture
image: >-
  http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/80_168_800_500_0_max_0_1_-5.jpg
---
<p><img src="http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/80_168_800_500_0_max_0_1_-5.jpg" align="right" width="45%" style="padding: 15px;" /></p>I am working to evolve an algorithm for Streamdata.io that helps measure the benefits of their streaming service. There are a couple layers to what they offer as a company, but as I dive into this algorithm, there are also multiple dimensions to what we all perceive as real time, and adding more complexity to the discussion, it is something that can significantly shift from industry to industry. The Streamdata.io team was working to productize this algorithm for quantifying the value their service delivers, but I wanted to take some time to break it down, lay it out on the workbench and think about it before they moved to far down this path.

Ok. To help me get my brain going, I wanted to work my way through the dictionary sites, exploring what is real time?  Real time often seems to describe a human rather than a machine sense of time. It is about communicating, showing, or presenting something at the time it actually happens, where there is no notable delay between the action and its effect or consequence. All of this is relative to the human receiving the real time event, as well as defining exactly when something truly happens / happened. Real time in banking is different than real time in stock trading, and will be different than media. All requiring their own perception of what is real time, and what the effects, consequences, and perceptions are.

When it comes to the delivery or streaming of real time events, it isn't just about the delivering of the event, message, or transaction. It is about doing it efficiently. The value of real time gets ruined pretty quickly when you have to wade through too much information, or you are given too many updates of events, messages, and transactions that are not relevant. Adding an efficient element to the concept of what is real time. Real time, streaming updates of EVERYTHING are not as meaningful as streaming updates of only what just happened, staying truer to the concept of real time, in my opinion. Making the caching, and JSON Patch aspect of what Streamdat.io relevant to delivering a true real time experience--you only get what has changed in real time, not everything else.

To help me break down the algorithm for measuring the value delivered by Streamdata.io, I've started with creating three simple APIs.

- **Poll API** - A service for polling any API I give it. I can adjust the settings, but the default is that it polls it every 60 seconds, until I tell it to stop. Storing every response on a private Amazon S3 bucket.
- **API Size** - A service that processes each API response in the bucket and calculates the size of the response.
- **API Change** - A service that determines if an API response has changed from the previous response from 60 seconds before, identifying the frequency of change.

This gives me a baseline of information I need to set the stage for what is real time. I am trying to understand what changes, and potentially what the value is of precise updates, rather than sending everything over the wire with each API response. After I set this process into motion for each API, I have another set of APIs for turning on the Streamdata.io portion, which reflects the other side of the coin.

- **Stream API** - This service proxies an API with Streamdata.io and begins to send updates every 60 seconds. Similar to the previous set of services, I am storing the initial request, as well as every incremental update on Amazon S3.
- **API Size** - A service that processes each partial API response in the bucket and calculates the size of the response. If nothing changed, there was no JSON Patch response.
- **API Change** - A service that determines if a partial API response has changed from the previous response from 60 seconds before, identifying the frequency of change. If nothing changed, there was no JSON Patch response.

This gives me all the raw data I need to calculate the value which Streamdata.io delivers for any single API. However, it also gives me the raw data I need to begin calculating what is real time, and the value of it. We are tagging APIs that we catalog, allowing us to break down by common areas like finance, banking, media, transit, etc. This will allow us to start looking at how often things change within different sectors, and begin to look at how we can measure the value brought to the table when events, messages, and transactions are efficiently delivered in real time.

I am going to build me a dashboard to help me work with this data. I need to look at it for a couple of months, and run a number of different APIs through until I will know what dimensions I want to add next. I'm guessing I'm going to want some sort of freshness score on this, to see if something really truly is a new event, message, or transaction, or possibly being recirculated, duplicated, or some other anti-pattern. IDK. I'm guessing there are a number of new questions I will have about this data before I will truly be able to feel comfortable that the algorithm defines a meaningful vision of real time. Right now the algorithm sets to compute a couple meaningful efficiency gains.

- **Client Bandwidth (BW) Savings** - What efficiencies are realized when working with data in the client.
- **Server Bandwidth (BW) Savings** - What efficiencies are realized in bandwidth, as data is transmitted.
- **Server CPU Savings** - What efficiencies are realized on the service in CPU savings.

You can see this calculated for [the Washington Metropolitan Area Transit Authority (WMATA) Data APIs in a story I wrote last year](http://apievangelist.com/2017/12/11/cost-savings-analysis-for-washington-metropolitan-area-transit-authority-wmata-data-apis/). I want to be able to calculate these efficiency gains, but I want to be able to do it over time, and begin to try and understand the real time dimension of savings, not just what is introduced through caching. These three calculations speak to the caching aspect of what Streamdata.io delivers, not the real time benefits of the service. Something that won't be as straightforward to quantify, but I want to give it a try regardless.

<p><img src="http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/80_174_800_500_0_max_0_-5_-5.jpg" align="right" width="45%" style="padding: 15px;" /></p>

I want the algorithm to measure these efficiency gains, but I want to be able to capture the real time value of an API, both in quantifying the real time value delivered by the APIs, as well as the real time value delivered by Streamdata.io--establishing a combined real time ranking. This moves the algorithm into territory where it isn't just describing the value delivered by Streamdata.io to their clients, but also quantifying the value delivered by the combination of the clients API, and Streamdata.io working together. This is where I think things will start to get interesting, especially as we begin to move Streamdata.io services, and our algorithm into new industries, and adding new dimensions and perceptions to the discussion.

This is when things will start to get interesting I feel. By the time we get to this point, the tagging structure I will have applied to different APIs will have evolved, and become more precise as well. Allowing me to further refine the algorithm to apply a real time value ranking to specific streams within a single provider, or even in aggregate across providers. Allowing consumers to subscribe to the most precise real time streams of events, messages, and transactions, and cutting out the noise and redundancy. This is when we can move things beyond just large volumes of data in real time, but precise volumes of data in real time. Consuming only what is needed, training our machine learning models on exactly what is required, and keeping them updating in real time, allowing us to deliver real time artificial intelligence streams that are updated by the second, or minute, producing the most relevant models possible.
