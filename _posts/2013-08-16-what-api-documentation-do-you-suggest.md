---
layout: post
title: "What API Documentation Do You Suggest?"
url: 'http://apievangelist.com/2013/08/16/what-api-documentation-do-you-suggest/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/Swagger-Screenshot-1.png'
---

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/swagger/Swagger-Screenshot-1.png" alt="" width="250" align="right" />

As I spend time in Washington DC, I get a lot of questions regarding API design, deployment and management. It is quite likely my writing will evolve here at API Evangelist during the next year. You will see me quickly scrub answers that I'm giving to questions that I receive from any number of federal agencies.

One question I received today was a classic one: what are some good examples of API docs? But in this particular case it wasn't just for an API, there is also a full download of data available as well.

First, regardless of whether or not it is data download (CSV, XML, JSON) or API you need to provide a wrapper area, or portal, that will onboard users and helps them understand what you are delivering, enabling them to go from 0-60 with as little friction as possible.

This is what I have studied for the last 3 years. After looking at thousands of APIs areas, you start to see patterns. You will find [my research in the form of "building blocks" on a section of my site][1]. Even though most of my research is focused on APIs, these patterns can apply universally to data download or API delivery.

But specifically to question of what API documentation I like? I also recommend looking at:

  * [Stripe][2]
  * [Twilio][3]
  * [Parse][4]
  * [Full Contact][5]
  * [Box][6]
  * [Dwolla][7]

When looking through these make sure and take notice of how [Dwolla separates their intro page, between non-devs and devs][8]. This is a very significant concept for delivering onboarding materials for users where not everyone will be a developer.

Beyond those suggestions for API docs, here are [Thirty APIs To Look At When Planning Your AP][9]I, if you are looking for more examples of quality API areas documentation.

Another thing to consider when actually deploying specifically an API, is making your API documentation "interactive". There are several solutions for doing this right now, but the leading solution (in my opinion) is called [Swagger][10]. This is a evolution from [WADL][11], but has come a long ways since just describing a web API in XML.

Swagger is developed by [Wordnik][12], and you can view the [documentation in action on their developer site][13]. In my examples above, Full Contact uses swagger to deliver their documentation in a very elegant way. Why Swagger is important, is the fact that it doesn't just deliver elegant documentation, it makes it interactive and learning about an API a hands on experience, which increases the potential for adoption.  

The benefits of Swagger only begin with interactive documentation, it will also [generate code samples in Java, Objective-C, PHP, Python, Ruby][14] automatically. 

Just some thoughts. I hope it helps. Remember, open data and APIs only start with the download or interface. The success of your implementation really depends on the richness of the area around your data download and API.

   [1]: http://management.apievangelist.com/building-blocks.html
   [2]: https://stripe.com/docs/api
   [3]: http://www.twilio.com/docs/api/rest
   [4]: https://www.parse.com/docs/rest
   [5]: http://www.fullcontact.com/developer/docs/person/
   [6]: http://developers.box.com/docs/#folders
   [7]: https://developers.dwolla.com/dev/docs
   [8]: https://developers.dwolla.com/
   [9]: http://apievangelist.com/2012/08/08/thirty-apis-to-look-at-when-planning-your-api/
   [10]: https://developers.helloreverb.com/swagger/
   [11]: http://en.wikipedia.org/wiki/Web_Application_Description_Language
   [12]: http://www.wordnik.com/
   [13]: http://developer.wordnik.com/docs.html
   [14]: https://github.com/wordnik/swagger-codegen
