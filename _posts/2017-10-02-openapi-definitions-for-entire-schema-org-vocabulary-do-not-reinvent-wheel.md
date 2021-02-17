---
published: true
layout: post
title: 'OpenAPI Definitions For Entire Schema.org Vocabulary (Do Not Reinvent Wheel)'
image: https://s3.amazonaws.com/kinlane-productions2/schema-org/schema-org.png
---

<p><a href="https://schema.org/"><img src="https://s3.amazonaws.com/kinlane-productions2/schema-org/schema-org.png" align="right" width="30%" style="padding: 15px;" /></a>
<p>I am preparing my Schema.org Github repo with a variety of data sources for use across my API tooling and other projects. I’m trying to get better at using a common vocabulary, and not reinventing the wheel each time I start a new project. Schema.org has the most robust vocabulary of shared schema available today–so I am using this existing work as the core of mine.

<p>I am slicing and dicing the schema.org vocabulary into several formats that I can use in my OpenAPI-driven editors, and other tooling. <a href="https://schema.org/docs/developers.html">I took the JSON-LD representation for Schema.org</a>, and published it as a simpler JSON schema definition format that can be applied quickly to an OpenAPI. It isn’t perfect, and you lose a lot of the semantics in the process, but I think it still provides an important base for API designers, architects, and developers to use across their OpenAPI.

<p>It is pretty verbose, with over 150K lines, but it provides a fairly consolidated view of Schema.org classes, in a single set of definitions:

<script src="https://gist.github.com/kinlane/a71967811f8ab47c15919d75107c5843.js"></script>

<p>You can download a copy via the Gist, or you can find as <a href="https://github.com/api-evangelist-tools/schema-org/blob/master/_data/definitions/index.json">JSON</a> and <a href="https://github.com/api-evangelist-tools/schema-org/blob/master/_data/definitions/index.yaml">YAML</a> in my Github repository for this work. I’m going to be creating complete OpenAPI for each Schema.org class, as well as individual JSON schema files for each class. I just haven’t to figure out how to decouple them into individual files, yet containing all the relevant schema. I have the code, I just need to dial it in, when I have more time.

<p>I am going to use this Schema.org JSON schema as an autocomplete in my API design tooling, and using the OpenAPI as the source definition for my API deployment and testing tooling. I’ve been evolving <a href="http://org.open.referral.adopta.agency/">my Human Services Data API</a> work to easily generate server side code using OpenAPI, and I’m going to use the same code base to generate any Schema.org API, and deploy as AWS EC2 instance. I’m not looking to develop a SaaS solution, but a quick deploy solution for my own work, and projects I work on with my clients. As I work with more, I will validate that each of these definitions are 100% correct, and properly represent the Schema.org vocabulary.


