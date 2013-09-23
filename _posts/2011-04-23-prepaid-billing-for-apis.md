---
layout: post
title: "Prepaid Billing for APis"
url: 'http://apievangelist.com/2011/04/23/prepaid-billing-for-apis/'
image: ''
---

One of the core principles of [cloud computing][1] is its pay-as-you-go billing model. As [APIs][2] are a essential part of cloud computing, it seems natural that this same model be used there as well. In other words, you pay based on how many calls you make to the API.

But there are other ways to handle payments. Rather than billing at the end of a month based on the number of calls made, you can offer developers the option to prepay. While they're still billed based on calls, that bill is paid in advance.<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/prepaid-api-billing.png" alt="" width="250" align="right" />

[Phaxio][3], an API that allows developers to [integrate faxing capabilities into their applications][3], is one example of this.

Under your account settings, Phaxio provides a Recharge your Balance tool for paying for calls made via the API.

You can select an amount between $10.00 and $1,000.00, enter a credit card and billing information, and prepay for all calls made to the API.

All incoming and outgoing faxes through the Phaxio API are 7� per page, debited against your prepaid account balance.

A prepaid billing model for APIs make a lot of sense, concerns about potentially out of control cloud computing bills are common. Paying for estimated API use ahead of time is a great way to keep development and IT costs under control.

   [1]: http://www.kinlane.com/category/cloud-computing/
   [2]: http://www.apievangelist.com
   [3]: http://www.phaxio.com/ (Phaxio)
