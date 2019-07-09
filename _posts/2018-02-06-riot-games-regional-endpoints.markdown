---
published: true
layout: post
title: Riot Games Regional API Endpoints
date: 2018-02-06T13:00:00.000Z
tags:
  - API Evangelist
  - Gaming
  - Regions
  - Performance
image: >-
  https://s3.amazonaws.com/kinlane-productions/riot-games/riot-games-developer-api.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/riot-games/riot-games-developer-api.png" align="right" width="45%" style="padding: 15px;" /></p>I'm slowly categorizing all the APIs I find who are offering up some sort regional availability as part of their operations. With the easy of deployment using leading cloud services, it is something I am beginning to see more frequently. However, there is still a wide variety of reasons why an API provider will invest in this aspect of their operations, and I'm looking to understand more about what these motivations are. Sometimes it is because they are serving a global audience, and latency kills the experience, but other times I'm seeing it is more about the maturity of the API provider, and they've have such a large user base that they are getting more requests to deliver resources closer to home.

[The most recent API provider I have come across who is offering regional API endpoints is from Riot Games](https://developer.riotgames.com/regional-endpoints.html), the makers of League of Legends, who offers [twelve separate regions for you to chose from](https://developer.riotgames.com/regional-endpoints.html), broken down using a variety of regional subdomains. The Riot Games API provides a wealth of meta data around their games, and while they don't state their reasons for providing regional APIs, I'm guessing it is to make sure the meta data is localized to whichever country their customers are playing in. Reducing an latency across networks, making the overall gaming and supporting application experience as smooth and seamless as possible. Pretty standard reasons for doing regional APIs, and providing a simple example of how you do this at the DNS level.

[RIot Games also provides a regional breakdown of the availability of their regional endpoints on their API status page](https://developer.riotgames.com/api-status/), adding another dimension to the regional API delivery conversation. If you are providing regional APIs, you should be monitoring them, and communicating this to your consumers. This is all pretty standard stuff, but I'm working to document every example of regional APIs I come across as part of my research. I'm considering adding a separate research area to track on the different approaches so I can publish a guide, and supporting white papers when I have enough information organized. All part of my work to understand how the API business operates, and is expanding. Showcasing how the leaders are delivering resources via APIs in a scalable way.
