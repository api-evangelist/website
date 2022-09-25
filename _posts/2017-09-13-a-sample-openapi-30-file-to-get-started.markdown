---
published: true
layout: post
title: A Sample OpenAPI 3.0 File To Get Started
date: 2017-09-13T15:00:00.000Z
tags:
  - API Evangelist
  - Definitions
image: 'https://s3.amazonaws.com/kinlane-productions/openapi/openapi-logo.png'
---
<p><a href="https://github.com/OAI/OpenAPI-Specification/edit/OpenAPI.next/examples/v3.0/petstore.yaml"><img src="https://s3.amazonaws.com/kinlane-productions/openapi/openapi-logo.png" align="right" width="15%" style="padding: 15px;" /></a></p>I am investing more time into [my Schema.org work](http://schema.org.apis.apievangelist.com/), alongside my learning about OpenAPI 3.0. [I'm pretty excited about the components object](http://apievangelist.com/2017/09/12/my-favorite-part-of-openapi-30-is-the-components-object/), and I want to push forward some of my Schema.org dictionary ideas, to help folks get better at reusing common schema throughout their work. [Schema.org](http://Schema.org) is the most robust vocabulary out there, and we shouldn't be reinventing the wheel in this area. I know the most important reason that folks aren't using is that they either don't know about it, or they are just lazy. I figure if I create some ready to go schema in an OpenAPI 3.0 components object, maybe people will be more inclined to put common schema to use.

To share my components I need basic OpenAPI 3.0 shell to hold all my reusable schema. I really don't care about the paths, and other elements being their. [So I headed over to the OpenAPI 3.0 Github repo and borrowed the sample Petstore OpenAPI 3.0 my friend Darrel Miller created](https://github.com/OAI/OpenAPI-Specification/edit/OpenAPI.next/examples/v3.0/petstore.yaml):

<script src="https://gist.github.com/kinlane/43934f44fd591a6ee59a45267d9e3066.js"></script>

I will change all the information in this sample to reflect my work, but I figured before I did I would share this example document with my readers. At first glance it doesn't look much different than version 2.0 of OpenAPI, but once you start studying you see the differences. You see the responses have JSON specific content types inserted in between their schema references. There is also a components object, with a couple of schema present--this is all I need. There are a bunch of other things you can store in your components object, but I think this provides a nice first look at what is going on.

If you are looking for some other working examples of OpenAPI 3.0 in action, [head over to Mike Ralphson's repository](https://github.com/Mermade/openapi3-examples/tree/master/pass/OAI), he has some additional ones you can play with. I don't know about you, but I learn from others. I need to reverse engineer API definitions from other people before I become fluent myself. I'm going to spend some time hand-crafting some OpenAPI 3.0 definitions, so that I become more fluent. It is tedious work when you are just getting going, but once you get it down, it becomes like any other language you use. I'm hoping to cut my teeth on this Schema.org work. I'm going to replicate the OpenAPI 2.0 work I did when I created over a 1,000 OpenAPIs for each of the Schema.org objects. I'm going to be using them to deploy APIs for clients, and in my API training and storytelling. I want all my examples to be reuable patterns that already exist, not anything custom that I pull out of my magic arse.