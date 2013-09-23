---
layout: post
title: "Efficient Social API Development with Singly"
url: 'http://apievangelist.com/2012/08/29/efficient-social-api-development-with-singly/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/singly-logo-horizontal.png'
---

[<img src="https://s3.amazonaws.com/kinlane-productions/singly/Singly-Personal-Data-Explorer.png" alt="" width="200" align="right" />][1]

Last week I announced that [API Evangelist and Singly were partnering][2], and while I’m helping Singly with their API Evangelism strategy and they are providing me with some vital data on some of the most important APIs in the industry and how developers are using them--I’m fascinated by the Singly unified API model and how it can simplify developing apps that use social and personal data.

As I do with any API, I sign up for an account, come up with an idea for a prototype, start hacking, then get to work telling the story of the process. To get started using Singly, I wanted to build a simply social data explorer that would help me understand how the platform works, but also give me a simple example for explaining to other developers.

Before diving in, let me start with the basics. What is [Singly][1]?

> Singly is a [unified API interface for accessing social and personal data][3] from the top API platforms. Singly has built an API on Twitter, Facebook, LinkedIn and other API platforms. Simplified the authentication, objects and API endpoints into a unified API, allowing you to access multiple APIs through a single, simpler API interface, drastically improving the time you have to spend developing social features in your web and mobile apps.

For this project I focused on the top social network APIs: [Facebook][4], [Foursquare][5], [Github][6], [Instagram][7], [LinkedIn][8] and [Twitter][9]. Ok, for many Github isn’t a social network. It’s something just geeks use, but to us, it is a social network. Anyways, let’s start building my social data exploration prototype.

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/github/github-logo.png" alt="" width="120" align="right" />

First, I [signed up for Singly using my Github login][10]. Once signed up, I added my first Singly application, which allows me to generate application specific Singly keys, which features I will use, and provides a single interface to store and manage that access for each social network that I will be using. When adding a new app, it takes some time to setup, and create an app definition in all 6 social networks and add keys to my Singly app, but once you are all done, all you have to worry about is a single Singly key--Singly takes care of the rest.

<img class="c2" src="https://s3.amazonaws.com/kinlane-productions/singly/Singly-App-Management.jpg" alt="" width="500" />

Now I have a single API for accessing all six social APIs. Singly provides consistent endpoints across these services:

  * https://api.singly.com/v0/services/facebook
  * https://api.singly.com/v0/services/foursquare
  * https://api.singly.com/v0/services/github
  * https://api.singly.com/v0/services/instagram
  * https://api.singly.com/v0/services/linkedin
  * https://api.singly.com/v0/services/twitter

Of course the objects you can work with across all of them aren’t the same, as they can be very different services, but the patterns are consistent and Singly standardizes the authentication and objects as much as possible across all APIs.

The first authentication and code library for Facebook took me about 10 minutes. Then after that I was able to reuse my code and had all five other services up and running in another 10 minutes.

How you use social data in your web and mobile applications will vary, but the unified API approach offered by Singly is taking API development to a new level. Using Singly I don’t think of terms of single APIs and how I have to approach each integration--I can now think of building social features into my applications across multiple APIs in a very seamless and efficient way.

I will be exploring this same approach, using the other blogging, productivity and quantified self services Singly offers. I just wanted to get started with the social APIs, and begin wrapping my head around more efficient API development using a unified API like Singly.

   [1]: https://singly.com (Singly)
   [2]: /2012/08/20/api-evangelist-partners-up-with-singly-to-evolve-the-social-and-personal-api-space/ (API Evangelist and Singly Were Partnering)
   [3]: https://singly.com (unified API interface for accessing social and personal data)
   [4]: https://www.singly.com/docs/facebook (Facebook)
   [5]: https://www.singly.com/docs/foursquare (Foursquare)
   [6]: https://www.singly.com/docs/github (Github)
   [7]: https://www.singly.com/docs/instagram (Instagram)
   [8]: https://www.singly.com/docs/linkedin (LinkedIn)
   [9]: https://www.singly.com/docs/twitter (Twitter)
   [10]: /2012/07/18/let-developers-register-for-your-api-with-their-github-profile/ (signed up for Singly which was instant using my Github login)
