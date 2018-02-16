---
published: true
layout: post
title: >-
  Insecurity Around Providing Algorithmic Transparency And Observability Using
  APIs
date: 2018-02-16T11:00:00.000Z
tags:
  - API Evangelist
  - Algorithms
  - Transparency
  - Observability
  - Ranking
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/68_113_800_500_0_max_0_-1_-1.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/68_113_800_500_0_max_0_-1_-1.jpg" align="right" width="45%" style="padding: 15px;" /></p>[I'm working on a ranking API for my partner Streamdata.io to help quantify the efficiencies they bring to the table when you proxy an existing JSON web API using their service](https://streamdata.io/blog/benchmark-quantifying-api-performance/). I'm evolving an algorithm they have been using for a while, wrapping it in a new API, and applying it across the APIs I'm profiling as part of my [API Stack](http://theapistack.com), and the [Streamdata.io API Gallery](https://streamdata.io/developers/api-gallery/) work. I can pass the ranking API any OpenAPI definition, and it will poll and stream the API for 24 hours, and return a set of scores regarding how real time the API is, and what the efficiency gains are when you use Streamdata.io as a proxy for the API.

As I do this work, I find myself thinking more deeply about the role that APIs can play in helping make algorithms more transparent, observable, and accountable. My API ranking algorithm is pretty crude, but honestly it isn't much different than many other algorithms I've seen companies defend as intellectual property and their secret sauce. Streamdata.io is invested in the ranking algorithm and API being as transparent as possible, so that isn't a problem here, but each step of the process allows me to think through how I can continue to evangelize other algorithm owners to use APIs, to make their algorithms more observable and accountable.

In my experience, most of the concerns around keeping algorithms secret stem from individual insecurities, and nothing actually technical, mathematical, or proprietary. The reasons for the insecurities are usually that the algorithm isn't that mathematically sophisticated (I know mine isn't), or maybe it is pretty flawed (I know mine is currently), and people just aren't equipped to admit this (I know I am). I've worked for companies who venomously defend their algorithms and refuse to open them up, because in the end they know they aren't defensible on many levels. The only value the algorithm possesses in these scenarios is secrecy, and the perception that there is magic going on behind the scenes. When in reality, it is a flawed, crude, simple algorithm that could actually be improved upon if it was opened up. 

I'm not insecure about my lack of mathematical skills, or the limitations of my algorithm. I want people to point out its flaws, and improve upon my math. I want the limitations of the algorithm to be point out. I want API providers and consumers to use the algorithm via the API (when I publish) to validate, or challenge the algorithmic assumptions being put forth. I'm not in the business of selling smoke and mirrors, or voodoo algorithmics. I'm in the business of helping people understand how inefficient their API responses are, and how they can possibly improve upon them. I'm looking to develop my own understanding of how can make APIs more event-driven, real time, and responsive. I'm not insecure about providing transparency and observability around the algorithms I develop, using APIs--all algorithm developers should be as open and confident in their own work.
