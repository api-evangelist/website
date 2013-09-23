---
layout: post
title: "A Single Provider for High Quality Transit Data and APIs"
url: 'http://apievangelist.com/2011/09/26/a-single-provider-for-high-quality-transit-data-and-apis/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/jeppesen-logo-400.jpg'
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/jeppesen/jeppesen-logo-400.jpg" alt="" width="275" align="right" />][1]

I wrote about the [need for more Transit APIs][2] a couple weeks ago, and the opportunity for some company or organization to step up and coordinate transit APIs on a global, country, regional and local level. Also the opporunity for developers to provide local resources for building applications, "acquiring" of local data, understanding local constraints, and be the overall contact for a specific locale.

To me, there appears to be a hunger for transit data, and there is a major gap in how this "public data" is being made available for developers to build websites, web and mobiles apps, that businesses and commuters can use. The opportunity is so big, that tech savvy commuters are stepping up, scraping data, and building transit APIs and applications themselves.

I had a lot of people contact me after my post, but one clear player emerged, that appears to be just the company I was looking for. That company is [Jeppesen][3], a Boeing funded company that has a new service called the [Jeppesen Journey Planner API][4].

Jeppesen has developed a very robust set of transit APIs, providing:

  * **Public Transit Journey Plans** \- Request multimodal public transit journey plans
  * **Polyline Trip Details** \- Draw the journey plans on a map
  * **Stop Locations** \- Locate all the public transit stops within an area
  * **Stop Timetable** \- Obtain a list of departures (or arrivals) from a public transit stop
  * **Walk Journey Plans** \- Request walking journey plans between locations
  * **Service Provider** \- Identify the public transit service providers in an area
  * **Fares** \- Find out the cost of the journey (when transit fare information is available)
  * **Trip Timetable** \- Discover all the stopping points for a specific trip

Jeppesen is aggregating data from transit agencies around the world, including 23 regions in the US, and locations in Australia, New Zealand, Canada and the UK, into a single set of web services. Jeppesen has enough markets to be a viable option, and they are looking to add more markets in the near future.

Their pricing is very affordable and is broken down by stop timetable and journey planning requests. Even though the API currently targets the enterprise and businesses, it is low priced enough that individual developers could use to build applications, that they could monetize and build a viable business around.

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/jeppesen/Jeppesen-Journey-Planner.png" alt="" width="325" align="right" />][1]

Jeppesen has spent the last 18 months developing the transit API, looking to provide high quality data aggregation for developers. The API has just been made available for production and has partners in Australia and the UK building applications on the platform.

The Jeppesen Journey Planner API comes in both SOAP and RESTful flavors, with C#, Java and Python code samples. The API is brand new so it lacks other code samples, mobile SDKs, and other community aspects that we are used to with more mature APIs. However, the API is very well done, walking you through an overview of the API, its features, and pricing--while also providing very simple and complete API documentation.

[Registration for the transit API][5] is not self-service, but they offer a free trial and I had my API key within 24 hours of submitting the request form.

There are still a lot of questions to be answered regarding how Jeppesen will incentivize partners and developers to build applications around the API, will there be revenue sharing opportunities, and what type of local, regional outreach and support there will be. But I'm sure these questions will get answered in time.

For now, Jeppesen shows a lot of potential to be transit API player I was looking for. I think they have a lot of work ahead of them, to meet the transit data needs of enterprise and businesses, while also satisfying the needs of local commuters, especially those very tech savvy ones we see demanding high quality access to their areas transit data.

   [1]: http://ww1.jeppesen.com/main/corporate/land/journey-planning/index.jsp
   [2]: /2011/09/11/the-need-for-more-transit-apis/ (need for more transit API)
   [3]: http://ww1.jeppesen.com/main/corporate/ (Jeppesen)
   [4]: http://ww1.jeppesen.com/main/corporate/land/journey-planning/index.jsp (Jeppesen Journey Planner API)
   [5]: http://ww1.jeppesen.com/main/corporate/land/journey-planning/signup.jsp (Registration for the transit API)
