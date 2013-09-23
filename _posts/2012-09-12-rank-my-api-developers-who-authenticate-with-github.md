---
layout: post
title: "Rank My API Developers Who Authenticate With Github"
url: 'http://apievangelist.com/2012/09/12/rank-my-api-developers-who-authenticate-with-github/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/singly-twitter-linkedin-github-facebook-authentication.png'
---

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/singly/singly-twitter-linkedin-github-facebook-authentication.png" alt="" width="150" align="right" />

I’m updating the login and authentication for my content management system, APIs and other tools to provide authentication using Twitter, Facebook, LinkedIn and Github by default. I’m using [Singly as an authentication provider][1], because their aggregation of API authentication, endpoints and objects across these providers is easy and most efficient way I know to get this accomplished.

In addition to it being easy, I’m using Singly for another advantage. Each service Singly provides has a discovery endpoint, which provides me with metadata and the other endpoints each service provides. I want to use this meta data to derive a quick snapshot ranking of my authenticating user.

For example, when a user authenticates via [Github Using Singly][2], I get the following meta data and endpoints:

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/singly/Singly-Github-Meta-Endpoints.png" alt="" width="550" />

Singly gives me 6 endpoints with data from the user’s activity in these areas. I’m looking to create an algorithm that will provide me with some quick ranking score based upon the number of repositories, followers and following a user has.

Right now I'm just going to add these up, take average across all my users that have logged in via Github. I’m sure I will evolve the design of the algorithm as I progress, but it should work for now.

My goal is to provide a little more insight into what type of user is signing up for my service, API or otherwise and possibly take different courses of action based upon their overall activity levels on Github. I mean, if they are Github superstar I want to know it, and also know if they aren’t very active at all.

I’ll explore the same algorithm for [Twitter][3], [Facebook][4] and [LinkedIn][5] authentication, but probably take different values into consideration for those social networks.

   [1]: https://singly.com/
   [2]: https://github.com/
   [3]: https://www.singly.com/docs/twitter
   [4]: https://www.singly.com/docs/facebook
   [5]: https://www.singly.com/docs/linkedin
