---
published: true
layout: post
title: Some Microservice Thoughts Around My Human Services API Work
date: 2017-08-14T12:00:00.000Z
tags:
  - API Evangelist
  - Microservices
  - HSDS
  - HSDA
  - City Government
  - Github
  - Lifecycle
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/algo-microservices.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/algo-microservices.jpg" align="right" width="40%" style="padding: 15px;" /></p>[The Human Services Data API I have been working on is about defining a set of API paths for working with organizations, locations, and services that are delivering human services in cities around the world](http://org.open.referral.adopta.agency/). As I'm working to evolve the OpenAPI for the Human Services Data API (HSDA), I'm constantly mindful of bloat, unnecessary expansion of features, and always working to separate things by concern. My thoughts have evolved this due to [a hackathon I attended this week in San Francisco where a team at Optmizely worked to decouple an existing human services application from its backend and help teach it to speak Human Services Data Specification (HSDS)](http://apievangelist.com/2017/08/11/a-hack-day-event-to-help-the-link-sf-app-speak-human-services-data-specification/)--allowing it to speak a common language around the services that us humans depend on daily.

As the hackathon team was decoupling the single page application (React) from the API backend (Firebase) I took the API calls behind and published to Github as two JSON files. [One of the files was locations, which contained 217 human service locations in San Francisco](https://raw.githubusercontent.com/optimizely/linksf/master/core/sf_location.json), and metadata, which contained a handful of categories being used to organize and display the locations. In this situation, there is no notion of an organization, just 217 locations, offering human services across five categories. This legacy application, and forward engineering hackathon project was quickly becoming a microservices project, ironically it is a microservice project that was about delivering human services. ;-)

Looking at this unfolding project through a microservices lens, I needed to provide a single service. In the context [of Link-SF](https://link-sf.com/), the original project, I needed to offer a service that would deliver 217 locations where people can find human services in the areas of food, housing, hygiene, medical, and technology via an web, or mobile application. To help me achieve my goals I began to step through each of the steps of the lifecycle of any self-contained microservices:

- Github - Each of my services begins with a Github repository, [so I created a new repo](https://github.com/adopta-agency/human-services-link/).
- Definitions - I defined the service I wanted as [an OpenAPI](https://github.com/adopta-agency/human-services-link/blob/master/_data/api-commons/openapi.yaml).
- Design - I worked to keep the design of it as simple as I possibly can.
- DNS - I relied on Github's DNS for this service, but may setup my own subdomain.
- Database - I published a YAML data file into the data folder for the Github repository, acting as the database for my service, leverage Github and Jekyll for helping me broker database connectivity.
- Deployment - I deployed [a simple static JSON API](https://adopta-agency.github.io/human-services-link/apis/locations.json) driven from the locations YAML store.
- Management - I am using Github as the management platform for my API, helping me deploy and manage consumption of my service. I'm using the Github API as the programmatic layer for managing my service operations to help me continuously deploy and integrate with this service.
- Portal - I am using Github pages as the portal for my service, providing both human and programmatic access to my service, making human service locations more available.
- Documentation - I published static HTML, and Swagger UI documentation for the service.
- Support - I have published a support page, and will be providing support via Github issues, Twitter, and email.
- Communications - I have a blog published, and will be publishing the story of the service using the Jekyll CMS blogging solution.
- Caching - The API, portal, and all aspects of the service I've launched is being cached by Github, riding on the backs of their Content Delivery Network (CDN).
- Reliability - While Github has been known to have stability issues, it is still some of the most reliable way to host data and API driven services.
- Encryption - I'm leveraging the Github DNS, and using their encryption in transit by default. I will be using my own subdomain and encryption in the future.
- Security - I'm offloading platform security to Github. They have more resources than I do. I'm also looking to keep things more secure be keeping my services as static as possible.
- Testing - I am setting up a series of monitors to ensure the service stays available, and delivering expected data and promised schema. I will be publishing a status update and history page.
- Transparency - Everything involved with my service runs on Github, either as a public or private repository, with the entire lifecycle transparent publicly, or privately to whoever is given access to the repository using Github.
- Observability - The entire service runs on Github. The entire lifecycle is observable in the Github history, and leverage their existing infrastructure for identity and access management (IAM), and continuous integration and deployment.
- Discovery - There is an APIs.json available in the root of the project, providing a machine readable index of the schema, data, API, and other resources available via this service.
- Client - I've published an HTML / JavaScript client on the home page of the project, with an editor for managing the data, which leverages the Github API for reading and writing data to the services repository.

I'm calling my new service, born out of the Link-SF legacy application [Human Services Link](https://adopta-agency.github.io/human-services-link/). However, the only thing remaining of the Link-SF application is the data. I've forward engineered the schema, API, and web interface to all run on Github as a single, yet decoupled service. It is a reduction of the overall Human Services Data Specification (HSDS) schema, focusing in on just providing services at a handful of locations, reducing complexity and scope, to deliver a specific service--do one thing and do it well. I will be launching an Amazon EC2, and containerized version of this human services microservice, but I wanted to look at this one incarnation of it though the microservices lens. Sure, its not your classic microservices definition, but I think it holds up to a microservices test, it just makes some different architectural choices than the rest of the community might have made.

My human services microservice definition solves a single problem, for a specific type of end-user. It was originally geographically limited to San Francisco, but with with this evolution I've made sure there is a state/province field, as well as country, so that solution can be deployed for any city. I want the compute, database, DNS, API, portal, docs, and UI elements and admin tools to all be self contained for the delivery of a single microservice, but I wanted it all forkable, so you could launch this service over and over, in any city around the globe. There is still a lot of work to be done on this project before it is ready for prime time, but I've planted the seeds when it comes to delivering microservices in my world this way. I'm hoping it will be something I can't ignore, and will keep pushing forward as part of my overall vision of how we can deliver sustainable API driven services.

I really like the static nature of this approach. I really like the forkability of this approach, and how you can use Github to separate out concerns by organization. I really like how I can offload much of the operation of my backend to Github, including security, CDN, and scalability / reliability. It is definitely not a pattern everyone should be following when doing microservices, but it does provide a static forkable pattern that can really help keep services very focused and self contained, but available to work in service of a bigger architectural picture. I'll keep playing around with this approach to delivering human service microservices, and see what I can push forward and make stick. I'm hoping it can providing a low coast way for cash strapped municipalities to better deliver up to date information about human services to their entire population.
