---
published: true
layout: post
title: Github Serverless
date: 2017-07-10T16:00:00.000Z
tags:
  - API Evangelist
  - Severless
  - Github
image: 'https://octodex.github.com/images/daftpunktocat-thomas.gif'
---
<p><a href="https://octodex.github.com/daftpunktocat-thomas"><img src="https://octodex.github.com/images/daftpunktocat-thomas.gif" align="right" width="30%" style="padding: 15px;" /></a></p>I run the entire front-end of my online presence using Github. [All my API Evangelist research lives as open repositories on Github, with the website running Jekyll, hosted on Github Pages](http://apievangelist.com/api-lifecycle/). My front-end is all HTML, JavaScript, and CSS, that leverages YAML data, and displayed using [Liquid](https://shopify.github.io/liquid/). It provides me a nice way to offload the public side of my operations to Github.

I am increasingly doing this with all of my data, by publishing it as YAML, and rendering a dynamic (static) API representation in JSON--all done with the same approach I'm using to publish my website(s). [You can get at all of the data I use across my API research in a single API Evangelist developer portal](http://developer.apievangelist.com/), which just aggregates all of the JSON APIs I've published across my network almost 100 Github repositories, and supporting sites.

Another thing I'm experimenting with is publishing simple JavaScript functions to individual pages within Github repositories. These scripts do a range of things from pulling items I've curated from [the Feedly API](https://developer.feedly.com/), fresh data from Google Sheets that I am using as data stores, and a variety of other jobs across my network of research sites, data projects, and API tooling. Some of these scripts I'm running manually, while others I run on a variety of schedules using [EasyCron](https://www.easycron.com).

The approach definitely has some significant limitations, but I find that I'm able to get quite a bit done with JavaScript by pulling data from external APIs and other feeds, and using each Github repo as storage, and the Github API as the read/write layer for this storage. I do not store any API keys, tokens, or other secrets in the Github repositories, I'm passing them all in via the URL, which isn't the most secure, and could in theory be abducted in transit even though I'm using SSL--something I'd like to improve upon by passing a single token to unlock a private store. I have access to external systems via APIs, storage and compute via Github, and I can control everything through variety of functional JavaScripts I maintain using Github, and keep indexed using APIs.json.

It is becoming a kind of poor man's serverless. I'm going to keep polishing my approach. Get better with my responses, and my approach to reading and writing data schema to the data storage folder in each of my repositories, which can then be read statically using JSON APIs I've pushed from this data, using Liquid. It is a pretty scrappy approach to serverless, but done in a way that takes the servers out of the equation for me, offloading the front-end and back-end work for my network of sites to Github. I am not sure where I'm going with this. Sometimes I get better results from a more straightforward API implementation on my Amazon infrastructure, but I am finding some interesting use cases, and seeing another side-effect I am enjoying--it is making my serverless infrastructure forkable and usable by others.
