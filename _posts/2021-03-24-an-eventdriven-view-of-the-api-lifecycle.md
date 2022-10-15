---
published: true
layout: post
title: 'An Event-Driven View of the API Lifecycle'
image: https://kinlane-productions2.s3.amazonaws.com/an-eventdriven-view-of-the-api-lifecycle.png
---

I am continuing my quest to define and visualize the API lifecycle across a diverse API toolbox. I am talking to anyone and everyone I possibly can when it comes getting their take on what the API lifecycle is, and what are the ways in which we can make more visible and tangible. I am meeting regularly with the [Solace](https://solace.com/) team to define the API lifecycle across a request and response, as well as an event-driven world. As part of our discussions Jonathan Schabowsky ([@jschabowsky](https://twitter.com/jschabowsky)) shared [his earlier vision of how he sees the event-driven API lifecycle](https://solace.com/blog/event-driven-architecture-demands-event-lifecycle-management/) which I though was worth documenting and including the visualization as part of my wider research.


![](https://kinlane-productions2.s3.amazonaws.com/an-eventdriven-view-of-the-api-lifecycle.png)


Jonathan breaks things down into four main areas or top level groups of the stops along his event-driven API lifecycle, but I think his outline provides a pretty interesting look at the API lifecycle from the view of an event-driven API service providers.


- **Discover**
- 
    - Event Streams:&nbsp;Search and locate events which are of interest
- 
    - Relationships:&nbsp;Understand the relationship between events, their sources and who is consuming them
- **Define**
- 
    - Use Case:&nbsp;Determine desired business outcome
- 
    - Schema:&nbsp;Create business objects that represent the event context
- 
    - Event:&nbsp;Construct event metadata including addressing (topic) and headers
- 
    - Specify Application:&nbsp;link events as inputs and outputs to the business logic
- **Develop**
- 
    - Generate code:&nbsp;Use code generators to create application “scaffolding” based on the application specification
- 
    - Add business logic:&nbsp;Create application which performs the required function
- **Operate**
- 
    - Secure:&nbsp;Enforce authentication and authorization policies
- 
    - Deploy:&nbsp;Start and connect to the runtime event broker
- 
    - Audit:&nbsp;Determine if there are any runtime vs. design time violations
- 
    - Monitor:&nbsp;Understand the utilization of events, schemas and applications based on historical and real-time metrics
- 
    - Improve:&nbsp;Enhance applications, events and schemas; deprecate events that aren’t being utilized


Anytime I look at someone else’s definition of the API lifecycle I immediately see things that are missing, but then I always check myself knowing that my bias is always towards my perspective and view of the API lifecycle at the 500K view. I am not down in the trenches of API operations, although I have visibility into many different types of API operations. I strongly identify with his four areas, and think his individual stops along the lifecycle are simple and purposeful, representing both reality on the ground, but also lean towards having a strategy—-not just responding to what is happening.


I am adding Solace’s view of the API lifecycle to my notebook. The outline and the visual. I am coming closer to establishing a baseline definition for what I’d consider to be a modern API lifecycle, but my biggest challenge is ensuring my definition is simple and relatable to the widest possible audience. I am notorious for providing TOO MUCH INFORMATION, and will lay out over 100 stops along the API lifecycle, which is not what folks need at any point in their journey. My mission is to get more precise in how I talk about the API lifecycle and distill things down to a simple vocabulary that I can then also work to visualize. Ultimately I am looking to get a little more grounded when it comes to how I talk about the API lifecycle, and stop being all over the place, while also work to make sure my definition works for a diverse API toolbox.
