---
published: true
layout: post
title: Budget API Management Using Github
date: 2017-10-23T13:00:00.000Z
tags:
  - API Evangelist
  - Management
  - Github
image: >-
  https://s3.amazonaws.com/kinlane-productions/github/github-oauth-api-management.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/github/github-oauth-api-management.png" align="right" width="40%" style="padding: 15px;" /></p>I am always looking for the cheapest, easiest ways to get things done in the world of APIs. As a small business owner I'm always on the hunt for hacks to get done what I need, and hopefully make things easier for my users, while keeping things free, or at least minimally priced for my business. When it comes to my simplest of APIs, where I'm not looking to fully manage, but I do want anyone using them to authenticate, and pass in API keys, so that I can track on their use. In some cases I'm going to bill against this usage, but for the most part I just want to secure, and quantify their consumption.

The quickest and dirtiest way I will enable authentication for any API is using Github. First thing you do is create a Github OAuth application, which is available under settings for your Github user or organization. Then I add a JavaScript icon and login link, and then paste a PHP script at another location, where it will be handling the login. All you have to do is update the URLs in both scripts, and when someone clicks on icon, they'll be authenticated and then dropped back on the original page with username, and valid OAuth token--which then at this point you have a validated user, and valid token.

In some situations I just require that the appid and appkey be passed in with each API call. I do not rate limit, or bill against usage. I am just looking to identify consumers. Other projects I'm actively billing against consumption, but I'm doing this by processing the web server logs for the API. Again, bare bones operations. For the next level up, in the login PHP script I'm actually adding a user to a specific plan I've setup for an API using the AWS API Gateway, and adding their key to the gateway. Now a user has access to APIs, and the platform has (limited) access to their Github account, and a way to identify all their API usage.

I use this approach to account authentication for reading and writing to the underlying Github repository I'm using for API developer portals, and other applications. I'm also using these accounts to access API resources I'm serving up across a variety of projects. The combination allows for some pretty easy, but powerful engagement with API consumers via Github. The best part is I can rely on Github security and accounts for this layer of my API management. Next, I like that I can extend the features of their account using the AWS API Gateway. Extending the API management capabilities for specific projects when I have higher needs.

[You can find the scripts for this on Github](http://github.oauth.apievangelist.com/). If you don't want to host the server side portion of this, I recommend checking out OAuth.io, as they have a simple SaaS version of this that will work beyond just Github. However, if you are looking for quick and dirty solution, this one should work just fine.
