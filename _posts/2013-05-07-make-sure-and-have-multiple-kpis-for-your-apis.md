---
layout: post
title: "Make Sure And Have Multiple KPIs For Your APIs"
url: 'http://apievangelist.com/2013/05/07/make-sure-and-have-multiple-kpis-for-your-apis/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/api-billionaires-club.png'
---

[<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/programmableweb/api-billionaires-club.png" alt="" width="325" align="right" />][1]

In the API space, we have to be constantly measuring and looking for signals that will help us understand where we should be focusing our resources, as part of an overall strategy. One of the ways we measure value within the world of APIs (and business) is using KPIs, or Key Performance Indicators. Using KPIs we strive to measure the Return on our Investment (ROI), as we gamble with the technology, business and politics of APIs.

One approach to quantifying the value, that has emerged from API providers, API service providers and the tech blogosphere is using the "API call". It is simple. You launch an API, so you quantify it by the number of times someone calls it. Kind of like a page view, right?

Out of this eyeball derived reality(which is silly since APIs aren't for humans), the API space has become obsessed with the number of API calls, resulting in what is known as the [API billionaires club][1]. The Billionaires Club is an elite group of tech providers who have billions of calls per month on their API. It is a pretty simple algorithm. Have API Have Billions of Requests = Your In The Billionaires Club. And if you are in the billionaires club, you are successful.  End of calculation.

To quickly get to the point of my story, let's take one of my favorite members of the API billionaires club, Netflix.  Billionaire Club Membership Shutting Down Public API = Success. It is a different variation on the whole concept of measuring API success. The news, commonly held KPIs and definition of success doesn't immediately pan out in the whole Netflix story.

Netflix, along with Twitter are both  API case studies for the history books. Both of these API stories reflect the ups and downs of the API world, and the often bipolar nature of the public API ecosystem and schizophrenic nature of the tech blogosophere. In contrast, along with Amazon Web Services, Twitter and Twilio, Netflix is a constant player in the stories I tell about success in the API sector. But at the same time, Netflix is considered to be a failure by common public APIs measurements. Are you feeling the crazy?  I do!!

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/netflix/netflix-square.png" alt="" width="200" align="right" />

As I've [covered before][2], the blogosphere tends to associate closure of the Netflix, with the ecosystem failures of Twitter. While this is an easy comparison to make, when you look further, you see a lot more going on.  Which tells me we need better ways to measure API success and failure and tell the stories around the ups and downs.

After monitoring the API space for some time now, I'm looking for signals beyond what normal bloggers, analysts and pundits are following. In this hunt, Github is becoming an ever increasing gold mine of signals.  To help demonstrate, let's take a look at the signals the [Netflix Github account][3] puts out.

  * **[Priam][4]** \- Co-Process for backup/recovery, Token Management, and Centralized Configuration management for Cassandra. (Last updated a day ago)
  * **[aminator][5]** \- A tool for creating EBS AMIs. This tool currently works for CentOS/RedHat Linux images and is intended to run on an EC2 instance. (Last updated 2 days ago)
  * **[astyanax][6]** \- A Cassandra Java Client (Last updated 2 days ago)
  * **[asgard][7]** \- Web interface for application deployments and cloud management in Amazon Web Services (AWS). Binary download: http://netflix.box.com/asgard Twitter: http://twitter.com/AsgardOSS (Last updated 3 days ago)
  * **[RxJava][8]** \- A library for composing asynchronous and event-based programs using observable sequences for the Java VM. (Last updated 4 days ago)
  * **[denominator][9]** \- (Last updated 5 days ago)
  * **[blitz4j][10]** \- Logging framework for fast asynchronous logging (Last updated 6 days ago)
  * **[SimianArmy][11]** \- Tools for keeping your cloud operating in top form. Chaos Monkey is a resiliency tool that helps applications tolerate random instance failures. (Last updated 8 days ago)
  * **[ribbon][12]** \- Ribbon is a Inter Process Communication (remote procedure calls) library with built in software load balancers. The primary usage model involves REST calls with various serialization scheme support. (Last updated 9 days ago)
  * **[frigga][13]** \- Utilities for working with Asgard named objects (Last updated 10 days ago)
  * **[curator][14]** \- ZooKeeper client wrapper and rich ZooKeeper framework (Last updated 11 days ago)
  * **[karyon][15]** \- The nucleus or the base container for Applications and Services built using the NetflixOSS ecosystem (Last updated 12 days ago)
  * **[edda][16]** \- Service to track changes in your cloud (Last updated 13 days ago)
  * **[brutal][17]** \- A multi-network asynchronous chat bot framework using twisted (Last updated 17 days ago)
  * **[archaius][18]** \- Library for configuration management API (Last updated 17 days ago)

When I pulled this data, several days ago, there are 15 separate repositories, in four separate programming languages, including Python, Java, Groovy, Scala, that have all been updated in the last 30 days.  The fact that Netflix has a Github account, has open sourced so much of their code, while also actively maintaining it all, point at some very meaningful signals that we can tune into and work to emulate.

While the number of calls against an API is a valid KPI to measure the potential success of an API, we have to have multiple KPIs when truly trying to understand the value of a company, the platform or any single API resource.  Let's not get hung up on any single KPI, let's consider as many as we can--to see what makes sense and truly defines succcess.

There is so much to learn from reading between the lines in the world of APIs.

   [1]: http://blog.programmableweb.com/2011/05/25/who-belongs-to-the-api-billionaires-club/
   [2]: http://apievangelist.com/2013/03/12/netflix-api-is-much-more-than-a-public-api/
   [3]: https://github.com/netflix
   [4]: https://github.com/Netflix/Priam
   [5]: https://github.com/Netflix/aminator
   [6]: https://github.com/Netflix/astyanax
   [7]: https://github.com/Netflix/asgard
   [8]: https://github.com/Netflix/RxJava
   [9]: https://github.com/Netflix/denominator
   [10]: https://github.com/Netflix/blitz4j
   [11]: https://github.com/Netflix/SimianArmy
   [12]: https://github.com/Netflix/ribbon
   [13]: https://github.com/Netflix/frigga
   [14]: https://github.com/Netflix/curator
   [15]: https://github.com/Netflix/karyon
   [16]: https://github.com/Netflix/edda
   [17]: https://github.com/Netflix/brutal
   [18]: https://github.com/Netflix/archaius
