---
layout: post
title: "New Pricing for Genability Energy API"
url: 'http://apievangelist.com/2011/06/30/new-pricing-for-genability-energy-api/'
image: ''
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/genability/genability-logo.jpg" alt="" width="250" align="right" />][1][Energy pricing data provider Genability][1] just announced the roll-out of more [flexible pricing for their API][2].

The new pricing structure gives Genability API developers more options with no long term commitments, when accessing the Genability tariff and electricity pricing database.

[Genability API][3] pricing starts with a free plan which offers 10 unique tariff credits per month, and will serve up 1,000 calls per hour.

Genability bulk paid plans range from $89.99 / month to $1499.99 a month:<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/genability/genability-pricing.png" alt="" width="325" align="right" />

  * **Bronze for 89.99 / month**, with 100 unique tariff credits per month, and 5,000 calls per hour
  * **Silver for 299.99 / month**, with 350 unique tariff credits per month, and 20,000 calls per hour
  * **Gold for $799.99 / month**, with 1000 unique tariff credits per month, and 50,000 calls per hour
  * **Platinum for $1499.99 / month**, with 2000 unique tariff credits per month, and 100,000 calls per hour
The call per hour portion is pretty straightforward, but whats a tariff credit?

A tariff credit is when you request a full tariff (including all its rates, bands and properties), or request a price, or a calculation on a tariff. Genability keep track of each tariff you request, and keep a count of the unique ones, with subsequent calls for previously requested tariffs being free.

All of Genability's API plans both, both free and paid, include LSE data, season

   [1]: http://www.genability.com/ (Energy pricing data provider Genability)
   [2]: https://developer.genability.com/plans-pricing (flexible pricing for their API)
   [3]: https://developer.genability.com/ (Genability API)
