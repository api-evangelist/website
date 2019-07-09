---
published: true
layout: post
title: An Organized Approach to OpenAPI Vendor Extensions Across API Teams
date: 2018-01-15T09:00:00.000Z
tags:
  - API Evangelist
  - Definitions
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/containership_blue_circuit.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/containership_blue_circuit.jpg" align="right" width="45%" style="padding: 15px;" /></p>One of aspects of a project I've been assisting with recently involves helping define, implement, and organize the usage of OpenAPI vendor extensions across a distributed microservice development team. When I first began advising this group, I introduced them to the concept of extending the OpenAPI definition using x-extension format, expanding the teams approach to how they use the OpenAPI specification. They hadn't heard that you can extend OpenAPI beyond what the specification brings to the table, allowing them to make it deliver exactly what they needed.

Within this project each microservice exists in its own Github repository, with an OpenAPI definition available in the root, defining the surface area of the API. At the organizational level, I have a script that will loop through all Github repos, spider each OpenAPI looking for any x-extensions, and then it aggregates them into a single master list of OpenAPI vendor extensions that are used across all APIs. I then take the list, and add descriptions to each verified extension, and when I come across ones I haven't seen before I reach out to microservice owners to understand what the vendor extension is used for, and ensure it is in alignment with overall API governance for the project.

I am looking to encourage API designers, developers, and architects to extend OpenAPI. I am also looking to help them be responsible with this power, and make sure they are doing it for good reasons. I am also looking to organize, then educate across teams regarding how different groups are using OpenAPI vendor extensions, and incentivize the reuse and standardization of these extensions. I see vendor extensions as an area for potential innovation when it comes to defining what an API is capable of, as well as the relationship each microservice has with its supporting architecture. Acting for a relief valve for the often perceived constraints of the OpenAPI specification.

This project reminded me that I need to make sure and add a reminder to pick my head up each week and spend time aggregating vendor extensions from across the API space. [I have a section dedicated to them in my OpenAPI toolbox](http://openapi.toolbox.apievangelist.com/), but I haven't added anything to it recently. OpenAPI Vendor extensions are an important way to learn about how companies are extending the specification, and similar to what I'm doing for this individual project, it is important to aggregate and organize them so people in the community can learn from them, and reuse them whenever possible.
