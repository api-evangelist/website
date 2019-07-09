---
published: true
layout: post
title: >-
  More Outputs Are Better When It Comes To Establishing An API Observability
  Ranking
date: 2018-02-12T15:00:00.000Z
tags:
  - API Evangelist
  - Observability
  - Transparency
  - Monitoring
  - Regulations
  - Politics of APIs
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/ellisisland_blue_circuit.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/ellisisland_blue_circuit.jpg" align="right" width="45%" style="padding: 15px;" /></p>I've been evolving an observability ranking for the APIs I track on for a couple years now. I've bene using the phrase to describe my API profiling and measurement approach [since I first learned about the concept from Stripe](http://apievangelist.com/2016/10/25/thinking-about-an-api-observability-stack/). There are many perspectives floating around the space about what observability means in the context of technology, however mine is focused completely on APIs, and is more about communicating with external stakeholders, more than it is just about monitoring of systems. To recap, [the Wikipedia definition for observability is](https://en.wikipedia.org/wiki/Observability):

> _Formally, a system is said to be observable if, for any possible sequence of state and control vectors, the current state can be determined in finite time using only the outputs (this definition is slanted towards the state space representation). Less formally, this means that from the system's outputs it is possible to determine the behavior of the entire system. If a system is not observable, this means the current values of some of its states cannot be determined through output sensors._

Most of the conversations occurring in the tech sector are focused on monitoring operations, and while this is a component of my definition, I lean more heavily on the observing occurring beyond just internal groups, and observability being about helping keep partners, consumers, regulators, and other stakeholders be more aware regarding how complex systems work, or do not work. I feel that observability is critical to the future of algorithms, and making sense of how technology is impacting our world, and APIs will play a critical role in ensuring that the platforms have the external outputs required for delivering meaningful observability.

When it comes to quantifying the observability of platforms and algorithms, the more outputs available the better. Everything should have APIs for determining the inputs and outputs of any algorithm, or other system, but there should also be operational level APIs that give insight into the underlying compute, storage, logging, DNS, and other layers of delivering technological solutions. There should also be higher level business layer APIs surrounding communication via blog RSS, Twitter feeds, and support channels like email, ticketing, and other systems. The more outputs around platform operations there are, the more we can measure, quantify, and determine how observable a platform is using the outputs that already exist for ALL the systems in use across operations.

To truly measure the observability of a platform I need to be able to measure the technology, business, and politics surrounding its operation. If communication and support exist in the shadows, a platform is not observable, even if there are direct platform APIs. If you can't get at the operational layer like logging, or possibly Github repositories used as part of continuous integration or deployment pipelines, observability is diminished. Of course, not all of these outputs should all be publicly available by default, but in many cases, there really is no reason they can't. At a minimum there should be API access, with some sort of API management layer in place, allowing for 3rd party auditors, and analysts like me to get at some, or all of the existing outputs, allowing us to weigh in on an overall platform observability workflow.

As I continue to develop my API observability ranking algorithm, the first set of values I calculate are the number of existing outputs an API has. Taking into consideration the scope of core and operational APIs, but also whether I can get at operations via Twitter, Github, LinkedIn, and other 3rd party APIs. I find many of these channels more valuable for understanding platform operations, than the direct APIs themselves. Chatter by employees, and commits via Github can provide more telling signals about what is happening, than the intentional signals emitted directly by the platform itself. Overall, the more outputs available the better. API observability is all about leveraging existing outputs, and when companies, organizations, institutions, and government agencies are using solutions that have existing APIs, they are more observable by default, which can have a pretty significant impact in helping us understand the impact a technological solution is having on everyone involved.
