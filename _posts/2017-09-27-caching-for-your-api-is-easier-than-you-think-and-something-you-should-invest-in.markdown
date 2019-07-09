---
published: true
layout: post
title: >-
  Caching For Your API Is Easier Than You Think And Something You Should Invest
  In
date: 2017-09-27T11:00:00.000Z
tags:
  - API Evangelist
  - Caching
  - Performance
  - Reliability
  - Politics of APIs
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/internet-gauages-3.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/internet-gauages-3.jpg" align="right" width="40%" style="padding: 15px;" /></p>I'm encountering more API providers who have performance and scalability concerns with their APIs, who are making technical procurement decisions (gateways, proxies, etc) based upon these challenges, but have not invested any time or energy into planning and optimization of caching for their existing web servers that are delivering their APIs. Caching is another aspect of HTTP that I keep finding folks have little or no awareness of, and do not consider more investment in it to assist them in alleviating their scalability and performance concerns.

There was a meeting I attended a couple weeks back where an API implementation was concerned about a new project for bulk loading and syncing of data between multiple external systems and their own, because of the strain it put on their database. Citing that they received millions of website, and API calls daily, they said they could not take the added load on their already strained systems during the day, limiting this type of activity to a narrow window at night. I began inquiring regarding caching practices in place on web, and API traffic, and they acknowledged that they new of no such activity or practices in place. This isn't uncommon in my experiences, and I regularly encounter IT groups who just don't have the time and HTTP awareness to implement any coherent strategy--this particular one just happened to admit it.

[My friends over at the API Academy have a great post on caching for RESTful and Hypermedia APIs](http://www.apiacademy.co/how-to-http-caching-for-restful-hypermedia-apis/), so I won't be addressing the details of HTTP, and how you can optimize your APIs in this way. API caching isn't an unproven technology, and it is a well known aspect of operating on the web, but it does take some investment and awareness. Like API design in general, you have to get to know the resources you are serving up, understand how your consumers are putting these resources to work, and adjust, dial-in, and tweak your caching strategy. It is something that gets incrementally harder, the more time zones you operate in, but with some investment you can significantly increase the scalability of your APIs, the performance of properly cached paths, and do more with less resources. Scaling the size of your server isn't always the first sensible thing you should be doing, a coherent caching strategy will be a much wiser and cost-effective approach in the long run.

A lack of API caching strategy amongst my clients and readers has a damaging effect on API operations. However, I'd say the most damage done isn't by the lack of a strategy, it is the reverberating decisions made around the inability to properly scale, and deliver the performance API clients are needing. I see many technology procurement decisions being made where scalability and performance are a major part of the conversation and decision making process. Where conversations around API caching have never occurred. This is just lazy. This is just ignoring one of the key tenets of what makes the web work. This is just investing in technical debt, over making sensible architectural decisions, and spending the time to get to know the resources you are serving up, and how your customers are using them. Learning about HTTP, and caching does take some investment and planning, but it is nowhere the investment and planning that will be required to unwind the technical debt you've acquired made from the other bad technology purchasing decisions you've made along the way.
