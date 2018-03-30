---
published: true
layout: post
title: Using Postman to Explore the Triathlon API
date: 2018-03-30T09:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Discovery
  - Sports
image: >-
  https://s3.amazonaws.com/kinlane-productions/triathalon/w2WBMG2bTD6TahNs2MG3_150919-chicago-elite-m-web-msj-43.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I'm taking time to showcase any API I come across who have published their OpenAPI definitions to Github like [New York Times](https://apievangelist.com/2017/03/01/new-york-times-manages-their-openapi-using-github/), [Box](https://apievangelist.com/2017/02/14/boxs-seamless-approach-to-api-documentation/), [Stripe](https://apievangelist.com/2017/06/02/the-github-repo-stripe-users-to-manage-their-openapi/), [SendGrid](https://apievangelist.com/2018/03/20/sendgrid-managing-their-openapi-using-github/), [Nexmo](https://apievangelist.com/2018/03/26/nexmo-manages-their-openapi-30-definition-using-github/), and others have. I'm also taking the time to publish stories showcasing any API provider who similarly publish Postman Collections as part of their API documentation. Next up on my list is [the Triathlon API](https://developers.triathlon.org/docs/using-postman-to-explore-the-triathlon-api), who provides a pretty sophisticated API stack for managing triathlons around the world, complete with a list of Postman Collections for exploring and getting up and running with their API.

[Much like Okta, which I wrote about last week](http://apievangelist.com/2018/03/20/breaking-down-your-postman-api-collections-into-meaningful-units-of-compute/), the [Triathlon API has broken their Postman Collections into individual service collections](https://developers.triathlon.org/docs/using-postman-to-explore-the-triathlon-api), and provides a nice list of them for easy access. Making it quick and easy to get up and running making calls to the API. Something that ALL API providers should be doing. Sorry, but Postman Collections should be a default part of your API documentation, just like OpenAPI definition should be as the driver of your interactive API docs, and the rest of your API lifecycle.

Every provider should be maintaining their OpenAPI definitions, as well as Postman Collections on Github, and baking them into their API documentation. Your OpenAPI should be the central truth for your API operations, and then you can easily import it, and generate Postman Collections as you design, test, and evolve your API using the Postman development suite. I know there are many API providers who haven't caught up to this approach to delivering API resources, but it is something they need to tune into, and make the necessary shift in how you are delivering your resources.

In addition to regular stories like this on the blog, you will find me reaching out to individual API providers asking if they have an OpenAPI and / or Postman Collections. I'm personally invested in getting API providers to adopt their API definition formats. I want to see their APIs present in [my API Stack work](http://theapistack.com), as well as other API discovery projects I'm contributing to like Streamdata.io, Postman Network, APIs.Guru, and others. Making sure your APIs are discovered, and making sure you are getting out of the way of your developers by baking API definitions into your API operations--it is just what you do in 2018.
