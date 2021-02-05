---
published: true
layout: post
title: 'API For Processing Common Logging Formats And Generating OpenAPI Definitions'
date: 2019-07-30T09:00:00.000Z
tags:
  - API Evangelist
  - Discovery
  - Logging
  - Search
image: https://s3.amazonaws.com/kinlane-productions/algorotoscope-master/abandonedbuildings_blue_circuit.jpg
---
<img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" />
I’ve invested a lot of time in the last six months into various research, scripts, and tooling to help me with finding APIs within the enterprise. This work is not part my current role, but as a side project to help me get into the mindset of how to help the enterprise understand where their APIs are, and what APIs they are using. Almost every enterprise group I have consulted for has trouble keeping tabs on what APIs are being consumed across the enterprise, and I’m keen on helping understand what the best ways are to help them get their API houses in order.

While there are many ways to trace out how APIs are being consumed across the enterprise, I want to start with some of the basics, or the low hanging when it came to API logging within the enterprise. I’m sure there are a lot of common logging locations to tackle, but my list began with some of the common cloud platforms in use for logging of operations to begin my work—focusing on the following three cloud logging solutions:

- **Amazon CloudFront** - Beginning with the cloud leader, and looking at how the enterprise is centralizing their logs with CloudFront.
- **Google StackDriver** - Next, I found Google’s multi-platform approach interesting and worth evaluating as part of this work.
- **Azure Logging** - Of course, I have to include Azure in all of this as they are a fast growing competitor to Amazon in this space.

After establishing a short list of cloud platforms logging solutions, I began looking at which of the common web server formats I should be looking for within these aggregate logging locations, trying to map out how the enterprise is logging web traffic. Providing me with a short list of the three most common web server formats I should be looking at when it comes to mapping the enterprise API landscape—-providing artifacts of the APIs that enterprise groups are operating.

- **Apache Log File** - The most ubiquitous open source web server out there is the default for many API providers.
- **NGINX Log File** - The next most ubiquitous open source web server is definitely something I should be looking for.
- **IIS Log File** - Then of course, many Microsoft web server folks are still using IIS to serve up their API infrastructure.

These three web server logging formats represent a significant slice of the API logging pie. If I can identify these logging formats across common cloud logging locations, I feel that I can provide a pretty significant solution for finding the APIs that are in use across the enterprise. However, I didn’t just want to be looking a the web server logging for understanding what APIs are being served up, I also wanted to look at the exhaust from how APIs are being consume by looking at these two web browser and proxy traffic formats:

- **HAR File** - Allowing for the discovery of APIs that are used in web and browser applications across common use cases.
- **Charles Proxy JSON Session** - Using a common proxy application to reverse engineer web and mobile application API calls.

These cloud logging solutions, web server formats, as well as browser and proxy solutions give me a pretty interesting look at the API discovery pie. I have scripts to help identify these common formats, and then automatically produce OpenAPI definitions from them. It is pretty easy to run these scripts in a variety of ways to help automatically produce a catalog of OpenAPI definitions from them, automating the mapping of the API landscape within he enterprise. I have all of these scripts working for me in a variety of capacities, the next step is to further automate them, organize them into more of a usable suite of API tooling, then unleash them on a larger set of enterprise logs.

All of my scripts currently run as APIs, as I'm API-first, but I’m currently exploring ways in which I can better execute them at the command line, and as autonomous solutions that can be installed within the enterprise, without any external connections or dependencies. I have a list of ways in which I want to add more value on top of these API discovery solutions, allowing me to generate revenue from them. However right now, I am more interested in ensuring they help automate the API landscape across the majority of enterprise logging solutions. Once I dial this in, I will be looking for more ways to implement the existing functionality, as well as evolve to cover other platforms and formats. I’m just looking to deliver a basic solution for understanding where the hell all the APIs are in the enterprise, before I look to bake in more advanced features.
