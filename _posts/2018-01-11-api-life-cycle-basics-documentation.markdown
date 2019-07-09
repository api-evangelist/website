---
published: true
layout: post
title: 'API Life Cycle Basics: Documentation'
date: 2018-01-11T11:00:00.000Z
tags:
  - API Evangelist
  - Documentation
image: >-
  https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-documentation-interactive.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-documentation-interactive.png" width="30%" style="padding: 15px;" align="right" /></p>API documentation is the number one pain point for developers trying to understand what is going on with an API, as they work to get up and running consuming the resources they possess. From many discussions I've had with API providers it is also a pretty big pain point for many API developers when it comes to trying to keep up to date, and delivering value to consumers. Thankfully API documentation has been being driven by API definitions like OpenAPI for a while, helping keep things up date and in sync with changes going on behind the scenes. The challenge for many groups who are only doing OpenAPI to produce documentation, is that if the OpenAPI isn't used across the API life cycle, it will often become forgotten, recreating that timeless challenge with API documentation.

Thankfully in the last year or so I'm beginning to see more API documentation solutions emerge getting us beyond the Swagger UI age of docs. Don't get me wrong, I'm thankful for what Swagger UI has done, but the I'm finding it to be very difficult to get people beyond the idea that OpenAPI (fka Swagger) isn't the same thing as Swagger UI, and that the only reason you generate API definitions is to get documentation. There are a number of API documentation solutions to choose from in 2018, but Swagger UI still remains a viable choice for making sure your APIs are properly documented for your consumers.

- [Swagger UI](https://swagger.io/swagger-ui/) - Do not abandon Swagger UI, keep using it, but decouple it from existing code generation practices.
- [Redoc](https://github.com/Rebilly/ReDoc/) - Another OpenAPI driven documentation solution.
- [Read the Docs](https://readthedocs.org/) - Read the Docs hosts documentation, making it fully searchable and easy to find. You can import your docs using any major version control system, including Mercurial, Git, Subversion, and Bazaar.
- [ReadMe.io](https://readme.io/) - ReadMe is a developer hub for your startup or code. It's a completely customizable and collaborative place for documentation, support, key generation and more.
- [OpenAPI Specification Visual Documentation](http://openapi-specification-visual-documentation.apihandyman.io/) - Thinking about how documentation can become visualized, not just text and data.

API documentation should not be static. It should always be driven from OpenAPI, JSON Schema, and other pipeline artifacts. Documentation should be part of the CI/CD build process, and published as part of an API portal life cycle as mentioned above. API documentation should exist for ALL APIs that are deployed within an organization, and used to drive conversations across development as well as business groups--making sure the details of API design are always in as plain language as possible.

I added the visual documentation as a link because I'm beginning to see hints of API documentation move beyond the static, and even dynamic realm, and becoming something more visual. It is an area I'm investing in with my subway map work, trying to develop a consistent and familiar way to document complex systems and infrastructure. Documentation doesn't have to be a chore, and when done right it can make a developers day brighter, and help them go from learning to integration with minimal friction. Take the time to invest in this stop along your API life cycle, as it will help both you, and your consumers make sense of the resources you are producing.
