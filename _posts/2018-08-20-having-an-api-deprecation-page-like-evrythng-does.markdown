---
published: true
layout: post
title: 'Having An API Deprecation Page Like EVRYTHNG Does'
date: 2018-08-20T09:00:00.000Z
tags:
  - API Evangelist
  - Deprecation
  - Communication
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/catacombs_blue_circuit_3.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>The API providers I talk to regularly are rarely proactive when it comes to addressing API deprecation. Most API providers aren't thinking about shutting down any service they deliver until they've actually encountered the need down the road. Many just begin their API journey, assuming their APIs will be a success, and they will have to support every version forever. However, once they encounter what it will take to support older versions, they begin to change their tune, something that often comes as an unexpected surprise to consumers.

Shutting down old APIs will never be easy, but the process can be made easier with a little proactive communication. One example of this practice in action can be found over at [the Internet of Things provider Evrythng, with their API deprecation page](https://developers.evrythng.com/docs/deprecation). Which provides a pretty simple layout for an API deprecation page, beyond just a title and description of what the future might hold.

_API Status_

_The following status labels are applicable to APIs, features, or SDK versions depending on their current support status:_

_- Preview - May change at any time.
- Stable - Fully released and stable. Will not change at short notice.
- Deprecated - No longer supported (and may have been replaced), and may be removed in the future at an announced date. Use not encouraged.
- Removed - Removed, and no longer supported or available._

_Communication_

_When a deprecation is announced, the details and any relevant migration information will be available on the following channels:_

_- The Developer Blog.
- The @evrythngdev Twitter account.
- The relevant feature page on the Developer Hub.
- Enterprise customers may receive information by email to their specified EVRYTHNG contact, if applicable._

_Customers using one our SLAs can read [the General section](https://evrythng.com/legal/sla/) for more information._

Evrythng provides us with some important building blocks for using as part of our overall API deprecation strategy. Something that EVERY API provide should be considering as they prepare to launch a new API. API deprecation shouldn't be an afterthought, and if we communicate open and honestly about it from the beginning, our API consumers will be more forgiving. Surprising consumers down the road is the quickest way to piss people off, and get the tech blogosphere publishing those pitchfork and torches type of stories we see so often about API providers.

I just finished sharing some API deprecation awareness as part of the API strategy for a federal government agency--they just hadn't had an open discussion about it. API deprecation is one of those uncomfortable subjects, we all have to get used to discussing early on, whether we like it or not. It is something that will always be difficult, and leave some API consumers unhappy, but if done well, it can help reduce a lot of friction. You can visit [my API deprecation research and storytelling](http://deprecation.apievangelist.com/) for more examples of how to do it right, and how you can avoid doing it wrong--bringing this important subject out into the open.
