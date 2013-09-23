---
layout: post
title: "Real-Time Notification Layer Within Your API"
url: 'http://apievangelist.com/2013/03/15/real-time-notification-layer-within-your-api/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/cisimple-plus-pusher.png'
---

<img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/pusher/cisimple-plus-pusher.png" alt="" width="250" align="right" />

[This story comes][1] from Phil Leggetter ([@leggetter][2]) over at [Pusher][3]. Its about a client of theirs, [cisimple][4], which provides continuous delivery services for mobile developers. [cisimple just released a new API][5], which gives mobile developers more control over the build processes for their mobile applications.

Using the cisimple API you can kick off new builds and download artifacts from your mobile dev process. cisimple is a very interesting API resource, that I will definitely be watching, and I’m sure I will be writing about in the near future. But what I really think is interesting is that cisimple is allowing clients to register for real-time updates via Pusher channels, using API tokens.

This means that when you use cisimple to manage your mobile development, you now have a real-time push system that will send notifications when builds start, pass, fail, etc. This opens up a whole world of human integration with the build process via desktop and mobile notifications, but also can be used in other systems that play a role in your dev cycles.

The weaving of a Pusher real-time notification layer into the cisimple API is pretty innovative. Something I’m sure will deliver huge value to their customers. But think of the potential as a standard approach for all API owners? You could offer developers real-time notifications about their own usage of your API, providing them with an intimate view of how their application(s) are using an API. Addiitionally it seems like you could set up a pretty interesting system wide notification layer that would let you, as the API owner, establish notification channels regarding overall API usage, thresholds and other important signals from your platform.

As I continue to dive into the [world of real-time APIs][6], I’m surprised at the multiple ways in which we can truly deliver real-time value using APIs. cisimple API Pusher is in interesting addition.

   [1]: http://blog.pusher.com/using-pusher-to-power-cisimples-real-time-api/
   [2]: https://twitter.com/leggetter
   [3]: http://pusher.com/
   [4]: https://www.cisimple.com/
   [5]: http://blog.cisimple.com/2013/03/06/check-out-our-shiny-new-api-and-pusher-integration/
   [6]: http://apievangelist.com/trends/realtime.php (real-time)
