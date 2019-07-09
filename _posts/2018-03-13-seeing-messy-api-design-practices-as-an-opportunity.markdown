---
published: true
layout: post
title: Seeing Messy API Design Practices As An Opportunity
date: 2018-03-13T13:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Definitions
  - Discovery
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/13439120_10154285627219813_3054276594176638940_n_copper_circuit_2.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I'm generating OpenAPI definitions for a wide variety of APIs currently, and I'm regularly stumbling on the messiness of the API design practices being deployed. When you are exposed to a large number of different APIs it is easy to get frustrated, begin ranting, and bitching about how ignorant people are of healthy, sensible API practices. This is the easy route. Making sense of it all, finding the interesting signals and patterns, and extracting where the opportunity are takes a significant amount of effort (so does biting tongue).

After profiling almost 500 API providers, I have almost 25K separate API paths indexed using OpenAPI, and APIs.json. I've tagged each API path using its OpenAPI definition. Pulling words from the path name, and any summary and description provided within the API documentation. Doing my best to describe the value contained within each API resource. Then I started grouping by these tags, to see what it produced. Sometimes the API paths it lists makes total sense, but most of the time it makes no sense at all. Then, I started noticing interesting patterns in how people describe their resources. Grouping things like "favorites" across all types of APIs, revealing some pretty interesting perspectives, and honest views of the resources being exposed. 

Something as simple as "activities" can mean 30 or 40 different things when applied across CRM, storage, DNS, travel or sports APIs. At first, I'm like this shit is broken. The more time I spend with the mess, the more I'm starting to think there is more to this mess than meets the eye. I could be wrong. I often am. It is likely just my contrarian view of things, and my unique view of the API landscape in action. [Where many people see duplicative work, I see common patterns](http://apievangelist.com/2017/07/31/you-see-duplicate-work-while-i-see-common-patterns/). I just see the landscape differently than people who are just looking to get their work done, sell a product or service, and find an exit for their startup. I'm not looking for any solution, doorway, or exit. I just see all of this as a journey, and I'm fascinated by how people view their API resources, then describe, tag and bag them.

I'm not sure where all of this API indexing and tagging will lead me. I don't feel compelled to sort out the mess, and covert any of these API providers to a more sensible API religion. I'm just looking to understand more about the motivations behind why they did what they did. Provide commentary on where they fit into the bigger picture, and if they are delivering interesting and valuable API resources, help make them more discoverable, and executable when it matters. As I have been doing for the las eight years, I'm just looking to learn from others, and stay in tune with where things are headed, no matter how messy it might be. I see APIs as a kind of controlled chaos, which are increasingly driving our already chaotic lives.
