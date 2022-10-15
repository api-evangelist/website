---
published: true
layout: post
title: 'A Mix of Blueprints for the API Lifecycle'
image: https://apis.how/images/lifecycle.png
tags:
    - Lifecycle
    - Blueprints
---

I am been doing a lot of research into what the API lifecycle can be, pulling together what I’ve gathered over recent conversations, but then also working to lay the foundation for driving the next wave of conversations around what the API lifecycle is across many different types of organizations and industries. [I was able to get this research to a state where I am going to be opening it up to w wider audience for feedback](https://apis.how/), and to help evolve the content, and other resources. I’ve chosen to use a very modular approach to defining the API lifecycle, establishing many actions and elements from across the API lifecycle that can be organized into a variety of blueprints. Encouraging reuse of some of the more common elements and actions we take across the lifecycle into blueprints that can be shared via the website, PDFs, and eventually via flowcharts and presentations. To jump start discussions I have published fourteen separate blueprints which provide different perspective of the API lifecycle, helping folks prioritize the development and automation around new and active APIs across a known API lifecycle.

### Base
While there are many perspectives of what the API lifecycle is, we are working to define the base layer, or maybe the starting point that folks should be considering as they work to define and standardize how they approach the API lifecycle.

- [**The Base of the API Lifecycle**](https://apis.how/blueprints/base/) - This blueprint provides a look at the base of the API lifecycle, laying the foundation for a API lifecycle you'll see variations of across this site, with different views depending on where you enter the lifecycle, and what your priorities are within your organization and teams.

### New APIs
When I talk with folks about the API lifecycle people overwhelmingly talk about the lifecycle for creating new APIs, which in my opinion reflects are more forward moving view of how we deliver APIs within our organizations, representing greener field development.

- [**New API Using the OpenAPI Specification**](https://apis.how/blueprints/new-api-using-the-openapi-specification/) - This provides a blueprint for beginning the API lifecycle by designing a new API using an OpenAPI, showing one possible lifecycle from end to end. Approaching the API lifecycle in a design-first way, while ensuring all the other essential areas of the API lifecycle are present.
        
- [**New API Using the AsyncAPI Specification**](https://apis.how/blueprints/new-api-using-the-asyncapi-specification/) - This is a blueprint to try and define a new event-driven API using AsyncAPI, pushing the boundaries of this API lifecycle blueprint to include multiple protocols, patterns, and ensure that there can be a well defined API lifecycle across a diverse set of approaches to delivering APIs.
        
- [**Prototype a New API Using a Postman Collection**](https://apis.how/blueprints/prototype-a-new-api-using-collection/) - Bringing a new API to life in a design-first way using a Postman collection to prototype the API, then an OpenAPI contract to help guide the API throughout the rest of it's lifecycle--establishing a working design of an API before you define the contract for how it will work.
        
- [**Creating a New GraphQL API**](https://apis.how/blueprints/creating-a-new-graphql-api/) - This is a blueprint for pushing this API lifecycle blueprint to also work for new GraphQL APIs, identifying the steps needed to define and stand up a new GraphQL API, but then apply a consistent well defined lifecycle to how the API is moved forward and supported in production.

### Existing APIs
Moving beyond the green field development, I started with three blueprints that propose how a more standardized API lifecycle can be established for existing APIs, helping push legacy APIs to be more consistent with more recent API efforts, and applying common elements.

- [**Manually Define Collection for Existing API**](https://apis.how/blueprints/manually-define-collection-for-an-existing-api/) - This is a blueprint for how to manually create a collection for an existing API, transferring details of each request from documentation to a collection, applying authentication, then continuing to explore and troubleshoot until you have a complete and documented collection for an API.
        
- [**Generate OpenAPI Using Code Annotations**](https://apis.how/blueprints/generate-openapi-from-code-annotations/) - This is a blueprint for entering the API lifecycle by generating an OpenAPI using code annotations, taking a code-first approach to bringing each API to life, while still ensuring that there is a contract to help guide the API across a more standardized API lifecycle.
        
- [**Import WSDL for an Existing SOAP Web Service**](https://apis.how/blueprints/import-wsdl-for-an-existing-soap-web-service/) - This is a blueprint for entering a standardized API lifecycle using a WSDL for an existing web service, acknowledging that SOAP still has it's place in many enterprise environments, but a common API lifecycle including documentation, testing, and other elements is still needed.

### Reverse Engineer
Further moving into to the realm of existing APIs, but acknowledging that many APIs are created for a single purpose, helping power desktop, web, mobile, and device applications, so I wanted to make sure we have some blueprints to help bring these hidden APIs into a more standardized API lifecycle.

- [**Generate Collection From Web Application API**](https://apis.how/blueprints/generate-collection-from-web-application/) - This blueprint introduces how APIs behind web applications can be reverse engineered and defined as a collection so that documentation, testing, and other common areas of the API lifecycle can be applied to help stabilize the APIs we depend on behind our applications.
        
- [**Generate Collection From Mobile Application API**](https://apis.how/blueprints/generate-collection-from-mobile-application/) - This blueprint introduces how APIs behind mobile applications can be reverse engineered and defined as a collection so that documentation, testing, and other common areas of the API lifecycle can be applied to help stabilize the APIs we depend on behind our applications.

### Automation
The API lifecycle isn’t just about moving forward new or existing APIs it can also be about automating the producing, sustainment, and consumption across APIs, so I wanted to make sure to get to work on some common blueprints for what is involved in API automation.

- [**Build a Business Workflow**](https://apis.how/blueprints/business-workflows/) - This API lifecycle blueprint focuses on defining common business workflows, then automating around these well defined scenarios. Defining collections across multiple APIs, including authentication, scripting, data, environments, then automate using monitors and pipelines.
        
- [**Test Automation**](https://apis.how/blueprints/test-automation/) - Test automation is essential for delivering reliable and consistent APIs at scale across the enterprise. This is a blueprint for walking through the base of how test automation can work as part of a well defined API lifecycle, helping teams standardize how they approach testing APIs.

### Governance
One last area I have made some investment in is around the governance of the API lifecycle, providing a very different, but extremely critical view of the API lifecycle, acknowledging that we will never be able to properly govern a lifecycle that isn’t well defined.

- [**High Level API Governance**](https://apis.how/blueprints/high-level-governance/) - A blueprint for approach the governance of APIs from the top down, establishing a higher level strategy for defining what governance is, and then helping spread guidance across teams that helps enable them to deliver more consistent APIs across a more consistent API lifecycle no matter what type of API they are delivering.=
        
- [**Low Level API Governance**](https://apis.how/blueprints/low-level-governance/) - A blueprint for approach the governance of APIs beginning with each individual API by individual developers, setting API governance into motion at the lowest level by a single or group of developers, acknowledging that governance will only get you so far at this level, but in many organizations it might sense to start at this level.

This project [runs on Github and all of the blueprints, elements, and actions published as YAML so they can be reused, remixed, and made available](https://github.com/postman-open-technologies/lifecycle) for presentation in many different ways. There is also a discussion setup for each blueprint with a link to the discussion from the detail page. There is a lot more work ahead in fleshing out each element and action with more content and resources, but it provides a pretty decent foundation to ground the conversations I am having. I have calls scheduled with a variety of API Providers and service providers regarding how they see the API lifecycle over the next couple of weeks. If you’d like to share your vision of what the API lifecycle is at your organization, or of the clients that you support as part of your products, services, or consultancy, I’d love to schedule 30 minutes to discuss more ([Just Tweet at Me](https://twitter.com/kinlane)). I’ll be creating a blueprint snapshot for every conversation I am having, then formalizing as many of them possible for showcasing and release as part of the project in coming months.