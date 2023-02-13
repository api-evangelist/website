---
published: true
layout: post
title: 'The Source of Truth for an API'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/yellow-journalism-marketplace-people.jpg
author:
name: kinlane
tags:
- OpenAPI
- AsyncAPI
- Collections
- Source of Truth
- Mocking
- Testing
---
I was talking with Laurent Broudoux ([@lbroudoux](https://twitter.com/lbroudoux)) and Yacine Kheddache ([@YadaYac](https://twitter.com/yadayac)) over at [Microcks](https://microcks.io/) this week. As I listened to them discuss the intersection of multiple API protocols like HTTP, gRPC, and Websockets, multiple specifications like OpenAPI, AsyncAPI, and Postman Collections, as well as multiple stops along the API Lifecycle like documentation, testing, and mocking, I found us discussing what is the source of truth for an API. Like. Many aspects of API operations, understanding where the source of truth lies for an API being developed, delivered, and iterated upon, is a contentious subject which means many different things depending on who you are talking to. Something that makes it difficult to agree upon a single API, let alone the hundreds or thousands of APIs we depend on to operate our businesses. 

Many of us design-first people will exclaim that the OpenAPI or AsyncAPI is the source of truth for an API, but when these artifacts can exist in multiple different locations, it can be difficult to establish any single copy as a single source of truth. Many code-first API believers will declare that the source of truth is whatever is in production, which gets us closer to the truth of this conversation, but with many APIs in production operating in an undocumented manner, the source of truth can be hard to nail down in any given moment. The folks of at Microcks who I feel represent the front line of this discussion for me because they operate in a multi-protocol and multi-specification world possess a definition for the source of truth that I consider to be the best I have come across to date. 

I will work to get a better definition from Laurent and Yacine, but their view goes something like this. It is easy to consider an artifact like OpenAPI, AsyncAPI, or Postman Collection the source of truth for an API. When you mock and establish tests for an API using these artifacts, you get even closer to a source of truth for not just an API in production, but also for one that is in development. But where Laurent and Yacine considered the actual source of truth lying was in the understanding reached between all the human beings involved in producing and consuming an API by leveraging artifacts, mocks, and tests. The source of truth isn’t the artifact, a mocked or production instance of an API, or even the tests—-the source of truth is the understanding reached between human beings at the intersection of all of these. A very powerful and important belief.

Once again, it isn’t the API. It is the humans. I really, really like this. I’ve long centered my definition of the source of truth on the machine-readable artifact, and often emphasize the importance of tests to validate this artifact. Then I will waffle between artifacts and tests being the truth or production being truth. I like Microck’s definition better. The truth is what the humans agree upon being the truth. Without humans there is no truth. If you can’t convince the people involved, there is no truth. I love this perpetually returning to why the humans matter. Even as someone who is team human over team API, I find myself perpetually sucked into the trap that APIs and the operations surrounding them are what really matters. In the end, none of these matters if it doesn’t matter to the humans. I understand that to many humans the technology is what matters, and to others the business is what matters. But sorry....it is the humans. It is always the humans. The source of truth is in the agreement between everyone involved, and demonstrates why the agreement between API producer and consumer is where we should be focusing, and searching for this often elusive truth.
