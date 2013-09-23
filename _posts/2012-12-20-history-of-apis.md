---
layout: post
title: "History of APIs"
url: 'http://apievangelist.com/2012/12/20/history-of-apis/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/Tag-Cloud-History-of-APIs.png'
---

[<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/Tag-Cloud-API-History.png" alt="" width="225" align="right" />][1]

The history of APIs is something I discuss a lot.  The history of modern web APIs is something I include in all my talks, and I'm always surprised by how little people understand some of the more popular APIs that got us to where we are at.

To further support this area, I've launched a [History of APIs][1] section where I've hung the stories I've already done in this area, and will be looking to dig up the history on other APIs that are shaking things up.

When I'm talking to people about APIs, the term APIs can mean many different things. Sometimes it means hardware APIs, or the Java API or various other technical incarnations. Right now when you hear the term API, it probably means web API or an API built using REST, running on the same infrastructure the World Wide Web runs on.

When it comes to APIs, I strongly feel that to understand where we are, we need to understand the short, modern history of the web APIs. There are several patterns to why the modern web API movement has worked, that I think you can take home and use in your own API strategy.

##  Commerce

While modern web APIs were officially born with [Roy Fieldings dissertation Architectural Styles and the Design of Network-based Software Architectures in 2000][2]\--Web APIs first appeared in the wild with the [introduction of Salesforce][3] on February 7th, when the company officially launched its API at the IDG Demo 2000 conference. Salesforce was an enterprise-class, web-based, sales force automation as a "Internet as a service", with XML APIs were part of Salesforce.com from day one.

[<img src="http://kinlane-productions.s3.amazonaws.com/salesforce/salesforce-original-web-site.png" alt="" width="400" /> ][3]
**[Salesforce**][3]** **

Later in the year, on November 20, 2000, [eBay launched the eBay Application Program Interface (API)][4], along with the eBay Developers Program--which was originally rolled out to only a select number of licensed eBay partners and developers.

[<img src="http://kinlane-productions.s3.amazonaws.com/ebay/ebay-developer-program-history.png" alt="" width="400" /> ][4]
**[Ebay**][4]

Then on July 16, 2002, [Amazon launched Amazon.com Web Services][5] allowing developers to incorporate Amazon.com content and features into their own web sites. Amazon.com Web Services (AWS) allowed third party sites to search and display products from Amazon.com in an XML format.

[<img src="http://kinlane-productions.s3.amazonaws.com/amazon/Amazon-Web-Services-News-Release.png" alt="" width="400" /> ][5]
**[Amazon E-Commerce**][5]

The modern Web API movement was kicked off. But for some reason it didn't gain the momentum we see today, whether it was due to the "dotcom" bubble bursting or other things werent quite ready--web APIs wouldn't get traction until things got social.

##  Social

In February 2004 the popular photo sharing site Flickr launched. Six months later [they launched their now infamous API][6], and six months after that, they were acquired by Yahoo. The launch of the RESTful API helped Flickr quickly become the image platform of choice for the early blogging and social media movement by allowing users to easily embed their Flickr photos into their blogs and social network streams. While allowing Flickr to focus on a [new approach to business development using web APIs][7].

[<img src="http://kinlane-productions.s3.amazonaws.com/flickr/flickr-beta.png" alt="" width="400" /> ][6]
**[Flickr**][6]

Then on August 15th 2006, [Facebook launched its long-awaited development platform and API][8]. Version 1.0 of the Facebook Development Platform allowed developers access to Facebook friends, photos, events, and profile information for Facebook.

[<img src="http://kinlane-productions.s3.amazonaws.com/facebook/Facebook-Developer.png" alt="" width="400" /> ][8]
**[Facebook**][8]

One month later on September 20, 2006 [Twitter introduced the Twitter API to the world][9]. Much like the release of the eBay API, Twitter's API release was in response to the growing usage of Twitter by those scraping the site or creating rogue APIs.

[<img src="http://kinlane-productions.s3.amazonaws.com/twitter/Twitter-Introducing-The-Twitter-API.png" alt="" width="400" /> ][9]
**[Twitter**][9]

At the same time Facebook and Twitter were playing with the social powers of web APIs, Google was exploring the power of web APIs supporting embeddable tools and apps. The [Google Maps API launched was just shy of 6 months after the release of Google Maps as an application][10], and was in direct response to the number of rogue applications developed that were hacking the application. Google Maps was immediately so popular that developers hacked the JavaScript interface and developed application such as housingmaps.com and chicagocime.org.

[<img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/trends/google-maps.png" alt="" width="400" /> ][10]
**[Google Maps**][10]

At this point web APIs were showing the power of the Internet when it came to sharing, making things embeddable and social. Web APIs still were perceived as "hobby" by mainstream business. You couldn't take care of business...yet.

##  Cloud Computing

As APIs were generating social buzz across the Internet, Amazon saw the potential of an [RESTful approach to business][11], [internalized and saw APIs in a way that nobody had seen them before][12]\--giving re-birth to an Amazon Web Services that was much, much more than just e-commerce.

In March, 2006 Amazon launched a new web service, something completely different from the Amazon bookseller and e-commerce site we've come to know. This was a new endeavor for Amazon: a storage web service called [Amazon S3][13]. Amazon S3 which provided a simple interface that can be used to store and retrieve any amount of data, at any time, from anywhere on the web. It gives developers access to the same highly scalable, reliable, fast, inexpensive data storage infrastructure that Amazon uses to run its own global network of websites.

[<img class="c2" src="http://kinlane-productions.s3.amazonaws.com/AWS_LOGO_CMYK.jpg" alt="" width="300" align="center" />][13]

Six month later, shortly after launching Amazon S3, Amazon followed with a new cloud computing service dubbed [Amazon EC2][14] or Elastic Compute Cloud. Amazon EC2 provided resizable compute capacity in the cloud, allowing developers to launch different sizes of virtual servers within Amazon data centers. Just like its predecessor Amazon S3, Amazon EC2 was just a RESTful API. Amazon wouldn't launch a web interface for another three years.

With cloud computing, web APIs got real. You could now deploy global infrastructure using APIs. It wasn't just about social fun anymore, you could actually run your business using APIs.

Even with this new found power of API driven cloud computing, it would take one more essential ingredient before web APIs were ready for the prime time.

##  Mobile

With everyone focused on social and the cloud, a new device emerged, and much like social and cloud, would prove to be a game changer. In June of 2009 Apple launched the iPhone 3G, the App Store began allowing iPod Touch and iPhone owners to download applications through the iTunes desktop software or the App Store on their iPhones--opening up entirely new world of mobile applications, one that APIs would be the driving force.

Soon after the launch of the iPhone, in March 2009 [Foursquare launched][15] at the SXSW interactive festival in Austin, TX. Foursquare was a location-based mobile platform that makes cities more interesting to explore, by checking in via a smartphone app or SMS, users share their location with friends while collecting points and virtual badges. This new type of mobile app, utilized APIs to allow developers to deliver a new generation of location aware, API driven applications, feeding the growing app economy.

[<img src="http://kinlane-productions.s3.amazonaws.com/foursquare-icon-large.jpg" alt="" width="200" /> ][15]
**[Foursquare**][15]

The mobile evolution of the Internet was under way, and the following year on October 6, 2010,[Instagram launched its photo-sharing iPhone application][16]. Less than three months later, it had one million users. Kevin Systrom the founder of Instagram focused on delivering a powerful, but simple iPhone app that solved common problems with the quality of mobile photos and users' frustrations with sharing.

[<img src="http://kinlane-productions.s3.amazonaws.com/instagram.PNG" alt="" width="290" /> ][16]
**[Instagram**][16]

Immediately many users complained about the lack of central Instagram web site or an API, with Instragram remaining firm on focusing its energy on the core iPhone application. In December a developer name Mislav Marohni? took it upon himself to reverse engineer how the iPhone app worked, and [built his own unofficial Instagram API][17] on top of private Instagram APIs. By [January Instagram shut down the rogue API, announcing that it was building one of its own][18].

The appetite for API resources to drive mobile has only grown with the introduction of the iPad tablet and the growth of the Android and Windows mobile platforms.

Mobile was the finalize piece of the digital strategy puzzle, which included commerce, social and cloud--all required before the original vision of web APIs could be realized.

##  Conclusion

Web APIs got their start in early e-commerce on the Internet, but without social, a scalable cloud backend and a ubiquitous mobile devices--APIs weren't ready for prime time. In 2012, we reached that point.

Every company needs a healthy digital strategy for success in 2013, which includes sensible uses of social, cloud, mobile--all depending upon APIs. While there are plenty of other APIs to learn from, we can learn a lot from the history of modern web APIs, and these early web API pioneers.

   [1]: http://apievangelist.com/history/ (History of APIs)
   [2]: http://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm
   [3]: /history/salesforce.php (Saleforce)
   [4]: /history/ebay.php (eBay)
   [5]: /history/amazon.php (Amazon E-Commerce)
   [6]: /history/flickr.php (Flickr)
   [7]: http://blog.apievangelist.com/2010/10/07/biz-dev-2-0/
   [8]: /history/facebook.php (Facebook)
   [9]: /history/twitter.php (Twitter)
   [10]: /history/google-maps.php (Google Maps)
   [11]: http://apievangelist.com/2011/04/09/restful-business-architecture/ (RESTful approach to business)
   [12]: http://apievangelist.com/2012/01/12/the-secret-to-amazons-success-internal-apis/
   [13]: /history/amazon-s3.php (Amazon S3)
   [14]: /history/amazon-ec2.php (Amazon EC2)
   [15]: /history/foursquare.php (Foursquare)
   [16]: /history/instagram.php (Instagram)
   [17]: http://blog.programmableweb.com/2010/12/15/the-full-featured-unpublished-instagram-api/
   [18]: /2011/02/08/instagram-launches-api/
