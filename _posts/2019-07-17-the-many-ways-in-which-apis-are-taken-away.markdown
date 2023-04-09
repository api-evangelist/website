---
published: true
layout: post
title: 'The Many Ways In Which APIs Are Taken Away'
date: 2019-07-17T09:00:00.000Z
tags:
  - API Evangelist
  - Deprecation
  - Reliability
image: >-
  https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/catacombs-catacombs-copper-circuit.jpg
---

APIs are notorious for going away. There are so many APIs that disappear I really stopped tracking on it as a data point. I used keep track of APIs that were shuttered so that I could play a role in the waves of disgruntled pitchfork mobs rising up in their wake--it used to be a great way to build up your Hacker News points! But, after riding the wave a couple hundred waves of APIs shuttering, you begin to not really not give a shit anymore—-growing numb to it all. API deprecation grew so frequent, I wondered why anyone would make the claim that once you start an API you have to maintain it forever. Nope, you can shut down anytime. Clearly.

In the real world, APIs going away is a fact of life, but rarely a boolean value, or black and white. There are many high profile API disappearances and uprising, but there are also numerous ways in which some API providers giveth, and then taketh away from API consumers.:

- **Deprecation** - APIs disappear regularly both communicated, and not so communicated, leaving consumers scratching their heads.
- **Disappear** - Companies regularly disappear specific API endpoints acting like they were never there in the first place.
- **Acquisition** - This is probably one of the most common ways in which high profile, successful APIs disappear.
- **Rate Limits** - You can always rate limit away users make APIs inaccessible, or barely usable for users, essentially making it go away.
- **Error Rates** - Inject elevated error rates either intentionally or unintentionally can make an API unusable to everyone or select audience.
- **Pricing Tiers** - You can easily be priced out of access to an API making it something that acts just like deprecating for a specific group.
- **Versions** - With rapid versioning, usually comes rapid deprecation of earlier versions, moving faster than some consumers can handle.
- **Enterprise** - APIs moving from free or paid tier, into the magical enterprise, “call us” tier is a common ways in which APIs go away.
- **Dumb** - The API should not have existed in the first place and some people just take a while to realize it, and then shut down the API.

I’d say Facebook, Twitter, and Google shutting down, or playing games in any of these areas have been some of the highest profile. [The sneaky shuttering of the Facebook Audience Insight API was one example](http://apievangelist.com/2017/12/04/facebook-quietly-deprecates-the-audience-insight-api-used-to-automate-targeting-during-the-election/), but didn’t get much attention. I’d say that [Parse is one that Facebook](http://apievangelist.com/2017/03/28/i-think-the-parse-twitter-page-sums-it-up-pretty-well/) handled pretty well. Google did it with Google+ and Google Translate, but then brought back it with a paid tier. LinkedIn regularly locks down and disappears its APIs. Twitter has also received a lot of flack for limiting, restricting, and playing games with their APIs. In the end, many other APIs shutter after waves of acquisitions, leaving us with as my ex-wife says--“nothing nice”!

Face.com, Netflix, 23andMe, Google Search, ESPN, and others have provided us with lots of good API deprecation stories, but in reality, most APIs go aware without much fanfare. You are more likely to get squeezed out by rate limits, errors, pricing, and other ways of consciously making an API unusable. If you really want to understand the scope of API deprecation visit the leading deprecated API directory ProgrammableWeb—-they have thousands of APIs listed that do not exist anymore. In the end it is very difficult to successfully operate an API, and most API providers really aren’t in it for the long haul. The reasons why APIs stay in existence are rarely a direct result of them being directly financially viable. Developers squawk pretty loudly when the free API they’ve been mooching off of disappears, but there are many, many, many other APIs that go away and nobody notices, or nobody talks about. In the world of APIs there are very few things you can count on being around for very long, and you should always have a plan B and C for every API you depend on.
