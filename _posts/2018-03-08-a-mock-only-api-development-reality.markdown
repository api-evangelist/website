---
published: true
layout: post
title: Imagine A Mock Only API Development Reality
date: 2018-03-08T12:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Mock
  - Prototyping
  - Maturity
  - Deployment
  - Lifecycle
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/gears_smoking_cigarette.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>Imagine if we didn't actually write code when we developed our APIs initially. What if the bar for putting an API into production was so high, that many APIs never actually made it to that level. I spend a lot of time mocking and prototyping APIs, but I don't have a strict maturity model determining when I actually bring an API to life using code. I'd love it if I never actually write code for many of my API prototypes and just mocked them, and iterated upon the mocks instead of thinking they needed actually have a database backend, and code or gateway front-end.

What if I only executed these stops along the API lifecycle, instead of actually writing any code:

- **Define** - Define what I want my API to do, and what types of resources will be involved.
- **Design** - Actually design my API and underlying schema using an OpenAPI definition.
- **Mock** - Publish a mock representation of my API, complete with virtualized data behind responses.
- **Document** - Make sure and publish documentation to a simple developer portal.
- **Plan** - A overview of what it will cost, and the model for managing consumption.
- **Testing** - Set up tests to ensure each API is up and doing what it was intended to do.
- **Communicate** - Actually write stories, and communicate around what an API does.
- **Support** - Establish and maintain feedback loops around the API to listen to consumers.
- **Road Map** - Gather feedback into a road map, and plan next version, complete with a change log.

In this life cycle I would never actually write any code. I would never actually setup a database backend. Everything would be mocked and virtualized, but seem as real as I possibly can. Even maybe providing different types of virtualized datasets and responses, so people can experience different types of responses or scenarios. I'd work hard to make sure each API was as complete, and function like a real APIs, as I possibly could.

Now imagine within a company, if I had to do all of this, and before I would ever be allowed to begin developing my API for real, I had to sell my API. Show its value, and get some consumers to buy into my overall API design, and even develop some mock integrations showing the potential. Before my API would be considered for inclusion in the production road map, I'd have to prove that my approach was mature enough in each of the areas outlined above:

- **Define** - Robust OpenAPI and JSON schema present.
- **Design** - A complete design meeting all governance guidelines.
- **Document** - Complete, up to date API document present.
- **Plan** - A clear definition of costs, and how consumption will be measured.
- **Testing** - A full suite of tests available with 100% coverage.
- **Communicate** - Demonstrated ability to communicate around its operations.
- **Support** - Demonstrated ability to support the APIs operation.
- **Road Map** - Clearly articulated road map, and change log for the API.

As an API developer, once I've build the case for my microservice, presented it, and demonstrated its value--then I would be approved to actually begin developing it. Maybe in some cases I would be required to iterate upon it for another version, and engage with a larger audience before actually given the license and budget to do it for real. Going well beyond just an API design first reality, and enforcing a maturity model around how we define and communicate around our services, and raising the bar for what gets let into production.

Many of the companies, organizations, institutions, and government agencies I'm working with are having a hard time adopting a define and design first strategy, let alone a reality such as this. Imagine how different our production worlds would look if you had all this experience before you were ever given the license to write code. Think about how much worthless code gets written, when we should just be iterating on our ideas. How much of our budget gets wasted on writing code that should never have existed to begin with. It's a nice thought. However, it is just a fantasy.
