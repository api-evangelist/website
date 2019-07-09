---
published: true
layout: post
title: Having The Right Communications Pipeline For Your API Platform
date: 2017-07-10T13:00:00.000Z
tags:
  - API Evangelist
  - Communications
  - Jekyll
  - Blog
image: 'https://s3.amazonaws.com/kinlane-productions/matts-blog.png'
---
<p><a href="https://matthewreinbold.com/2017/07/04/SiteUpdate/"><img src="https://s3.amazonaws.com/kinlane-productions/matts-blog.png" align="right" width="40%" style="padding: 15px;" /></a></p>My friend Matthew Reinbold, formerly of Vox Pop, and now the Lead for the Capital One API Center of Excellence, as well as the maintainer of [web API events](http://webapi.events/) has shifted [his blogging platform to use Github, using Jekyll](https://matthewreinbold.com/2017/07/04/SiteUpdate/). Ok, yawn, why is this news? Someone is shifting the underlying platform for their blog. Well, first Matt is one of the leading API practitioners in the space, who is also a storyteller. Second, his approach highlights a set of tools that other API providers should be considering for their API communications pipeline.

Matt is using a pretty potent formula for his communications platform in my opinion, with a handful of essential ingredients:

- **[Github](https://github.com)** - Using a Github repository as the open source folder for your website.
- **[Github Pages](https://pages.github.com/)** - Using Github Pages to publish the front-end for your website.
- **[Jekyll](https://jekyllrb.com/)** - The content management system that sits in the folder for your website.
- **[CloudFlare](https://www.cloudflare.com/)** - The DNS and SSL front-end for your website, complete with analytics.
- **[Hover](https://www.hover.com/)** - The registrar for the domain which you offload DNS management to CloudFlare.

Matt is taking advantage of the benefits of static website development, which some of the benefits are, as Matt describes:

- **SPEED** - There’s no processing server side; posts have already been reduced to the essential atomic units of the web: HTML, Javascript, and CSS. There’s something poetic to me about that.
- **Security** - While not so much an issue with my own coded CMS, I lived in constant fear of missing a zero-day Wordpress exploit patch and finding myself, along with clients, compromised. Reducing the number of moving parts significantly decreases the places where something might go wrong.
- **Hosting** - Rather than having to find, research, and deploy to increasingly rare ColdFusion hosts (or port to another language), I can post my content to anywhere that supports HTTP/JS/CSS. hosting. This becomes very compelling given that Github Pages, one option, is free.

This is the cheapest and quickest way for your API to get a blog stood up, and get publishing stories about the value your API is bringing to the table. This approach isn't just limited to your developer portal or engineering team blog, this could be for partners, or any API related project that you are running. I publish a static Jekyll blog [for each area of my research](http://apievangelist.com/api-lifecycle/), and I try to always have one for each of my data, or API tooling project--telling the story of each project that is independent from the API Evangelist blog, providing a static log of everything that has happened.

Github isn't just a pipeline for code, it can be a pipeline for your communications and storytelling. It also can be a pipeline for your documentation, how-to-guides, and other resources. I'm happy to see Matt putting it to be use. Another thing I like about his post, other than him mentioning me ;-), is that he also mentioned the benefits of this approach over using Medium, which is something I've been advising API providers against for some time. In my opinion you are better off publishing your blog like Matt has, and then syndicating to Medium if you want. [There is a lot more detail available on Matt's story behind his new blog strategy](https://matthewreinbold.com/2017/07/04/SiteUpdate/), I recommend heading over and learning from what he's done.
