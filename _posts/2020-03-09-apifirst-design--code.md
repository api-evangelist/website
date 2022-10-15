---
published: true
layout: post
title: 'API-First [Design || Code]'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/la_muse-alan-turing-side.jpg
tags:
- API-First
---

[I worked through my thoughts on what API first is](http://apievangelist.com/2020/03/09/what-is-api-first/), which I consider to be the outer layers of what is going on when we use this phrase. I wanted to focus on the technical and business rift that exists in this discussion first, now I want to dive into the more technical core of this phrase, and get to the heart of how developers are going to see this phrase. Depending on the type of developer you are, and your exposure to different aspects of the API industry or API operations within your organization you are going to make different assumptions about what API first is or isn’t. Some will feel it is more just about doing APIs before you build applications, while others are going to see it as being more about going API design first, before you ever write any code. Ultimately I want to establish a definition of API first that is inclusive, and not pushing people out, while also helping me ground how I use the phrase.

### Let’s Recap, What Is API-First?

From the previous post, let’s take a fresh look at what is [API-first](https://www.postman.com/api-first/) from the vantage point of a more technically included stakeholder like architect, developer, or other IT actors. Setting the stage for how API-First \[Code\] can be approached.

*   Before developing a web application, develop an API first
*   Before developing a mobile application, develop an API first
*   Before developing a device application, develop an API first
*   Before attempting any system integration, develop an API first
*   Before directly connecting to a databases, develop an API first

### Also, Why do API-First?

Naturally people will ask why? To help flesh out why API-First matters, before we help separate API-First \[Code\] from API-First \[Design\], let’s look at the benefits of going API-First, then separate code from design approaches might make a little more sense.

*   Allow potential stakeholders to communicate about what is needed before applications are actually build.
*   API will reduce redundancy across multiple types of applications
*   API will allow for reuse across multiple types of applications
*   API will allow for increased efficiency across multiple types of applications.
*   API will allow for centralization of observability across applications
*   API will allow for meeting needs of the known knowns, known unknowns, and help with unknown unknowns.

### API-First \[Code\]

This is the most common approach to API first that I see, because it is the next step towards being API-First from a historically API-last approach. Going API-First by writing code is a perfectly valid way to develop an API, if it doesn’t occur in isolation, and a machine readable artifact is produced from the process. I wanted to consider what an API-First \[Code\] approach might look like, if approached in a general sense across potentially different platforms and programming languages. 

*   **Requirements** - Hopefully you aren’t just diving straight into writing code and there are some requirements dictating what is going on.
*   **Database** - Setting up the database that will exist behind each API, providing a persistent data store for each individual service.
*   **Storage** - You will also need persistent or ephemeral object storage for each API, ensuring that you places to put your heavy objects as well.
*   **Compute** - Establishing where you will run the code you are using to define and develop an API as part of this process.
*   **Scaffolding** - Often times developers are using frameworks, libraries, and other scaffolding for helping deliver common elements of APIs.
*   **Code** - Then within the framework provided, developers are often times writing custom code to do the heavy lifting of each API.
*   **Pipeline** - Modern API delivery systems are leveraging CI/CD processes to help establish reproducible pipelines for the delivery of APIs.
*   **Tests** - Develop tests that ensure the surface area of the API is properly defined, and operates as expected meeting requirements defined.
*   **Definition** - Generation of an OpenAPI, RAML, or other API definition that represents the surface area of the API defined through development.
*   **Collection** - Producing a Postman collection from the generated API definition, enabling users to make calls to the API using the Postman client.
*   **Documentation** - Publishing of up to date and complete documentation for an API using the API definition that was generated from code.
*   **Sharing** - Once you have the API definition, documentation, and collection you can share the link with other stakeholders to get feedback.
*   **Feedback** - Stakeholders can leave feedback by forking definitions or collections, commenting within Postman, or using GitHub / GitLab issues.

There are benefits to being code-first in an API-First world. Once you are done iterating upon the API, there is no development needed to move towards actual deployment. I would say there is additional overhead with setting up the development environment and pipeline in an API-First \[Code\] approach, but I think you also can offset that because it is a process more developers are going to be familiar with over having to learn a new API-First \[Design\] process. This is why API-First \[Code\] still has such a strong foothold, because it is what is familiar and working currently.

### API-First \[Design\]

This is the API-First approach that progressive API believers and developers picture in their minds eye. Where you can define, design, and iterate upon the design of an API and its underlying schema without ever writing code. Simplifying how APIs are designed, leveraging mock servers, and modern tooling and services to bring an API to life in a collaborative way, without writing any code. This is what many organizations are talking about, but few are actually able to achieve due to a variety of concerns from developers.

*   **Assumptions** - Outlining the assumptions being made about what each API should do, providing a simple list of what all stakeholders expect.
*   **Definitions** -  Designing of an OpenAPI or RAML definition describing all details of the surface area of an API, ensuring it meets the assumptions of stakeholders.
*   **Collections** - Generating a Postman collection from the API definition, providing an executable runtime to drive mocks, tests, and docs, as well as manual use in Postman as a client.
*   **Mocks** - Generating mock servers from the Postman collection, mocking all the API paths using example responses defined as part each API definition.
*   **Tests** - Develop tests for each of the assumptions put forth as part of the design process, ensuring there is a check for business and technical assumption.
*   **Documentation** - Publishing of up to date and complete documentation for an API using the collection that was generated from the OpenAPI or RAML.
*   **Sharing** - Once you have the API definition, documentation, and collection you can share the link with other stakeholders to get feedback.
*   **Feedback** - Stakeholders can leave feedback by forking definitions or collections, commenting within Postman, or using GitHub / GitLab issues.

API-First \[Design\] is the preferred approach being peddled across the API sector today. If you believe in the importance of OpenAPI and RAML you feel that you can define a more complete and consistent API than you can with an API-First \[Code\] approach. If you are coming at API development from a more engineering focused background you are more likely to believe the API-First \[Code\] is faster and superior. Really it comes down your comfort level and understanding of API definitions, and whether you place value on code over the API definitions, but in the end, regardless of how you feel on the subject, API-First \[Code\] is still the primary approach to delivering APIs on the ground across enterprise organizations.

### Changing Behavior Is Hard

I firmly believe API-First \[Design\] is a faster and more consistent way to deliver APIs. You can iterate upon them faster, and reduce the length of time for the feedback loop between each version. Code and pipelines aren’t necessary at the design stage. An API-First \[Design\] approach is less intimidating to business users, making the process more inclusive, and not just something that happens in isolation with developers. However, changing  behavior is hard and takes time. The efficiency gains on API-First \[Design\] is mostly likely lost when throwing inexperienced developers into the process, but it is a cost of doing business that will pay off at other stops along the API life cycle like documentation, testing, monitoring, security, and overall governance. API-First \[Design\] will produce more consistent APIs in the end, but again, changing behavior is hard, costly, and takes time, so teams will have to weigh the overall cost.

### Infrastructure Is Costly

![](https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/la-muse-blechlety-old-racks.jpg)

It takes time, resources, and know-how to setup the infrastructure needed to deliver an API. If you are looking to just design and iterate upon each API amongst stakeholders you don’t really need a database, storage, compute, code, and pipelines to get things done. Sure, you’ll need these things before you can move an API from design to production, but you really don’t need these things to iterate upon the design of an API. So I wouldn’t say they aren’t unnecessary, but they are extra costs and potential friction when you are just trying to iterate upon the design of an API. As I stated in the previous paragraph, each organization will have to weigh what is more costly based upon their own infrastructure costs, as well as the cultural and organizational costs of an API-First \[Design\] shift. Even if API-First \[Design\] is more efficient I do not think we can expect every organization will make the shift, and I am not in the business of shaming folks for their practices. We need to acknowledge, and equip API-First \[Code\] teams with what they need to be successful, and work to ensure the API contract produced from all approaches are in alignment.

### API-First \[Design || Code\]

I do not think this is about API-First \[Code\] vs API-First \[Design\]. It should be API-First \[Design || Code\]. Honestly, I’m weighing making it API-First \[Design || Code || Gateway\], because I have seen groups who are defining an API using AWS API Gateway, then exporting an OpenAPI to document, monitor, test, secure, and govern. So I am more concerned with continueing to define what API-First is in a meaningful and pragmatic way that includes as many people as possible in the conversation. This whole series of posts is all about me being able to better articulate what I mean by API-First when discussing APIs with enterprise organizations and within Postman. I am looking to root what I mean with API-First in some solid beliefs and practices that actually match what is going on across the industry. I am not completely convinced that API-First is as well defined as it could / should be, but I feel like I am on a better path when it comes to talking about it in detail.

API-First isn’t as squishy as it was just a couple days ago. I can see the outer layer of meaning with just API-First, and I can see the inner layer with API-First \[Design || Code\]. It has helped me be more precise in what I say, which will hopefully reduce some confusion in at least the conversations I am having. I don’t have much faith that everyone in the API sector will immediately be enlightened, but it will help me produce better stories, tutorials, talks, and webinars that show what is possible with an API-First mindset, even if you are API-First \[Code\], aspiring to be API-First \[Design\], or already made the conversion to API-First \[Design\]. I am on firmer ground, but my API-First storytelling journey is only beginning, and I predict I will be telling some of the same stories over and over the next couple years to help others realize the state of their API delivery process, and further optimize, and move towards a more efficient and effective way of doing things no matter which approach they end up choosing.