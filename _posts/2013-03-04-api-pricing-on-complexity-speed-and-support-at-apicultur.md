---
layout: post
title: "API Pricing On Complexity, Speed and Support At Apicultur"
url: 'http://apievangelist.com/2013/03/04/api-pricing-on-api-complexity-speed-and-support-at-apicultur/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/apicultur-logo.png'
---

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/apicultur/apicultur-logo.png" alt="" width="200" align="right" />

How to structure pricing for an API is one of the top 5 questions I get from people who are currently planning their API strategy. In my opinion, there is, and never will be a one size fits all API pricing strategy. What you charge for your API resources should reflect their value and how they are accessed and used by your target consumers.

The Backend as a Service (BaaS) space is working hard to differentiate themselves in 2013 with [different approaches to pricing of mobile backend resources][1]. Amazon is still shaking up the API space with new services, pricing models and the price reduction of API resources at a dizzying pace.

I had the pleasure of meeting the [Apicultur][2] team while in Paris for [API Days][3] last October. Apicultur is a linguistics API platform, that is pushing the boundaries of what is an API platform as well as how you price language API resources.

Apicultur recently shared some of the thinking behind the [current version of their platform pricing][4] where they structure the price depending on three factors:

  * **Complexity of the API** \- Some APIs perform a very simple task (like removing commas from a text) while others deal with more complex task (like extracting if the opinion expressed in a particular text is positive or negative)--the "bigger" the API, the pricier it gets
  * **Speed** \- The max speed by default is one call per second. In order to get more calls per second, Apicultur ask for a prepayment that is discounted from the final price at the end of the month (i.e., is not an extra price, is just a prepayment as a commitment). In addition, there's a discount at the end of the month for users for those who get a speed limit feature
  * **Support - **The basic support offered is the community support. For more support, special fees are offered

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/apicultur/apicultur-pricing.png" alt="" width="325" align="right" />

Apicultur feels that by keeping the everything priced at 10,000 API calls, keeps things easy to understand as well as being fair for small and large projects.  Leaving the costs spread between the varying value of individual API endpoints, the speed at which you need API calls and for overall support.

Small projects can register for the free account, which gives you up 20€ a month in calls without requiring a credit card, allowing developers to try an API before giving personal information and committing. I find it very interesting they call it a free account, while still applying a price to the value users are getting.

Apicultur has put a lot of thought into how they structure their API pricing. I think their approach can help other API providers think about the value each of their endpoints offer, as well as other areas you can monetize, delivering more of what your API consumers need, while also bringing in revenue to make sure your API initiative is successful.

   [1]: /2013/02/07/which-baas-pricing-model-is-better/ (baas pricing)
   [2]: https://store.apicultur.com/ (apicultur)
   [3]: http://apidays.io
   [4]: https://store.apicultur.com/site/pages/prices.jag
