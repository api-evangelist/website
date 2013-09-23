---
layout: post
title: "Estimating the Number of Non-Public APIs"
url: 'http://apievangelist.com/2013/01/24/estimating-the-number-of-non-public-apis/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/SDKBridge-logo.gif'
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-service-providers/sdk-bridge/SDKBridge-logo.gif" alt="" width="200" align="right" />][1]

_This post comes from the [SDK Bridge][1] newsletter.  I find so much value from what Peter and Jonathan do over at SDK Bridge, I always have to post their newsletter here and share with all of you._

ProgrammableWeb is known for publishing the number of public APIs in its directory, and they regularly present an impressive [graph][2] that shows how this number has increased exponentially over time. However, not all APIs are public, and ProgrammableWeb is not able to obtain information on how many non-public APIs exist.

SDK Bridge writes API documentation as a service, and many of our customers have us document their non-public APIs. That puts us in a unique position to be able to estimate what percentage of APIs is public compared to non-public.

###  Definitions

What exactly is a non-public API? For the purposes of this article, let's define a few terms.

**Public API.** A public API is an API where the documentation is freely available on the Web. Using the API may require registering and paying a fee.

**Partner API.** A partner API is an API where the documentation is not made available to the public, but is made available to select companies who have some kind of partnership agreement with the API provider. Typically the documentation is accessible through a password-protected website.

**Internal API.** An internal API is an API that is only used by developers who work for the company that provides the API. Typically the documentation is available only on an internal website.

###  Data

Since its inception in 2008, SDK Bridge has written documentation for 23 web APIs. (Web APIs are only a portion of the writing that we do for software professionals. We also write SDK documentation, IT documentation, and training curricula, as well as create video tutorials for developers.) Of these APIs, 12 were public, 9 were partner, and 2 were internal. The following pie chart shows the breakdown:

<img src="https://i6.createsend1.com/ei/r/97/AC3/A0A/061035/nonpublicapipie.png" alt="" />

Web API documentation by type.

For the non-public APIs (partner and internal), it's interesting to note that 82% were RESTful and 18% were SOAP APIs. Also, 91% supported XML formats and 18% supported JSON formats. This suggests that non-public APIs have mostly made the transition from SOAP to REST, but have largely not made a transition from XML to JSON.

###  Conclusions

Our data analysis indicates that roughly half of web APIs are not public. Two factors to consider:

  * The sample size is still fairly small. As time goes on and we get a larger sample size, we will improve the accuracy.
  * Companies may be less inclined to hire outside writers for non-public APIs than for public APIs. This means that our data could easily result in an underestimation of non-public APIs.

However, for now, if you are looking for a rough estimation of the total number of APIs, you can take the number published by ProgrammableWeb and double it.

   [1]: http://sdkbridge.com/ (SDK Bridge)
   [2]: http://sdkbridge.createsend1.com/t/r-l-utikkyk-hdhyyhjli-j/
