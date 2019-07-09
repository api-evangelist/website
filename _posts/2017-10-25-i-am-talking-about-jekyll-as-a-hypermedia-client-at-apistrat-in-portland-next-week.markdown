---
published: true
layout: post
title: >-
  I Am Talking About Jekyll As A Hypermedia Client At APIStrat in Portland OR
  Next Week
date: 2017-10-25T13:00:00.000Z
tags:
  - API Evangelist
  - API Events
  - Hypermedia
  - Github
  - Clients
  - Static
  - Jekyll
image: 'https://s3.amazonaws.com/kinlane-productions/jekyll/jekyll-logo.png'
---
<p><a href="https://jekyllrb.com/"><img src="https://s3.amazonaws.com/kinlane-productions/jekyll/jekyll-logo.png" align="right" width="45%" style="padding: 15px;" /></a></p>Static website, and headless CMS approaches to providing API driven solutions have grown in popularity in recent years. Jekyll has been leading the charge when it comes to static website deployment, partly due to Github being behind the project, and their adoption for [Github Pages](https://pages.github.com/). I've been pushing forward a new approach to [using Jekyll as a hypermedia client](http://apievangelist.com/2017/09/20/jekyll-as-a-hypermedia-client/) to help deliver some of my API training and curriculum, and as part of this work I'm [giving a talk at APISTrat next week on the concept](http://events.linuxfoundation.org/events/apistrat). APIStrat is a great forum for this kind of project, helping me think through things in the form of a talk, the opportunity to share with an audience, and get immediate feedback on its viability, which I can then use to push forward my thinking on this aspect of my API work.

If you aren't familiar with [Jekyll](https://jekyllrb.com/), I recommend spending some time reading about it, and even implementing a simple site using Github Pages. I have multiple non-developers in my life who I've introduced to Jekyll, and it has made a significant impact on the way they do their work. Even if you do know about Jekyll, additionally I recommend spending time learning more about the underscore data folder, and the [concept of Jekyll collections](https://jekyllrb.com/docs/collections/). Every Jekyll site has its default data collection, and the opportunity to create any additional collection, using any name you desire. Within these folders you can publish static CSV, JSON, and YAML data files, using any schema you desire. All of these data collections then become available for referencing through the static Jekyll website or application.

All of this functionality is native Jekyll. Nothing revelatory from me. What I'm looking to push things forward around is what happens when the data collections are using a hypermedia media type. I'm using [Siren](https://github.com/kevinswiber/siren), which allows me to publish structured data collections, complete with links that define a specific experience across the data and content stored within collections. Next piece of the puzzle involves leveraging Jekyll and its use of Liquid as a hypermedia client, allowing me to build resilient websites and applications that are data driven, but can also evolve and change without breaking. All I do is update the static data behind, with minor revisions to the client--all using Github's API or Git infrastructure.

I've found Jekyll's data features to be infinitely beneficial, and is something I use to run my entire network of sites on. Adding the hypermedia layer is allowing me to push forward the storytelling experience around my API research and curriculum. The first dimension I find interesting, is that I can publish updates to the data for each project without breaking the client--classic hypermedia benefits. However, additionally, I can publish data and changes using Github workflows, and because every application runs as independent Github Pages driven website, it can stay in sync with updates via commits, or stay completely independent and never receiving any changes, which will also introduce another dimension of client stability, which is also so hypermedia.

I am still in the beta phase of evolving some of my API projects to use this approach. I'm pioneering this work using my API design curriculum. I'll be publishing an instance as part of[my session at APIStrat in Portland, OR next week](http://events.linuxfoundation.org/events/apistrat). I'll make sure I cover some of the Jekyll and Github basics for people in the audience who aren't familiar with these areas. Then I'll walk through how I'm using the Jekyll collections, includes, and the Liquid syntax to behave as a hypermedia client for my Siren data collections. All my talks live on Github, so if you can't make it you can still follow along with my work. [However, if you are going to be in Portland next week, make sure you come by and give a listen to my talk](http://events.linuxfoundation.org/events/apistrat)--I'd love to get your feedback on the concept.
