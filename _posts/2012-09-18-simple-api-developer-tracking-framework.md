---
layout: post
title: "Simple API Developer Tracking Framework"
url: 'http://apievangelist.com/2012/09/18/simple-api-developer-tracking-framework/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/charts-graphs-2.png'
---

<img src="https://s3.amazonaws.com/kinlane-productions/charts-graphs-1.png" alt="" align="right" />

When you have an API, you track two things: 1) Number of Developer Registrations and 2) Number of API requests. This is how we determine a successful API, right?

You should track those two things, but those metrics alone do not define a successful API. You should go much further. Each API owner will have their own definition of success, thus their own set of metrics to measure success.

With this in mind, there is no single framework for measuring your API, but here is one suggestion for a basic framework to think about when tracking your API developers.

First establish some buckets to put users in:

  * **New** \- Brand new developer
  * **Active** \- Developer actively using API (come up with number)
  * **Inactive** \- Developers who go below the "active" number threshold for X number of days
  * **Billable** \- Developer who is paying you $$
  * **Partner** \- A developer who are working closer with than rest of developers
  * **Internal** \- Your staff or contractors who actively use your API, even for testing

Then make sure and flag each user with a timestmap when they change status:

  * 5/2/2012 - New
  * 5/2/2012 - Active
  * 7/9/2012 - Billable
  * 8/15/2012 - Inactive

<img src="https://s3.amazonaws.com/kinlane-productions/charts-graphs-2.png" alt="" align="right" />

I like to generate daily, weekly and monthly counts for each bucket, plus see numbers on the churn between buckets.

Looking at developers in buckets, and tracking on their transitions between buckets allows you to start seeing the big picture, when large groups of users are migrating between status, or the individual picture, like why a single developer just went inactive.

I don’t see much to learn from just watching new registrations and number of API calls, but by creating meaningful buckets to place developers in, then understanding their evolution between these buckets, I think you can learn a lot with a pretty simple set of metrics.