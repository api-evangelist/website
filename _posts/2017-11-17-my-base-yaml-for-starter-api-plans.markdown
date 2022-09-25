---
published: true
layout: post
title: My Basic YAML For Starter API Plans
date: 2017-11-17T09:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Plans
image: >-
  http://kinlane-productions.s3.amazonaws.com/api_evangelist_site/blog/api_plans_pricing_tiers.png
---
<p><img src="http://kinlane-productions.s3.amazonaws.com/api_evangelist_site/blog/api_plans_pricing_tiers.png" align="right" width="45%" style="padding: 15px;" /></p>[I started developing a machine readable format for describing the API plans and pricing for leading API providers a few years back](http://plans.apievangelist.com/). Eventually I'd like to see the format live alongside OpenAPI, Postman, and other machine readable API specifications within a single APIs.json index. I am looking to adequately describe the plans and pricing for APIs, which are often just as important as the technical details, in the same way we've describe the technical surface area of an API using OpenAPI for some years now. People love to tell me that I will never be able to do it, which only makes me want to do it more.

I'm revisiting my work as part of work I'm doing on a clients project, which I'm also using to push forward my API portal and management toolbox. The project I'm working on has two API plans:

1) Starter - The free level of access everyone gets when signing up for access to an API.
2) Verified - A verified level of pay as you go usage once you have credit card on file.

I've taken the common elements across these plans and described them in a YAML format which allows me to remix the elements into the two plans I currently have, while also allowing me to reuse them for possible future plans, helping keep my approach consistent.

<script src="https://gist.github.com/kinlane/e1bbbabe8f24c0aced4d41b45f2295d8.js"></script>

I'm using the plan elements in this YAML file to generate the plans and pricing page for each API. Generating two separate plan boxes, with the details, and elements of each plan. I keep all the moving parts of each plan defined as separate fields and collections so that I can reuse in any new plans. I also make use of the individual elements in comparison charts, and other pricing and plan related resources through an APIs portal. The specification isn't perfect, but it provides me a starting point for considering how I make my API plans and pricing machine readable, and indexed as part of the [APIs.json](http://apisjson.org/) for each of my projects.

Next, I am taking API plan templates and auto-generating plans using AWS API Gateway. I'm going to play around with recreating some of the common plans we see for leading API providers out there using an existing gateway solution. Similar to generating the technical surface area of an API using AWS API Gateway, I'm looking to generate the business surface area of each API using the API Gateway in the same way. Definitely still a lot of work ahead of me when it comes to polishing my API plan specification format, but I feel like it is pretty good start, and after publishing a version for leading API providers, as well as some of the custom projects I'm working on, I think it will be a little more ready for prime time.
