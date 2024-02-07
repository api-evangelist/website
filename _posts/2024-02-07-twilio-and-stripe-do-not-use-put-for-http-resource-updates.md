---
published: true
layout: post
title: 'Twilio and Stripe Do Not Use PUT For HTTP Resource Updates'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/gone-with-the-wind-old-bearded-man-thinking.jpeg
author:
    name: kinlane
tags:
- Methods
- PUT
- Design
- REST
---
The shouts of the RESTafarians in 2010 still ring loud in my head. REST wasn’t just a philosophy, it was a religion. You needed to have read Roy Fielding’s dissertation and posses a strong handle on the four levels of REST maturity, otherwise you were doing IT WRONG!!! Folks rarely demonstrated what they were talking about, and almost always shamed you when you didn’t emulate what they were talking about in your work. Maybe I am just too sensitive, but it was this dogma that pushed me to start API Evangelist to help others understand what was going on without shaming them.

There are many dimensions of this conversation, but one of the many fundamental principles of REST states clearly that you utilize your HTTP methods for handling your basic Create, Read, Update, and Delete (CRUD) capabilities. Meaning you use POST to create resources, GET to read resources, PUT to update resources, and DELETE to delete resources. It is so simple. It is widely known and believed. However, in 2024, anyone on the ground doing APIs, knows it is far from the gospel truth. Evidence for this is that both Stripe and Twilio use POST to update many common payment, messaging, and other resources.

## Stripe
<p><a href="https://stripe.com/docs/api/charges/update"><img src="https://kinlane-productions2.s3.amazonaws.com/stripe-post-update.png" width="100%" style="padding; 15px;"></a></p>

￼
## Twilio
<p><a href="https://www.twilio.com/docs/iam/api/account"><img src="https://kinlane-productions2.s3.amazonaws.com/twilio-post-update.png" width="100%" style="padding; 15px;"></a></p>
￼
These are two API producers that we hold up as shiny examples of how to do APIs well, and both deviate from true REST, operating in the RESTful and RESTish lands where the rest of us are struggling in for years. What does it mean? Not much. Sure, I recommend you standardize your APIs what the other APIs developers are use to do, but the world doesn’t end if you are kinda sorta REST. Sorry, it doesn’t. I know it drives many of us API pedantic nuts, but it reflects the real world we all are forced to live in each day.

Stripe and Twilio using POST to update resources isn’t something you hear when people showcase these two API producers. This isn’t a blog post that will get a lot of traffic or discussion. This isn’t a blog post you’d write if you are an API analyst or service provider looking to sell you something. This is a mundane anecdote of API operations that has rippling effects on how applications work and how developers see the world. Semantically it will screw up many iPaaS solutions being used to stitch together our digital experiences across many APIs. It is one of thousands of little inconsistencies that exist and cause developers to stumble today and one that will muck up the inner workings of our AI.

