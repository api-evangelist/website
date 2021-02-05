---
title: I Published 60K Patents To Github As Part Of My API Patent Research
date: 2017-06-27 09:00:00 Z
tags:
- Patents
- Jekyll
- Github
- API Evangelist
image: https://s3.amazonaws.com/kinlane-productions/patents/api-evangelist-patent-listing-screenshot.png
---

<p><a href="http://patents.apievangelist.com/#Patents"><img src="https://s3.amazonaws.com/kinlane-productions/patents/api-evangelist-patent-listing-screenshot.png" align="right" width="40%" style="padding: 15px;" /></a></p>I've been migrating from my own homebrew CMS system over the last couple of weeks, ditching it for a variety of existing services, balancing my operations across a diverse set of platforms I've identified as useful. I'm using Github and Jekyll to manage my content system, storing thinks like blog, news, notes, and patents there. Github repos are well suited for storing this type data for free (if it is public), and Jekyll is well suited for helping me manage small to large repositories of content I need to use across my platform.

This last week I migrated 60K patents I had filtered out of all the [XML dumps of patents I downloaded](http://patents.reedtech.com/pgrbft.php), between the years of 2005 and 2016. I filtered out any patent with API or application programming interface in the title, abstract, or body of the patent. Once done importing, I clean up the body a little bit and publish each one as a Jekyll post within a Github repo. I had to break them down by year, as Github started getting wonky after 10K file, but the Jekyll structure works well for managing up to 10K patents. Once committed, I find the Jekyll post and data structure pretty easy to navigate and use for some API storytelling.

[I like having the full listing of title and abstract available to search in a single public HTML page](http://patents.apievangelist.com/#Patents). I have also started publishing keyword filters for each area of my research. It is taking me a while to build the index for each JSON API, but it is allowing me to quickly get at [cached searches for machine learning, API management](http://patents.apievangelist.com/#Patents), and other patents that affect the areas of the API lifecycle I'm keeping a close eye on. I will keep adding filters and enhancing the ones that I have, but ultimately it takes me reading a large number of patents and then actually tagging each one, that will help me build a useful API patent catalog.

I feel that these relevant patents help tell an important story about each layer of the API lifecycle. Patents add another dimension to the story of what is going on when it comes to API design, deployment, management, discovery, and other areas that are growing in 2017, and in coming years. The products, services, and tooling I track on from organizations included in [my API lifecycle research](http://apievangelist.com/api-lifecycle/) paint a significant part of the picture, but I feel that patents pull back the curtain just a little bit more when it comes to what companies are thinking. I will keep processing new files from the USPTO every couple of weeks, evolving my filters, and tagging patents for better recall in my API patent storytelling.
