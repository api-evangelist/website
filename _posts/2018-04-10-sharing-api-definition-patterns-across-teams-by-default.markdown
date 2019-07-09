---
published: true
layout: post
title: Sharing API Definition Patterns Across Teams By Default
date: 2018-04-10T09:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Collaboration
  - Teams
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/carryload_smoking_cigarette.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>_This is a story, in a series I’m doing as part of the version 3.0 release of [the Stoplight.io platform](https://next.stoplight.io/). Stoplight.io is one the few API service providers I’m excited about what when it comes to what they are delivering in the API space, so I jumped at the opportunity to do some paid work for them. As I do, I’m working to make these stories about the solutions the provide, and refrain from focusing on just their product, hopefully maintaining my independent stance as the API Evangelist, and keeping some of the credibility I’ve established._

One of the things I’m seeing emerge from the API providers who are further along in their API journey, is a more shared experience when it comes to not just the API design process, but in action throughout the API lifecycle. You can see this reality playing out with the API definitions, and the move from Swagger 2.0 to the OpenAPI 3.0, where there is a more modular approach to defining an API, encouraging reuse of common patterns across API paths within a single definition, as well as across many different API definitions. Expanding on how API definitions can move an API through the lifecycle, and beginning to apply that across projects and teams, and moving APIs through lifecycle much more quickly, and consistently.

**Emulating the Models We Know**<br />
We hear a lot about healthy API design practices, following RESTful philosophies, and learning from the API design guides published by leading API providers. While all of these areas have a significant influence on what happens during the API design and development process, the most significant influence on what developers know, it is just what they are exposed to in their own experience. The models we are exposed to often become the models we employ, demonstrating the importance of adopting a shared experience when it comes to defining, designing, and putting common API models to work for us in our API journeys.

**A Schema Vision Reflects Maturity**<br />
The other side of this shared API definition reality, are the reuse and sharing of schema. The paths, parameters, and models for the surface area of our APIs is essential, but the underlying schema we use as part of the request and responses will eliminate or introduce the most friction when it comes to API integration. Reinventing the wheel with schema creates friction throughout the API lifecycle from design to documentation, and will make each stop significantly more costly, something that will ultimately be also passed off to consumers. Sharing, reusing, and being organized with schema used across the development of APIs is something you see present within the practices of the API teams who are realizing more streamlined, mature, API deliver pipelines.

**Sharing Across Teams Is How Its Done**<br />
Using common models and schema is important, but none of it matters if you aren’t sharing them across teams. Leveraging Git, as well as the social, team, and collaborative features to share and reuse common models and schema is what helps reduce friction, and introduce efficiency into both the deployment and integration of APIs. API design doesn’t occur in isolation anymore. Gone are the pizza in the basement days for developing APIs, and the API lifecycle is a social, collaborative affair. Teams that have a mature, consistent, and reproducible API lifecycles, are sharing definitions across teams, and actively employing the most mature patterns across the APIs they deliver. Without a team mentality throughout the API lifecycle, APIs will never truly be interoperable, reusable, and consumable set of services we expect.

**Without API Definitions There Is No Discovery**<br />
Ask many large organizations who are doing APIs without API definitions like OpenAPI, and who haven’t adopted a lifecycle approach, where their APIs are, and they will just give you a blank stare. APIs regularly get lost in the shuffle of busy organizations, and can often be hidden in the shadows of the mobile applications they serve. However, when you adopt and API definition by default, as well as an API definition-driven life cycle, discovery is baked in by default. You can search Github, reverse engineer schema from application logs, and follow the code pipeline to find APIs. API definitions leave a trail, and API documentation, testing, and other resources all point to where the APIs are. API discovery isn’t a problem in an API definition driven world, it is baked in by default.

**API Governance Depends on API Definitions**<br />
I get a regularly stream of requests from organizations who have already embarked on their API journey regarding how they can work to more consistently deliver APIs, and institute a governance program to help them measure progress across teams. The first question I always ask is whether or not they use OpenAPI, and the second question is regarding what their API lifecycle and Git usage looks like. If they aren’t using OpenAPI, and haven’t adopted a Git workflow across their teams, API governance will rarely ever be realized. Without definitions you can’t measure. Without a Git workflow, you can find the artifacts you need to measure. API governance can’t exist in isolation, without relevant definitions in play.

OpenAPI has significantly contributed to the evolution, and maturity of what we know as the API lifecycle. Without them we can’t share common models and schema. We can’t work together and learn from each other.  Without tooling and services in place that allow us to share, collaborate, mock, and communicate around the API design and development process, the API process will never mature. It will not be consistent. It will not move forward and reach a production line level of efficiency. To realize this we have to share definitions across teams by default--without it, we aren’t really doing APIs.

P.S. Thanks [Stoplight.io](https://next.stoplight.io/) for the support!
