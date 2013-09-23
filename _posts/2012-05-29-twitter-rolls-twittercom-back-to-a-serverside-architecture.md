---
layout: post
title: "Twitter Rolls Twitter.com Back to a Server-Side Architecture"
url: 'http://apievangelist.com/2012/05/29/twitter-rolls-twitter.com-back-to-a-server-side-architecture/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/Twitter-Home.png'
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/twitter/Twitter-Home.png" alt="" width="250" align="right" />

Twitter just [rolled back their architectural approach for Twitter.com][1] back to a server side implementation.

If you remember back in September of 2010, [Twitter rebuilt Twitter.com to use a web application architecture][2] that pushed all of the UI rendering and logic to Javascript running in the browser and consumed the Twitter API directly.

Now they are "taking back control" of their front-end performance by moving the rendering back to the server. They don't say whether they don't use the APIs at all, but I am working under the assumption that they abandoned them.

Twitter felt the API driven web application architecture broke new ground, offered a number of advantages, but it lacked support for various optimization techniques available only on the server.

I was excited to see Twitter go with the API driven approach, along other sites, like [the FCC][3].  I hate to see them abandon it.

_**What does this say about an API oriented architecture?**_

Are we not ready? Are there are not enough tools for optimization, or the talent to deliver the performance necessary for Internet at scale via API driven architecture?  Or maybe there are other business reasons for stopping eating their own dog food and going back to a server side architecture?

   [1]: http://engineering.twitter.com/2012/05/improving-performance-on-twittercom.html
   [2]: /admin/blog/twitter%20eats%20own%20dogfood%20api%20evangelist
   [3]: http://blog.programmableweb.com/2011/04/06/everything-should-be-an-api-says-fcc/ (FCC Website)
