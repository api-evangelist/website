---
title: My New CMS For Manging My Network Of Github Site
date: 2017-05-15 15:00:00 Z
tags:
- CMS
- My
- Github
- Amazon S3
image: https://s3.amazonaws.com/kinlane-productions/siteleaf/siteleaf-logo.png
---

<p><img style="padding: 15px;" src="https://s3.amazonaws.com/kinlane-productions/siteleaf/siteleaf-logo.png" align="right" width="25%" /></p>All of my websites have run 100% on Github for the last three years. The core of my API industry research is always in JSON or YAML, stored in individual project-based Github repositories. I leverage Jekyll for the page and other content collections (blogs, news, etc.). Since 2011 I've used my own homebrew CMS system, making it accommodate the switch to a more static presence on Github. 

Over the weekend I ditched my CMS and lit up a new CMS I came across called Siteleaf, which has all the core features I need: Github, Jekyll, Amazon S3, and API. This is how I manage a couple hundred API research sites, and the images, video, and other heavy objects I store using Amazon S3--these services and tools are critical to my business.

I am writing this post in Siteleaf. I do not have it setup for publishing across all of my websites, but so far it has worked for getting up 3 blog posts on API Evangelist, providing me with a successful test run. Siteleaf represents how I think software tools should be built, providing a simple useful application, that leverages Github, common storage like AWS S3, Dropbox, and others, and [of course, they should ALL have an API](https://learn.siteleaf.com/api/).