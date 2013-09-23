---
layout: post
title: "Netflix API Is Much More Than A Public API"
url: 'http://apievangelist.com/2013/03/12/netflix-api-is-much-more-than-a-public-api/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/netflix-square.png'
---

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/netflix/netflix-square.png" alt="" width="200" align="right" />

Netflix has [entered the final stages of shuttering its public API last week][1]. Its been coming for a while now, [starting in June of 2012][2], and now is official with the platform no longer accepting new API registrations.

After reading about the changes to the Netflix Public API program on their blog, and hearing much of the news in response, [everyone seems to file this away, along with the Twitter API][3]\--just another API platform screwing over its developers.

As I do, I wanted to take a step back, look at the bigger picture and try understand what happened.  On [October 1st 2008, Netflix launched their public API][4], and they appear to have done everything right. They had a blog, [solicited code samples from developers][5], [accepted application submissions][6] and even [showcased the developers apps in the gallery][7]. Netflix would even help [promote your app to Netflix subscribers][8] and [threw hackathons][9]. The Netflix API team worked to [improve API performance][10], communicate regularly, but really nothing that amazing happened.

There were applications like [InstaWatcher][11] and [WhichFlicks][12] (among others) developed on the API, but as Daniel Jacobson puts it, [a thousand flowers didn’t bloom][13]. In these situations its easy to blame the API provider, but developers didn’t really step up and build anything that innovative and cool. So is this a failure of Netflix? A failure of developers to innovate? Or could it possibly be a third: failure of the API vision?

I would say the demise of the Netflix public API is equal part Netflix and the developer, and just the nature of the industry it exists in. It didn’t take me long to look through the Netflix API blog, so I can tell they didn’t put alot into evangelizing the API. But I really can’t find any innovation that occurred by developers as part of it, so I think us devs have to share some of the responsibility as well.

Several of the blog posts covering the news last week, [compared this to Twitter][14] which I think for the untrained eye of the mainstream tech blogosphere, this is easy to do. But Twitter is user generated content, via one of the newest types of content platforms, and Netflix is heavily licensed and policed content from one of the oldest content platforms. I think expecting public API success from Netflix and / or developers was a lot to ask.

I love and believe in APIs, but I’m not delusional enough to think they will work magically everywhere they are applied. However, even with the closing of the public Netflix API, I consider Netflix is an API success story. Look what they’ve done with their internal and partner APIs. They’ve managed to scale not just from the data center to the cloud, but globally and across 800 devices--while also [sharing this knowledge and wisdom with the public][15] via their blog:

  * [Public Continuous Integration Builds for our OSS Projects][16]
  * [Introducing the first NetflixOSS Recipe: RSS Reader][17]
  * [Karyon: The nucleus of a Composable Web Service][18]
  * [Denominator: A Multi-Vendor Interface for DNS][19]
  * [Announcing EVCache: Distributed in-memory datastore for Cloud][20]
  * [Netflix Queue: Data migration for a high volume web application][21]
  * [Functional Reactive in the Netflix API with RxJava][22]
  * [Announcing Ribbon: Tying the Netflix Mid-Tier Services Together][23]
  * [NetflixGraph Metadata Library: An Optimization Case Study][24]
  * [Optimizing the Netflix API][25]

If that wasn't enough, they are also [open sourcing much of the technology][26] behind their approach:

  * [eureka][27] \- AWS Service registry for resilient mid-tier load balancing and failover
  * [RxJava][28] \- a library for composing asynchronous and event-based programs using observable sequences for the Java VM
  * [Governator][29] \- A library of extensions and utilities that enhance Google Guice to provide: classpath scanning and automatic binding, lifecycle management, configuration to field mapping, field validation and parallelized object warmup
  * [Priam][30] \- Co-Process for backup/recovery, Token Management, and Centralized Configuration management for Cassandra
  * [edda][31] \- Service to track changes in your cloud recipes-rss - RSS Reader Recipes that uses several of the Netflix OSS components
  * [astyanax][32] \- Cassandra Java Client
  * [karyon][33] \- The nucleus or the base container for Applications and Services built using the NetflixOSS ecosystem
  * [netflix-graph][34] \- Compact in-memory representation of directed graph data
  * [asgard][35] \- Web interface for application deployments and cloud management in Amazon Web Services (AWS)
  * [Hystrix][36] \- Hystrix is a latency and fault tolerance library designed to isolate points of access to remote systems, services and 3rd party libraries, stop cascading failure and enable resilience in complex distributed systems where failure is inevitable
  * [servo][37] \- Netflix Application Monitoring Library
  * [frigga][38] \- Utilities for working with Asgard named objects

When measuring the success or failures of API initatives, we can't use the same yardstick in all scenarios. When you look at the knowledge, wisdom and code that has come out of Netflix, there is no way you can say their API initiative is anything but a success. I don’t see see Netflix as a case study in how to stream movies over the web via public APIs, but a deeply important experiment in how to deliver licensed content to over 800 devices, via the next generation of APIs.  Something that probably isn't an edge case, it actually represents where we all might be headed in the near future.

Let’s not get caught up in the recent deprecation of the Netflix public API.  There is so much going on!  Let's get studying some of the knowledge and technology coming out of Netflix. I know its my motivation for writing this post, and doing this research.

   [1]: http://developer.netflix.com/blog/read/Changes_to_the_Public_API_Program
   [2]: http://developer.netflix.com/blog/read/Upcoming_Changes_to_the_Netflix_API_Program
   [3]: http://www.rethink-wireless.com/2013/03/11/netflix-public-api-program-retired.htm
   [4]: http://readwrite.com/2008/09/30/netflix_api_launches_tomorrow
   [5]: http://developer.netflix.com/blog/read/Let_Us_Know_About_your_Libraries
   [6]: http://developer.netflix.com/blog/read/App_Gallery_Open_for_Developer_Submissions
   [7]: http://developer.netflix.com/blog/read/Finding_nice_applications_via_the_Netflix_App_Gallery
   [8]: http://developer.netflix.com/blog/read/Promote_Your_App_to_Netflix_Subscribers
   [9]: http://developer.netflix.com/blog/read/Untitled_1
   [10]: http://developer.netflix.com/blog/read/API_Performance_Improvements
   [11]: http://instantwatcher.com/
   [12]: http://www.whichflicks.com/
   [13]: http://www.slideshare.net/michaelhart2/api-strategy-evolution-at-netflix
   [14]: http://www.engadget.com/2013/03/08/netflix-changes-its-current-api-program-by-ending-it-will-no/
   [15]: http://techblog.netflix.com/
   [16]: http://techblog.netflix.com/2013/03/public-continuous-integration-builds.html
   [17]: http://techblog.netflix.com/2013/03/introducing-first-netflixoss-recipe-rss.html
   [18]: http://techblog.netflix.com/2013/03/karyon-nucleus-of-composable-web-service.html
   [19]: http://techblog.netflix.com/2013/03/denominator-multi-vendor-interface-for.html
   [20]: http://techblog.netflix.com/2013/02/announcing-evcache-distributed-in.html
   [21]: http://techblog.netflix.com/2013/02/netflix-queue-data-migration-for-high.html
   [22]: http://techblog.netflix.com/2013/02/rxjava-netflix-api.html
   [23]: http://techblog.netflix.com/2013/01/announcing-ribbon-tying-netflix-mid.html
   [24]: http://techblog.netflix.com/2013/01/netflixgraph-metadata-library_18.html
   [25]: http://techblog.netflix.com/2013/01/optimizing-netflix-api.html
   [26]: https://github.com/netflix
   [27]: https://github.com/Netflix/eureka
   [28]: https://github.com/Netflix/RxJava
   [29]: https://github.com/Netflix/governator
   [30]: https://github.com/Netflix/Priam
   [31]: https://github.com/Netflix/edda
   [32]: https://github.com/Netflix/astyanax
   [33]: https://github.com/Netflix/karyon
   [34]: https://github.com/Netflix/netflix-graph
   [35]: https://github.com/Netflix/asgard
   [36]: https://github.com/Netflix/Hystrix
   [37]: https://github.com/Netflix/servo
   [38]: https://github.com/Netflix/frigga
