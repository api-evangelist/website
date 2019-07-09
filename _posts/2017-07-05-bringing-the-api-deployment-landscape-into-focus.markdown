---
published: true
Title: Bringing The API Deployment Landscape Into Focus
layout: post
title: Bringing The API Deployment Landscape Into Focus
date: 2017-07-05T09:00:00.000Z
tags:
  - API Evangelist
  - Deployment
  - Virtualization
  - Data
  - Database
  - Spreadsheet
  - Search
  - Scraping
  - Proxy
  - Rogue
  - Microservices
  - Containers
  - Serverless
  - Real Time
  - Devices
  - Marketplaces
  - Webhooks
  - Orchestration
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-api-deployment.png'
---
<p><a href="http://deployment.apievangelist.com/"><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-api-deployment.png" align="right" width="30%" style="padding: 15px;" /></a></p>I am finally getting the time to invest more into the rest of my API industry guides, which involves deep dives into core areas of my research like API <a href="http://definitions.apievangelist.com/">definitions</a>, <a href="http://design.apievangelist.com/">design</a>, and now <a href="http://deployment.apievangelist.com/">deployment</a>. The outline for my API deployment research has begun to come into focus and looks like it will rival my API management research in size.

With this release, I am looking to help onboard some of my less technical readers with API deployment. Not the technical details, but the big picture, so I wanted to start with some simple questions, to help prime the discussion around API development.

- Where? - Where are APIs being deployed. On-premise, and in the clouds. Traditional website hosting, and even containerized and serverless API deployment.
- How? - What technologies are being used to deploy APIs? From using spreadsheets, document and file stores, or the central database. Also thinking smaller with microservices, containes, and serverless.
- Who? - Who will be doing the deployment? Of course, IT and developers groups will be leading the charge, but increasingly business users are leveraging new solutions to play a significant role in how APIs are deployed.

**The Role Of API Definitions**
While not every deployment will be auto-generated using an API definition like OpenAPI, API definitions are increasingly playing a lead role as the contract that doesn't just deploy an API, but sets the stage for API documentation, testing, monitoring, and a number of other stops along the API lifecycle. I want to make sure to point out in my API deployment research that API definitions aren't just overlapping with deploying APIs, they are essential to connect API deployments with the rest of the API lifecycle.

**Using Open Source Frameworks**
Early on in this research guide I am focusing on the most common way for developers to deploy an API, using an open source API framework. This is how I deploy my APIs, and there are an increasing number of open source API frameworks available out there, in a variety of programming languages. In this round I am taking the time to highlight at least six separate frameworks in the top programming languages where I am seeing sustained deployment of APIs using a framework. I don't take a stance on any single API framework, but I do keep an eye on which ones are still active, and enjoying usag bey developers.

**Deployment In The Cloud**
After frameworks, I am making sure to highlight some of the leading approaches to deploying APIs in the cloud, going beyond just a server and framework, and leveraging the next generation of API deployment service providers. I want to make sure that both developers and business users know that there are a growing number of service providers who are willing to assist with deployment, and with some of them, no coding is even necessary. While I still like hand-rolling my APIs using my peferred framework, when it comes to some simpler, more utility APIs, I prefer offloading the heavy lifting to a cloud service, and save me the time getting my hands dirty.

**Essential Ingredients for Deployment**
Whether in the cloud, on-premise, or even on device and even the network, there are some essential ingredients to deploying APIs. In my API deployment guide I wanted to make sure and spend some time focusing on the essential ingredients every API provider will have to think about.

-Compute - The base ingredient for any API, providing the compute under the hood. Whether its baremetal, cloud instances, or serverless, you will need a consistent compute strategy to deploy APIs at any scale.
-Storage - Next, I want to make sure my readers are thinking about a comprehensive storage strategy that spans all API operations, and hopefully multiple locations and providers.
-DNS - Then I spend some time focusing on the frontline of API deployment--DNS. In todays online environment DNS is more than just addressing for APIs, it is also security.
-Encryption - I also make sure encryption is baked in to all API deployment by default in both transit, and storage.

**Some Of The Motivations Behind Deploying APIs**
In previous API deployment guides I usually just listed the services, tools, and other resources I had been aggregating as part of my monitoring of the API space. Slowly I have begun to organize these into a variety of buckets that help speak to many of the motivations I encounter when it comes to deploying APIs. While not a perfect way to look at API deployment, it helps me thinking about the many reasons people are deploying APIs, and craft a narrative, and provide a guide for others to follow, that is potentially aligned with their own motivations.

- Geographic - Thinking about the increasing pressure to deploy APIs in specific geographic regions, leveraging the expansion of the leading cloud providers.
- Virtualization - Considering the fact that not all APIs are meant for production and there is a lot to be learned when it comes to mocking and virtualizing APIs.
- Data - Looking at the simplest of Create, Read, Update, and Delete (CRUD) APIs, and how data is being made more accessible by deploying APIs.
- Database - Also looking at how APIs are beign deployed from relational, noSQL, and other data sources--providing the most common way for APIs to be deployed.
- Spreadsheet - I wanted to make sure and not overlook the ability to deploy APIs directly from a spreadsheet making APIs are within reach of business users.
- Search - Looking at how document and content stores are being indexed and made searchable, browsable, and accessible using APIs.
- Scraping - Another often overlooked way of deploying an API, from the scraped content of other sites--an approach that is alive and well.
- Proxy - Evolving beyond early gateways, using a proxy is still a valid way to deploy an API from existing services.
- Rogue - I also wanted to think more about some of the rogue API deployments I've seen out there, where passionate developers reverse engineer mobile apps to deploy a rogue API.
- Microservices - Microservices has provided an interesting motivation for deploying APIs--one that potentially can provide small, very useful and focused API deployments.
- Containers - One of the evolutions in compute that has helped drive the microservices conversation is the containerization of everything, something that compliments the world of APis very well.
- Serverless - Augmenting the microservices and container conversation, serverless is motivating many to think differently about how APIs are being deployed.
- Real Time - Thinking briefly about real time approaches to APIs, something I will be expanding on in future releases, and thinking more about HTTP/2 and evented approaches to API deployment.
- Devices - Considering how APis are beign deployed on device, when it comes to Internet of Things, industrial deployments, as well as even at the network level.
- Marketplaces - Thinking about the role API marketplaces like Mashape (now RapidAPI) play in the decision to deploy APIs, and how other cloud providers like AWS, Google, and Azure will play in this discussion.
- Webhooks - Thinking of API deployment as a two way street. Adding webhooks into the discussion and making sure we are thinking about how webhooks can alleviate the load on APIs, and push data and content to external locations.
- Orchestration - Considering the impact of continous integration and deployment on API deploy specifically, and looking at it through the lens of the API lifecycle.

I feel like API deployment is still all over the place. The mandate for API management was much better articulated by API service providers like Mashery, 3Scale, and Apigee. Nobody has taken the lead when it came to API deployment. Service providers like DreamFactory and Restlet have kicked ass when it comes to not just API management, but making sure API deployment was also part of the puzzle. Newer API service providers like Tyk are also pusing the envelope, but I still don't have the number of API deployment providers I'd like, when it comes to referring my readers. It isn't a coincidence that DreamFactory, Restlet, and Tyk are API Evangelist partners, it is because they have the services I want to be able to recommend to my readers.

This is the first time I have felt like <a href="http://deployment.apievangelist.com/">my API deployment research</a> has been in any sort of focus. I carved this layer of my research of <a href="http://management.apievangelist.com/">my API management research</a> some years ago, but I really couldn't articulate it very well beyond just open source frameworks, and the emerging cloud service providers. After I publish this edition of my API deployment guide I'm going to spend some time in the 17 areas of my research listed above. All these areas are heavily focused on API deployment, but I also think they are all worth looking at individually, so that I can better understand where they also intersect with other areas like management, testing, monitoring, security, and other stops along the API lifecycle.
