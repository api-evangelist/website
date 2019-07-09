---
published: true
layout: post
title: >-
  The Metropolitan Transportation Authority (MTA) Bus Time API Supports Service
  Interface for Real Time Information (SIRI)
date: 2018-01-11T13:00:00.000Z
tags:
  - API Evangelist
  - Transit
  - Real Time
  - Definitions
image: 'https://s3.amazonaws.com/kinlane-productions/mta/mta-bus-time-siri.png'
---
<p><a href="http://bustime.mta.info/wiki/Developers/SIRIIntro"><img src="https://s3.amazonaws.com/kinlane-productions/mta/mta-bus-time-siri.png" align="right" width="45%" style="padding: 15px;" /></a></p>The General Transit Feed Specification (GTFS) format for providing access to transit data has dominated the landscape for most of the time I have been researching transit data and APIs over the last couple of weeks. A dominance led by Google and their Google Maps, who is [the primary entity behind GTFS](https://developers.google.com/transit/). However the tech team at Streamdata.io brought it to my attention the other day that the Metropolitan Transportation Authority (MTA) Bus Time API Supports Service Interface for Real Time Information (SIRI), another standard out of Europe. [I think MTA's introduction to Siri](http://bustime.mta.info/wiki/Developers/SIRIIntro), and the story behind their decision tells a significant tale about how standards are viewed.

According to the MTA, _"[SIRI (Service Interface for Real Time Information)](http://user47094.vs.easily.co.uk/siri/overview.htm) is a standard covering a wide range of types of real-time information for public transportation.  This standard has been adopted by the European standards-setting body CEN, and is not owned by any one vendor, public transportation agency or operator.  It has been implemented in a growing number of different projects by vendors and agencies around Europe."_ I feel like their thoughts about SIRI not being owned by any one vendor is an important thing to take note of. While GTFS is an open standard, it is clearly a Google-led effort, and I'd say their decision to use Protocol Buffers reflects the technology, business, and politics of Google's vision for the transit sector.

The MTA has evolved SIRI as part of their adoption, opting to deliver APIs as more of a RESTful interface as opposed to SOAP, and providing responses in JSON, which makes things much more accessible to a wider audience. While technologically sound decisions, I think using Protocol Buffers or even SOAP have political implications when you do not deeply consider your API consumers during the planning phases of your API. I feel like MTA has done this, and understands the need to lower the bar when it comes to the access of public transit data, ensuring that as of an audience as possible can put the real time transit data to use--web APIs, plus JSON, just equals an easier interface to work with for many developers.

I'm getting up to speed with GTFS and GTFS Realtime, and I am also getting intimate with SIRI, and learning how to translate from GTFS into SIRI. I'm looking to lower the bar when it comes to accessing real time transit data. Something simple web APIs excel at. I've been able to pull GTFS and GTFS Realtime data and convert into simpler JSON. Now that MTA has introduced me to SIRI, I'm going to get acquainted with this specification, and understand how I can translate GTFS into SIRI, and then [stream using Server-Sent Events (SSE) and JSON Patch using Streamdata.io](http://apis.how/streamdata). Truly making these feeds available in real time, using common web standards.
