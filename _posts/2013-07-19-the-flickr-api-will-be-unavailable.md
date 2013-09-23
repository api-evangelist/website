---
layout: post
title: "The Flickr API Will Be Unavailable"
url: 'http://apievangelist.com/2013/07/19/the-flickr-api-will-be-unavailable/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/flickr-logo.jpg'
---

<img src="https://s3.amazonaws.com/kinlane-productions/flickr.jpg" alt="" width="250" align="right" />

I received an email from Flickr today about a planned API outage later this month. I'm an afficinado of the interesting ways API providers communicate around maintenance and outages within their ecosystem, and wanted to share:

> _We see that you own an active API key for the Flickr API, and wanted to let you know that Flickr is scheduling a maintenance outage for Thursday, July 25th, from 4 to 10pm PDT._

> _During the outage window, the Flickr API will be unavailable. As such, you may want to adjust your app to gracefully handle the error that will result when it calls our API during the outage. (If your app is not yet public, this will only impact your personal use of the API.)_

> _Specifically, a call to the Flickr API will result in the following error: 105: Service currently unavailable (Site Disabled). Here are example responses to expect:_

_XML (REST): _

_JSONP: jsonFlickrApi({ "stat": "fail", "code": "105", "message": "Service currently unavailable (Site Disabled)" })_

_JSON: { "stat": "fail", "code": "105", "message": "Service currently unavailable (Site Disabled)" }_


> _We hope this helps, and thank you for being a member of our API community,_

> _The Flickreenos_

When it comes to communication around your API, it can be more art, than science. I don't think there is a precise formula for keeping people informed of what is coming down the pipes with your API. But if you keep it active, personal and informative--you can do alright.

While the Flickr API might not be in the limelight all the time, they've been doing it a while, and I can't help but cheer for the image and photo API pioneer.