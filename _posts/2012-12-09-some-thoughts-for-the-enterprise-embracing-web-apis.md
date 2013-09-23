---
layout: post
title: "Some Thoughts For the Enterprise Embracing Web APIs"
url: 'http://apievangelist.com/2012/12/09/some-thoughts-for-the-enterprise-embracing-web-apis/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/enterprise-business.jpg'
---

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/enterprise-business.jpg" alt="" width="250" align="right" />

At the Gartner AADI Conference in Las Vegas, NV last week I discussed the _"grass-roots web API movement"_ with quite a few enterprise folks. Walking through the exhibit floor, where I did my [building blocks of an API workshop][1], I noticed the signage and discussions were all focused on APIs.

During my discussions with multiple enterprise developers, analysts, architects and executives, one question seemed to come up a lot: **_Didn’t we do all of this 10 years ago? What is different this time around?_**

With a strong focus on the technology of web services, many in the enterprise fail to see the difference between SOA and API. In an effort to better tell stories in this area, I wanted to revisit the SOAP vs. REST argument, and refresh my thoughts.  So I got to work pulling up old stories, and while conducting my research I noticed the same patterns I see in the REST debates--a heavy focus on the technical, with only a few discussions of the business and politics of web services.

If you are new to the SOAP vs. REST debate, let me get you up to speed. [Wikipedia defines SOAP][2] as:

> _SOAP, originally defined as Simple Object Access Protocol, is a protocol specification for exchanging structured information in the implementation of Web Services in computer networks._

> _SOAP was designed as an object-access protocol in 1998 by Dave Winer, Don Box, Bob Atkinson, and Mohsen Al-Ghosein for Microsoft, with a specification of SOAP currently maintained by the XML Protocol Working Group of the World Wide Web Consortium (W3C)._

> _After SOAP was first introduced, it became the underlying layer of a more complex set of Web Services, based on Web Services Description Language (WSDL) and Universal Description Discovery and Integration (UDDI)._

SOAP, XML and [Web Services][3] are all part of earlier approach to APIs which is widely considered to be called [Service Oriented Architecture][4] (SOA). While SOA is still used in enterprise environments, it is considered in open developer circles to have been a failure in comparison to API efforts in the more grassroots, popular web API approach employed by companies like Flickr, Twitter and Amazon.

I will spare you much of technical detail of the SOAP vs. REST debate, but the the main advantages of a web API approach are:

  * Simple and Lightweight
  * Human Readable Results
  * Easy to Build and Consume

The SOAP advantages are:

  * Rigid, Well Defined and Adhering to a Contract
  * Wide Variety of Development tools
  * Agreed Upon Standard

SOAP is a very well defined, strict technical, industry defined set of rules for approaching APIs. To the enterprise, SOAP and a SOA approaches appears to be the proper solution for the exchange of structured information.

But around 2003, outside the enterprise, we started seeing a shift in how developers viewed web services. According to [Tim O’Reilly of O’Reilly Media][5]:

> _Amazon has both SOAP and REST interfaces to their web services, and 85% of their usage is of the REST interface. Despite all of the corporate hype over the SOAP stack, this is pretty compelling evidence that developers like the simpler REST approach._

Over the course of the next nine years we see this trend continue with [REST JSON][6] growing in dominance, wrestling control over web services and the term API from a more SOAP XML approach.

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/enterprise-business-1.jpg" alt="" width="250" align="right" />

After re-reading much of the SOAP vs. REST debate this weekend, I see the same as with the REST debate, where much of the discussion is technical. But there are some great statements on what contributee to the success of API over SOA. From [Supun Kamburugamuva on Life of a Software Engineer blog][7]:

> _REST as a framework gives the developers exactly that. The freedom to innovate. Developers love that. As a framework REST introduces very few rules. Most of them are not even rules. Rather they are soft guidelines. So building a proper powerful REST API is an Art and a challenging task. In my opinion this makes it cool._

> _This is completely opposite to SOAP. SOAP gives the developer all the rules. First thing about SOAP is you get a SOAP envelope where you have to put your data according to some rules. So from start to end the system is pretty well defined. There are standards for doing even the simplest things. Top of all this SOAP is very complex to understand. So in my opinion SOAP doesn't give user the nuts and bolts to innovate. Instead it gives a half baked solution that user has to obey. I guess not all developers like to bog down by rules and they don't like to learn that kind of rules as well._

Martijn Linssen at CloudAve also had a great statement:

> _SOAP was originally introduced to and by Microsoft, and was one in a range of futuristic machine-to-machine self-describing protocols. Needless to say, the world wasn’t ready then, nor is it now. Current implementations of SOAP are arbitrary, proprietary, bi-lateral human agreements at best. In their worst form, SOAP implementations are dictated by governments and other bodies of power and bring nothing else to the other party but a cumbersome and hard-coupled interface_

In my opinion SOAP vs. REST is about Structure vs. Simplicity, Defined vs. Organic, Control vs. Open. The differences aren’t just technical. As technologists we like to see things through a certain lense, add in capitalists and we can really have our blinders on.

There are a lot of lessons in the modern web API movement that the enterprise can learn from. SOA and API have a lot of parallels in trying to facilitate the exchange of structured information between applications, but where they begin to differ is that SOA was born within industry and within an enterprise. API was born on the open Internet, where it was able to get the oxygen it needed to grow.

My advice to the enterprise is when you look at adopting a web API approach over SOA approach, you look beyond just the technology and vendor solutions--you need to look at a lot of the more human elements that exist in the business and politics of APIs. Consider essential elements like:

  * **Simplicity** \- Keep things small, modular and intuitive
  * **Access** \- You should be widening access to your resources, not ever limiting
  * **Openness** \- While not everything should be 100% open, be as open as possible
  * **Transparency** \- Provide insight into operations and your roadmap allowing consumers to operate in alignment
  * **Communication** \- Two way communication between you and your consumers
  * **Privacy** \- Protect the privacy of your consumers
  * **Ownership** \- Be open to alternative licensing and ownership of content and data that is favorable to consumers
  * **Legal** \- Be as open as you can be with copyright, patents and trademark in API initiatives
  * **Terms** \- Establish terms of use that favor your business, but also the interests of consumers
  * **Revenue** \- Acknowledge the monetization needs of your consumers

These are just a few of the key ingredients in the grassroots recipe that so many companies are following when deploying web APIs. A balance of technical, business and politics has been found and is currently being explored in the web API movement. You can see examples of both success and failure in these areas, with APIs like Amazon and Twitter. Both API providers have found success technologically, but took different approaches to business and politics, delivering very different results within their respective developer ecosystems.

There is a reason web APIs have found success on the open Internet. Web APIs require a certain amount of “open” to be present in not just the technical, but also the business and political layers. When embracing APIs, make sure you understand the full scope of why API is different than SOA--then internalize this difference and make it part of how you conduct business internally, with partners and the public on the open Internet.

Some other reading on this subject:

  * [REST][8], Wikipedia
  * [SOAP][2], Wikipedia
  * [Web Service][3], Wikipedia
  * [SOAP vs. REST][9], Steve Francia
  * [History of REST, SOAP, POX and JSON Web Services][10] 
  * [REST vs. SOAP – The Right WebService][11], Tarandeep Singh
  * [SOAP, REST and Occam’s Razor][12], Daniel Silva
  * [1 in 5 APIs Say “Bye XML”][6] \- Adam DuVander
  * [REST vs SOAP Adoption - A Perspective][7] \- Supun Kamburugamuva
  * [How and why REST will beat SOAP][13], Martijn Linssen
  * [The Next Wave? Enterprises Moving SOAP to REST][14], Adam DuVander
  * [REST vs. SOAP at Amazon][5], Tim O'Reilly
  * [SOAP vs REST: The war between simplicity and standards][15], Lori MacVittie

   [1]: /2012/11/30/my-api-building-blocks-workshop-with-intel-at-the-gartner-aadi-conference/
   [2]: http://en.wikipedia.org/wiki/SOAP
   [3]: http://en.wikipedia.org/wiki/Web_Service
   [4]: http://en.wikipedia.org/wiki/Service-oriented_architecture
   [5]: http://www.oreillynet.com/pub/wlg/3005
   [6]: http://blog.programmableweb.com/2011/05/25/1-in-5-apis-say-bye-xml/
   [7]: http://supunk.blogspot.com/2012/08/rest-vs-soap-adoption-perspective.html
   [8]: http://en.wikipedia.org/wiki/REST
   [9]: http://spf13.com/post/soap-vs-rest/
   [10]: http://www.servicestack.net/mythz_blog/?p=154
   [11]: http://geeknizer.com/rest-vs-soap-using-http-choosing-the-right-webservice-protocol/
   [12]: http://silvanolte.com/blog/2009/12/01/soap-rest-and-occams-razor/
   [13]: http://www.cloudave.com/22132/how-and-why-rest-will-beat-soap/
   [14]: http://blog.programmableweb.com/2012/03/22/the-next-wave-enterprises-moving-soap-to-rest/
   [15]: https://devcentral.f5.com/blogs/us/soap-vs-rest-the-war-between-simplicity-and-standards
