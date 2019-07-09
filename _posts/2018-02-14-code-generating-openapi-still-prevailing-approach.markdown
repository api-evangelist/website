---
published: true
layout: post
title: Code Generation Of OpenAPI (fka Swagger) Still The Prevailing Approach
date: 2018-02-14T14:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Deployment
  - Design
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/gears-numbers-blue.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/gears-numbers-blue.jpg" align="right" width="40%" style="padding: 15px;" /></p>Over 50% of the projects I consult on still generate OpenAPI (fka Swagger) from code, rather then the other way around. When I first begin working with any API development group as an advisor, strategist, or governance architect I always ask, "are you using OpenAPI?" Luckily the answer is almost always yes. The challenge is that most of the time they don't understand the full scope of how to use OpenAPI, and are still opting for the more costly approach--writing code, then generating OpenAPI from annotations. It has been over five years since Jakub Nesetril(@jakubnesetril) of Apiary first decoupled this way of doing API design first, but clearly we still have a significant amount of work when it comes to API definition and design literacy amongst development groups.

When you study where API services and tooling are headed it is clear that API deployment, and the actual writing of code is getting pushed further down in the life cycle. Services like Stoplight.io, and Postman are focusing on enabling a design, mock, document, test, and iterate approach, with API definitions (OpenAPI, Postman, etc) at the core. The actual deployment of API, either using open source frameworks, API gateways, or other method, is coming into the picture more downstream. Progressive API teams are hammering out exactly the API they need without ever writing any code, making sure the API design is dialed in before the more expensive, and often permanent code gets written and sent to production.

You will see me hammering on this line of API design first messaging on API Evangelist over the next year. Many developers still see OpenAPI (fka Swagger) about generating API documentation, not as the central contract that is used across every stop along the API lifecycle. Most do not understand that you can mock instead of deploying, and even provide mock data, errors, and other scenarios, allowing you to prototype applications on top of API designs. It will take a lot of education, and awareness building to get API developers up to speed that this is all possible, and begin the long process of changing behavior on the ground. Teams just are used to this way of thinking, but once they understand what is possible, they'll realize what they have been missing.

I need to come up with some good analogies for generating API definitions from code. It really is an inefficient, and a very costly way to get the job done. Another problem is that this approach tends to be programming language focused, which always leaves its mark on the API design. I'm going to be working with both Stoplight.io and Postman to help amplify this aspect of delivering APIs, and how their services and tooling helps streamline how we develop our APIs. I'm going to be working with banks, insurance, health care, and other companies to improve how they deliver APIs, shifting things towards a design-first way of doing business. You'll hear the continued drumbeat around all of this on API Evangelist in coming months, as I try to get the attention of folks down in the trenches, and slowly shift the behavior towards a better way of getting things done.
