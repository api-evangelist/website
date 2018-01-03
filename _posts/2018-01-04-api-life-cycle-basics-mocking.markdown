---
published: true
layout: post
title: 'API Transit Basics: Mocking'
date: 2018-01-04T09:00:00.000Z
tags:
  - API Evangelist
  - Virtualization
  - Mocking
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-mock-interface.png '
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-mock-interface.png" align="right" width="45%" style="padding: 15px;" /></p>

_This is a series of stories I'm doing as part of [my API Transit work](http://basics.apievangelist.com/), trying to map out a simple journey that some of my clients can take to rethink some of the basics of their API strategy. I'm using a subway map visual, and experience to help map out the journey, which I'm calling [API transit](http://basics.apievangelist.com/)--leveraging the verb form of transit, to describe what every API should go through._

One key deficiency I see in organizations that I work with on a regular basis, is the absence of the ability to quickly deploy a mock version of an API. Meaning, the ability to deliver a virtualized instance of the surface area of an API, that will accept requests, and return responses, without writing or generating any existing backend code. Mocking APIs require an API definition, and with many groups still producing these definitions from code, the ability to mock an API is lost in the shuffle. Leaving out the ability to play with an API before it ever gets built--which if you think about it, goes against much of why we design APIs in the first place.

Mocking of an API goes hand in hand with a design first approach. Being able to define, design, mock, and then receive feedback from potential consumers, then repeat until the desired API is delivered is significantly more efficient than writing code, deploying an API, and iterating on it over a longer time frame. Over the last couple of years, a growing number of services and tooling have emerged to help us mock our APIs, as well as the schema that are used as part of their requests and responses, giving birth to this entirely new stop along the API life cycle.

- [**Mockable**](https://www.mockable.io/) - A simple service for mocking web and SOAP APIs
- [**Sandbox**](https://getsandbox.com/) - A simple service for generating sandboxes using a variety of formats.
- [**Stoplight Prism**](https://github.com/stoplightio/prism) - An open source tool for mocking and transforming from OpenAPIs.
- [**Wiremock**](https://github.com/tomakehurst/wiremock) - An open source tool for mocking APIs.
- [**Postman Mock Server**](https://www.getpostman.com/docs/postman/mock_servers/setting_up_mock)You can setup mock servers from within the Postman environment.

Mocking of API is something that organizations who have not adopted an API definition approach to delivering APIs cannot ever fully realize. When you have a robust, machine readable definition of the surface area of your API it allows you to quickly generate sandboxes, mocks, and virtualized instance of an API. These interfaces can then be consumed, and played with, and allow for API definitions to be adjusted, tweaked, and polished until it meets the needs of consumers. Shortening the feedback loop between each iteration, and version of an API--saving both time and money.

The API developers I've seen who have become proficient in defining and designing their APIs, and delivering mock APIs, have also begun to be more agile when it comes to mocking and virtualizing of data that gets returned as part of mock API responses. Further pushing mocking and virtualization into testing, security, and other critical aspects of API operations. Being able to mock API interfaces is a sign that API operations is maturing, allowing for costly mistakes to be eliminated, or identified long before anything goes into production, making sure APIs meet the needs of both providers and consumers long before anything gets set into stone.
