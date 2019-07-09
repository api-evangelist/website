---
published: true
layout: post
title: 'Machine Readable Definitions For All Things API, Including Your Bots'
date: 2017-09-12T16:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Bots
image: >-
  https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-robot-lightning-bold.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-robot-lightning-bold.png" align="right" width="30%" style="padding: 15px;" /></p>Every aspect of my business runs as either YAML or JSON. This blog post is YAML stored on Github, viewed as HTML using Jekyll. All the companies, services, tooling, building blocks, patents, and other components of my research all live as YAML on Github. Any API I design is born, and lives as an OpenAPI YAML document on Github. Sure, much of this will be imported, exported, and exported with a variety of other tools, but the YAML and JSON definition is key to every stop along the life cycle of my business, and the work that I do. 

It isn't just me. I'm seeing a big shift in how many platforms, services, and tooling operate, with often times YAML, and still in many situations it has JSON, XML, and CSV at its core. Everything you do should have some sort of schema definition, providing you with a template that you can reuse, share, collaborate, and communicate around. Platforms should allow for the creation of these template schema, and enable the exporting, and importing of them, opening up interoperability, and cross-platform functionality--much like APIs do in real-time using HTTP. This is what OpenAPI has done for the API lifecycle, and there should be many complementary, or even competing formats that accomplish the same, but for specific industries, and use cases. 

You can see this in action over at AWS, [with the ability to export your Lex bot schema for use in your Alexa skill](https://developer.amazon.com/blogs/alexa/post/d362a0ab-61f3-4b17-9fb7-1ad12f39496e/export-your-amazon-lex-bot-schema-to-use-in-your-alexa-skill). Sure, this is interoperability on the same platform, but it does provide one example of how YAML and JSON definitions can help use share, reuse, and develop common templates for not just APIs, but also the clients, tooling, and other platforms we are engaging with. You'll see this expand to every aspect of tech as continuous integration and deployment takes root, and Github continues it's expansion beyond startups, into the enterprise, government, and other institutions. Along the way there will be a lot of no name schema finding success, but we will also need a lot more standardization and maturing as we've seen with OpenAPI, for all of this to work.

I hear a lot of grumbling from folks when it comes to YAML. I get it, I had the same feeling. It also reminds me of how I felt about JSON when it first emerged. However, I find YAML to be very liberating of brackets, slashes, and other delimiters, but I also find it is just one format, and I should always be supporting JSON, XML, and CSV when it comes to one dimensional schema. I don't find it a challenge to convert between the formats, or keep some things one-dimensional to bridge to my spreadsheet oriented users. I actually feel it helps me think outside of my bubble. I enjoy rifling through the YAML and JSON templates I find on Github from a variety of operations, defining their bots, conversational interfaces, visualizations, CI/CD, configuration, clients, and other aspects of operations. Even if I'm never using them, I find it interesting to learn how others define what they are up to.