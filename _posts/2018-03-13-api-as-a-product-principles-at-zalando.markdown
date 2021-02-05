---
published: true
layout: post
title: API As A Product Principles From Zalando
date: 2018-03-13T09:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Governance
  - Business of APIs
image: >-
  https://s3.amazonaws.com/kinlane-productions/zalando/zalando-api-guidelines.png
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>As I'm working through the API design guides from API leaders, looking for useful practices that I can include in my own API guidance, I'm finding [electronic commerce company Zalando's API design guide](zalando.github.io/restful-api-guidelines/) full of some pretty interesting advice. I wanted to showcase the section about their API as a product principles, which I think reflects what I hear many companies striving for when they do APIs.

From the Zalando API design guide principles:

_Zalando is transforming from an online shop into an expansive fashion platform comprising a rich set of products following a Software as a Platform (SaaP) model for our business partners. As a company we want to deliver products to our (internal and external) customers which can be consumed like a service._

_Platform products provide their functionality via (public) APIs; hence, the design of our APIs should be based on the API as a Product principle:_

- _Treat your API as product and act like a product owner_
- _Put yourself into the place of your customers; be an advocate for their needs_
- _Emphasize simplicity, comprehensibility, and usability of APIs to make them irresistible for client engineers_
- _Actively improve and maintain API consistency over the long term_
- _Make use of customer feedback and provide service level support_

_RESTful API as a Product makes the difference between enterprise integration business and agile, innovative product service business built on a platform of APIs._

_Based on your concrete customer use cases, you should carefully check the trade-offs of API design variants and avoid short-term server side implementation optimizations at the expense of unnecessary client side obligations and have a high attention on API quality and client developer experience._

_API as a Product is closely related to our API First principle which is more focused on how we engineer high quality APIs._

Zalando provides a pretty coherent vision for how we all should be doing APIs. I like this guidance because it helps quantify something we hear a lot--APIs as a product. However, it also focuses in on what is expected of the product owners. It also gets at why companies should be doing APIs in the first place, talking about the benefits they bring to the table.

I'm enjoying the principles section of Zalando's API design guide. It goes well beyond just API design, and reflects what I consider to be principles for wider API governance. Many companies are still considering this API design guidance, but I find that companies who are publishing these documents publicly are often maturing and moving beyond just thinking deeply about design--providing a wealth of other wisdom when it comes to doing APIs right.
