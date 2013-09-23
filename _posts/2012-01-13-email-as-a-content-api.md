---
layout: post
title: "Email as a Content API"
url: 'http://apievangelist.com/2012/01/13/email-as-a-content-api/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/ifthisthenthat-api-evangelist-to-wordpress-via-email.png'
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/ifthisthenthat/ifthisthenthat-api-evangelist-to-tumblr.png" alt="" width="300" align="right" />

I think email is highly underrated as a content API. I know its not what we traditionally think of as an API, but has a lot of potential as a basic interface into an application.

An example of this is [If This Then That (iftt)][1]. I use iftt to syndicate content to some of my blog platforms. As part of my blogging strategy I want posts I publish on API Evangelist, to also show up on my [Blogger][2], [Posterous][3], [Tumblr][4] and [Wordpress][5].

Using iftt you can setup tasks that get triggered on certain events. One such trigger is a new post to an RSS feed. So when a new blog posts shows up in the [API Evangelist RSS][6] feed I can have iftt pull the title and body and push to a channel. iftt provides channels for Posterous and Tumblr, allowing me to automatically syndicate using their APIs.  

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/ifthisthenthat/ifthisthenthat-api-evangelist-to-wordpress-via-email.png" alt="" width="300" align="right" />

There are no channels for Blogger and Wordpress, so I use their Gmail channel in conjunction with the post by email features on Blogger and Wordpress. So instead of using an API to syndicate my content, I use email as an interface for these blogging platforms.

Using email as a content API is obviously not for every situation, but for some application processes, it might just work for moving content from one application to another, without much overhead.

   [1]: http://ifttt.com/ (If This Then That)
   [2]: http://kinlane.blogspot.com/ (Blogger)
   [3]: http://kinlane.posterous.com/ (Posterous)
   [4]: http://kinlane.tumblr.com/ (Tumblr)
   [5]: http://kinlane.posterous.com/ (Wordpress)
   [6]: http://feeds.feedburner.com/ApiEvangelist (API Evangelist RSS Feed)
