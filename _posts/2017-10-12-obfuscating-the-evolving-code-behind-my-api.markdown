---
published: true
layout: post
title: Obfuscating The Evolving Code Behind My API
date: 2017-10-12T09:00:00.000Z
tags:
  - API Evangelist
  - Facade
  - Design
  - Deployment
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/christianity-under-construction_copper_circuit.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/christianity-under-construction_copper_circuit.jpg" align="right" width="40%" style="padding: 15px;" /></p>I'm dialing in a set of machine learning APIs that I use to obfuscate and distort the images I use across my storytelling. The code is getting a little more hardened, but there is still so much work ahead when it comes to making sure it does exactly what I needed it to do, with only dials and controls I need--nothing more. I'm the only consumer of my APIs, which I use them daily, with updates made to the code along the way, evolving the request and response structures until they meet my needs. Eventually the APIs will be done (enough), and I'll stop messing with them, but that will take a couple months more of pushing forward the code.

While the code for these APIs are far from finished, I find the API helps obfuscate and diffuse the unfinished nature of things. The API maintains a single set of paths, and I might still evolve  the number of parameters it accepts, and the fields it outputs, the overall will keep a pretty tight surface area despite the perpetually unfinished backend. I like this aspect of operating APIs, and how they can be used as a facade, allowing you to maintain one narrative on the front-end, even with another occurring behind behind the scenes. I feel like API facades really fit with my style of coding. I'm not really an A grade programmer, more a B- level one, but I know how to get things to work--if I have a polished facade, things look good.

Honestly, I'm pretty embarrassed by my wrappers for TensorFlow. I'm still figuring everything out, and finding new ways of manipulating and applying Tensor Flow models, so my code is rapidly changing, maturing, and not always complete. When it comes to the API interface I am focused on not introducing breaking changes, and maintaining a coherent request and response structure for the image manipulation APIs. Even though the code will at some point be stabilized, with updates becoming less frequent, the code will probably not see the light of day on Github, but the API might eventually be shared beyond just me, providing a simple, usable interface someone else can use.

I wouldn't develop APIs like this outside a controlled group of consumers, but I find being both API provider and consumer pushes me to walk a line of unfinished and evolving backend, with a stable, simple API, without any major breaking changes. The fewer fixes I have to do to my API clients, the more successful I've been pushing forward the backend, while keeping the API in forward motion without the friction. I guess I just feel like the API makes for a nice wrapper for code, acting as shock absorbers for ups and downs of evolving code, and getting it to do what you need. Providing a nice facade that obfuscates the evolving code behind my API.
