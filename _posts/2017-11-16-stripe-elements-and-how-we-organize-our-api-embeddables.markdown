---
published: true
layout: post
title: Stripe Elements And How We Organize Our API Embeddables
date: 2017-11-16T09:00:00.000Z
tags:
  - API Evangelist
  - Embeddable
  - SDK
  - Payments
image: >-
  https://s3.amazonaws.com/kinlane-productions/stripe/stripe-elements-grey-embeddable.png
---
<p><a href="https://stripe.github.io/elements-examples/"><img src="https://s3.amazonaws.com/kinlane-productions/stripe/stripe-elements-grey-embeddable.png" align="right" width="45%" style="padding: 15px;" /></a></p>I am setting up Stripe for a client, and I found myself browsing through Stripe Elements, and [the examples they have published to Github](https://stripe.github.io/elements-examples/). If you aren't familiar, "Stripe Elements are pre-built rich UI components that help you build your own pixel-perfect checkout flows across desktop and mobile." I put Stripe Elements into my bucket of [API embeddables](http://embeddable.apievangelist.com/), which overlaps with [my API SDK research](http://sdk.apievangelist.com/), but because they are JavaScript open up a whole new world of possibilities for developers and non-developers, I keep separate.

[Stripe.js and supporting elements](https://stripe.com/docs/stripe-js) provides a robust set of solutions for integrating the Stripe API into your website, web or mobile application. You can choose the pre-made element, customize as you see fit, or custom build your own using the Stripe.js SDK. It provides a great place to start when learning about Stripe, reverse engineering some existing solutions, and figuring out what integration will ultimately look like. In my scenario, the default Stripe element in their documentation works just fine for me, but I couldn't help but playing with some of the others just to see what is possible.

You can tell Stripe has invest A LOT into their Sripe.js SDK, and the overall user experience around it. It provides a great example of how far you can go with embeddable API solutions. I like that they have the Stripe Elements published to Github, and available in six different languages. As I was learning and Googling, I came across other examples of Stripe.js deployment on other 3rd party sites, making me think it would be nice if Stripe had a user generated elements gallery as part of their offering, accepting pull requests from developers in the Stripe community. It wouldn't be that hard to come up with a template markdown page that developers could fill out and submit, sharing their unique approach to publishing Stripe Elements.

Having a Github repository to display example embeddable API tooling makes sense, and is something I'll add to my embeddable research. While not all SDKs warrant having their own Github repository, I'd say that embeddable JavaScript SDKs rise to the occasion, and when they are as robust as Stripe Elements might benefit from their own landing page, and forkable, continuously integratable elements. Actually, on second thought, in a CI/CD world I'm feeling like ALL API SDKs should have their own repository, opening up the possibility for them to have their own landing page, issues, and code in a separate repo, for easier integration. I'm going to do a round-up of Stripe's embeddable efforts, as well as the other SDKs they support, and see what other examples I can extract for other API providers to consider as they pull together their approach to supporting the intersection of embeddable and SDK.
