---
published: true
layout: post
title: 'What is an API Review?'
tags:
  - Governance
  - Reviews
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/copper-circuit-fixing-cross.jpg
---
I am immersed in all the business and technical details of API reviews, and I want to continue working through my thoughts about what an API review currently is, as well as what it could be. There are a number of reasons API reviews work or don’t work, and they are definitely a critical place for learning and engagement, but also anxiety and friction. I want to unwind all of the different things occurring at this intersection, and work to reorganize things to optimize for learning and engagement, while reducing the anxiety and friction for everyone involved.

## Design
Most of the API reviews today are considered API design reviews where teams are looking at the RESTfulness of an API, evaluating the naming and ordering of the paths, consistent use of HTTP verbs, and status codes. Design governance is the dominant form of API governance out there today, which seems like on the surface it will help teams, but when teams haven’t received any guidance or education on REST and HTTP, it will just become a DDOS of what people do not understand. API governance today makes sure you know that you don’t have a clue what REST is or isn’t, and oh here are 348 things you’ve done wrong-—could you go fix those things.

## Self-Service
Making API reviews self-service helps reduce the anxiety for teams producing APIs, but also the API governance teams who are in charge of API reviews. Self-service API reviews help more efficiently move API operations forward in an asynchronous way without meetings. Self-service also leaves teams producing APIs to figure things out for themselves in isolation, oftentimes without the proper context, references, and guidance to understand why each particular aspect of API governance means, why it matters, and how to implement. Self-service is essential to a successful API governance program, but it also can quickly become the number one reason why your API governance will slow, stall, and fail.

<img src="https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/copper-circuit-ferris-wheel-fair.jpeg" style="padding: 15px;">

## In-Person
Most API reviews are conducted before you can leave a development stage via video conferencing. Reviews are often a single API governance, design, or architect leading the review, with one or many team members representing the producers behind an API. In-person reviews provide much needed human interaction, can facilitate learning and engagement on both sides of the equation, but then can also quickly become a bottleneck depending on schedules and the amount of API governance resources that are available.

## Technical
API reviews primarily look at the technical details of an API, making sure your paths, HTTP methods, request-bodies, responses, status codes, and schema are ordered. API governance is almost always defined and implemented by technical folks because when hiring for API governance roles you are measured based upon your technical chops. There is a meaningful baseline for the technical baseline for API reviews, but when left in the hands of technologist to define the rules and apply the rules you end up with technological creep and complexity, often choosing that over simplicity, and expanding API governance into other protocols and patterns that will dilute the effectiveness of HTTP API reviews.

## Business
We are beginning to see API reviews move into the realm of business concerns, beginning with what is needed for documentation, discovery, and other things business and product stakeholders will care about, but we need much, much more of this. APIs are seen as technical, developed by technical people, and governed by technical people, but yet they are powering our businesses. API reviews must cover onboarding, pricing, terms of service, privacy, status, performance and other real world business concerns.

## Lifecycle
I see very little evidence that the lifecycle of an API is playing into the API review approach of API governance teams, services, and tooling. Despite teams asking, when should I do this work, and do I need to do all of this during development--we aren’t doing a very good job of organizing our API governance and reviews based upon any time frame or lifecycle. There are some efforts to shift API governance left, but API reviews are still generally done before you move into staging or production to support a code-first approach.

<img src="https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/copper-circuit-statue-supreme-court.jpg" style="padding: 15px;">

## Teams
The team who is producing an API will significantly change the tone of any review, and teams as a whole should be part of an API review. Teams are expected to do reviews, without much consideration to which roles are involved, what skills do they possess, and any confirmation that they’ve read the API review guidance. Teams are why API reviews should zoom out beyond just the technical details of an API, ensuring that we are reviewing the whole package of what delivers an API, with actual people at the center.

## Enforcement
It is common for enterprise leadership and API governance teams to enforce API reviews as part of CI/CD pipelines. We have seen API reviews being automated and made self-service earlier on in the API lifecycle, but I’ve repeatedly seen leadership opt to just turn on hundreds of rules as part of automation and CI/CD without much consideration for what the impact will be. The enforcement of API reviews needs to be multi-faceted, spread across the API lifecycle, and enforced technically as well as organizationally.

## Exceptions
There will always be exceptions to rules applied as part of API reviews. Exceptions can be done verbally and through the application of manual overrides. Exceptions can also be done in automated ways using ticketing, specification extensions, and using more robust and complex rules. Exceptions should be a default aspect of API reviews, but should always be visible on the permanent record for an API, being revisited with each future iteration, and reported upon holistically across teams and the APIs they produce to inform API governance.

## Automation
API reviews can and should be automated within tooling teams are using, through the adoption of design tooling, through IDE plugins and extensions, and baked into existing source control and CI/CD solutions. API review automation ideally is incremental over time beginning with the first step in bringing an API to life, but then also validated and enforced on any API moving out of development stages, keeping automation incremental and guiding teams forward rather than just dumping a bunch of errors in the way of production.

<img src="https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/copper-circuit-supreme-court_36341562380_o.jpg" style="padding: 15px;">

## Rules
API reviews are defined and automated using Spectral and other types of machine-readable rules that help us define each granular detail of API governance. Rules are defined using a YAML or  TypeScript/JavaScript format which apply to specific patterns or anti-patterns present in an OpenAPI or other machine-readable artifact we use to define our APIs. Rules are only as good as the artifact they are being applied to, and then again based upon how that artifact is used to actually configure API operations and most importantly the runtime. 

## Policies
API governance policies help organize the many rules we use during API reviews into meaningful groupings for business stakeholders. API policies provide the business logic behind why we are governing our APIs, and applying individual rules throughout the lifecycle of an API. API policies provide us with the knobs and levers we need to align our API governance and the review of our APIs with our business operations, helping bridge the gap between product and engineering, and translate the technical details into actual business value.

## Strategy
API reviews can and should be conducted in a tactical fashion to help ensure more consistent APIs, but they are ideally also being rolled up and evaluated based upon an overall API strategy. Without a higher level API strategy framework to define API operations, API reviews can leave you wandering without direction, or worse, heading in the wrong direction. API strategies should start simple and help organize the policies and rules applied during reviews, and allow for reporting on progress and change in business terms.

## Guidance
API reviews should possess Just-in-Time API Guidance &#8482;, ensuring that teams have exactly what they need at the moment of an API review to correct and evolve the design and delivery of their APIs. API guidance should be textual, video, and provide examples of what to do, as well as what not to do. API guidance should be simple, informative, and help turn each technical and business element of an API review into a teachable moment, helping make up for other deficiencies in education and teams reading the documentation.

<img src="https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/copper-circuit-old-books-rack.jpg" style="padding: 15px;">

## Education
API reviews are always reflecting the overall training and education that exists within an enterprise. Each technical and business detail being surfaced by an API review will represent a single area that an individual or team is missing from the skills needed to properly design, develop, and deliver a modern HTTP API. API governance and the reviews that happen on the ground are the result of underinvestment by enterprises and entire industries in their works regarding the fundamentals of HTTP and the web we use each day.

## Artifacts
Machine-readable artifacts like APIs.json, OpenAPI, JSON Schema, and Spectral are what shapes and defines an API review. When you conduct an API review in-person or self-service you are in fact reviewing the APIs.json for business details, an OpenAPI with JSON Schema for the technical details, and API reviews are automated using Spectral. API reviews are all about the artifacts present and the completeness of those artifacts at the time of review, as well as the usage of those artifacts in other stages of the API lifecycle.

## Source of Truth
Having a source of truth for the technical and business details of an API, but also for the discussion and coordination around an API will make or break individual API reviews, but also wider API governance. If what is being reviewed is incomplete or a moving target, the API review becomes exponentially more complicated to accomplish. If we aren’t on the same page going into a review, conducting a review, coming out of a review, and across multiple reviews, there will be no reason to even conduct API reviews.

## History
API reviews aren’t a one time affair and the history of an API, the team behind, as well as the teams who are governing and reviewing APIs will define the success, failure, and friction of API reviews. An API review will likely not happen in a single isolated instance and will occur over time, while also being applied to each version of an API as they are being iterated upon. Having a handle on the history of each API review should inform future reviews, and ensure that we are actually moving forward with our APIs.

<img src="https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/copper-circuit-railroad-tracks-rocks.jpeg" style="padding: 15px;">

## Progress
Keeping an eye towards the progress being made through the review of APIs will help improve APIs and the teams behind them, but also the policies, rules, and overall API strategy. It is easy to focus on API reviews being a single event, but in reality they happen throughout the lifecycle of an API. Tracking on the progress of teams, APIs, as well as policies and rules are how you collectively iterate upon your business operations from a technical, business, policy, and people perspective, keeping things always on track.

## Change
APIs are all about managing change, and API reviews are just as much about change management as versioning, and your change log or road map. API reviews are where we communicate change with API producers, but also at the API governance policy and rule level. API reviews help us communicate and absorb the shock of technical but also business change, but API reviews are also the frontline for witnessing the damaging impact of change that isn’t planned or communicated, so make sure you are ready.

## Reviews
Ok, so what are we reviewing? APIs? Teams? Culture? Process? D) All the Above. This stroll through the elements of a review demonstrate how early on in this API governance journey we are. As with other areas of API operations we continue to over invest in the technical details, and ignore the business and people aspects of our operations. Reviews are an opportunity for us to come together and find alignment synchronously or asynchronously. An API review is our chance to get on the same page regarding all of the many technical and business details that are required to deliver enterprise-grade API infrastructure—making sure we are covering all of our bases.

I needed a reality check on what an API review is. I have conducted around 150 in-person API reviews in the last year, as well as ongoing API reviews done asynchronously. All of these elements are fresh in my mind as I talk with mainstream enterprises who have no idea what API governance is, barely can tell Swagger from OpenAPI, and haven’t learned about Spectral. I needed to load up all of these elements in my head as I reviewed all the current API service and tooling providers that exist out there today. Ultimately I am looking to define the right set of strategies, policies, and rules being applied to machine-readable artifacts that define and configure the business and technical aspects of our API operations at scale using a consistent set of stories. 