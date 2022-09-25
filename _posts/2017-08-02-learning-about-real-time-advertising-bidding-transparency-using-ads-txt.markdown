---
published: true
layout: post
title: Learning About Real-Time Advertising Bidding Transparency Using Ads.txt
date: 2017-08-02T13:00:00.000Z
tags:
  - API Evangelist
  - Advertising
  - Transparency
  - Observability
image: 'https://s3.amazonaws.com/kinlane-productions/ads-txt/ads.txt-about.png'
---
<p><a href="https://iabtechlab.com/ads-txt/"><img src="https://s3.amazonaws.com/kinlane-productions/ads-txt/ads.txt-about.png" align="right" width="40%" style="padding: 15px;" /></a></p>[I was learning about real-time bidding transparency using Ads.txt from Lukasz Olejnik](https://blog.lukaszolejnik.com/real-time-bidding-transparency-via-ads-txt/). The mission of the ads.txt project is to "[increase transparency in the programmatic advertising ecosystem. Ads.txt stands for Authorized Digital Sellers and is a simple, flexible and secure method that publishers and distributors can use to publicly declare the companies they authorize to sell their digital inventory.](https://iabtechlab.com/ads-txt/)" While Ads.txt isn't an API, it is an open, machine readable definition that is working to make advertising more transparent and observable to everyone, not just people in the ad-tech space.

Ads.txt works similar to robots.txt, and is a simple text file that lives in the root of a domain, listing the companies that have permission to sell advertising. The format is new, so there isn't a lot of adoption yet, but [you can see one in action over at the Washington Post](https://www.washingtonpost.com/ads.txt). Helping make platforms observable is why I perform as the API Evangelist. I see them as one of the important tools we have for making systems, algorithms, and platforms more observable, and less of a black box. I see ads.txt having similar potential for the world of advertising, and something that eventually could have an API, for helping make sense of the very distributed, brokered, and often dark world of online advertising.

Honestly, I know almost nothing about online advertising. I have a basic level of understanding of Google Analytics, Adwords, and Adsense, as well as reading the blogs, and documentation for many advertising APIs I come across in my regular monitoring of the API space. I am just interested in ads.txt as an agent of observability, and pulling back the current on who is buying and selling our digital bits online. I am adding ads.txt to [my API definitions research](http://definitions.apievangelist.com/). This will allow me to keep an eye on the project, see where it goes, and think about the API level for aggregation of the ad network data, on maybe Github or something--caching ads.txt on a daily basis. Who knows where it will go. I'll just keep learning, and playing around until it comes into a little more focus.

I'm guessing that not all companies will want to be transparent like this. Folks who have the upper hand, or are just doing shady things, rarely like to have the curtain pulled back. I'll keep an eye ads.txt adoption, and also spend some time thinking thinking about transparency and observability at the API monetization and plans level, going beyond just advertising, which is the staple of the web, and think about how we can keep things open when it comes to API business models.
