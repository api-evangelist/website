---
published: true
layout: post
title: 'API-First Development'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/aws-s3-lighthouse-lighthouse-still.jpg
author:
 name: kinlane
tags:
    - API-First
---
This is part of my on-boarding work as Chief Evangelist with Postman. Part of my work to understand how Postman users are putting the platform to work is to process earch one of their use cases in a narrative format. The process helps these things stick in my mind, and since they are all driven by actual feedback and stories from their users, it populates my brain with relevant talking points when I'm engaging with customers.

[API-first](https://www.postman.com/api-first/) is a philosophy and way of life that involves beginning every software capability as an API before you ever begin developer any user interface, or any other element. API-first ensures that all organizational capabilities are defined as simple, intuitive, well-designed API interfaces that can be used and reused across many different applications and systems. Right now, API-first is more of a myth than it is reality in most companies, but regardless, API-first is something many companies strive for when it comes to the development of their software.  
  
Postman has a dedicated [API-First development use case](https://www.postman.com/use-cases/api-first-development) which provides a simple set of steps to consider when it comes to establishing an API-first development process—breaking things down into four separate phases.  
  
**1\. Specification Phase -** Getting to work defining what each API capability will actually do.  
  
**\- Create a new API -** Begin defining a new API fro scratch, not working from existing pattern.  
**\- Write or import a new specification -** Working on an API from an existing API specification.  
  
**2\. Development Phase -** The actual development of an API that is being specified.  
  
**\- Create a mock server -** Turn the specification into a mock representation of the API.  
**\- Create documentation -** Publish documentation for your API using the API specification.  
**\- Debug API -** Track, coordinate and fix bugs and defects in the API being developed.  
  
**3\. Testing Phase -** Ensuring you have the surface area of your API covered by API tests.  
  
**\- Explore the API -** With an API mocked and being developed you can explore its details.  
**\- Write tests using JavaSCript -** Tests defining expected outcomes can be defined for all APIs.  
**\- Verify test results in Collection Runner -** Automate the verification of tests for all APIs.  
  
**4\. Deployment Phase -** Actually realizing and deploying the API capability that is being defined.  
  
**\- Integrate tests in build system through Newman -** Bake all tests for APIs into the CI/CD workflow.  
**\- Deploy to production through your CI/CD pipeline -** Publish code if all the tests pass as part of build.  
**\- Setup monitors to get alerts -** Monitor APIs to ensure the tests are regularly ran and validated.  
  
There are definitely more details in the cracks of API-first, but this list provides you with a high level view of what it is all about. Providing a simple checklist to use when starting API-first conversations across your organization. Each element of the phases above will look different depending on how your organization does what it does, but this basic blueprint is intentionally kept simple to help jumpstart the conversation, and not overwhelm API stakeholders who might not have a lot of experience with the API-first development process.  
  
This [API-first use case blueprint](https://www.postman.com/use-cases/api-first-development) is the most talked about approach to APIs out there today. Companies who have invested in their API-first journey realize how much time, money, and pain can be saved by starting every software application conversation with APIs, and how much more efficient it is to define, mock, and be test-focused as part of their API-first reality. API-first is never as easy as it seems, but once development teams make the investment and begin making API-first a reality, they quickly realize that it was something they should have done a long time ago, and they understand how it can dramatically shift the conversation around how APIs get done across companies, organizations, institutions, and government agencies.