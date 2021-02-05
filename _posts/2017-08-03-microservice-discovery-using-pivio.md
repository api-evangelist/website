---
published: true
layout: post
title: Microservice Discovery Using Pivio
date: 2017-08-03T09:00:00.000Z
tags:
  - API Evangelist
  - Discovery
  - Microservices
  - Definitions
image: >-
  https://s3.amazonaws.com/kinlane-productions/pivio/pivio-microservice-documentation-for-your-platform.png
---
<p><a href="http://pivio.io/"><img src="https://s3.amazonaws.com/kinlane-productions/pivio/pivio-microservice-documentation-for-your-platform.png" align="right" width="40%" style="padding: 15px;" /></a></p>I'm finally feeling the ground move in the area of [API discovery](http://discovery.apievangelist.com/) a little bit. It is an area I'm perpetually trying to create my own seismic activity with [APIs.json](http://apisjson.org), but it always makes me happy to see other folks contributing to the conversation in a significant way. My friend Erik Wilde ([@dret](https://twitter.com/dret)) turned me onto [Pivio for microservice discovery](http://pivio.io/), providing a machine readable approach to API discovery that resembles what I've been trying to do with APIs.json, but has several very interesting service-centric characteristics.

According to the project website Pivio is a "description in your source code with all the metadata of your service describing itself. This can be as simple as the name, owner and VCS information as well as useful information about runtime environment, used licenses and service dependencies. Pivio is a service registry for humans." Pivio is a microservice discovery schema, and a web platform for uploading, searching, and viewing your catalog of microservices. It is in alpha version, but already provides a very interesting take on discovery from the microservices perspective.

Pivio begins with a common set of mandatory fields:

- id - Unique id in pivio. You can ask the pivio service for a unique id.
- name - The name of the artifact. This is intended for humans.
- short_name - A very brief name for the service.
- type - The type of this artifact. Values could be service, library or mobile_app.
- owner - Which team is responsible for this artifact.
- description - What does this service do?

Next Pivio begins to break out some interesting collections:

- contact - Who should be contacted if one has a question.
- vcs - Where is the location of source code that runs this service.
- tags - Add tags for organizing each service as part of larger collection.
- lifecycle - In which lifecycle is this component? Only in development, in production or out of service.
- links - All sort of links which might be interesting. Candidates are homepage, buildchain, api docs

Then Pivio breaks out some very useful service-focused collections:

- Provides - What and where does this artifact provides services? description Should be a human readable description. service_name is the unique identification of the particular interface. port, protocol and transport_protocol are self describing.
- Dependences
	- internal - To which other service_name (from provides) services does this service talk?
	- external - To which external target needs this artifact to talk to? This is meant to show if 		this service talks to another one outside of your system, like a public API of another service 		provider 'in the cloud'.
- Service Context
	- belongs_to_bounded_context - General rule is that every service belongs to a bounded context.
	- visibility
    	- private: intended usage is only by the owner
		- public: exposes an api for other owners.
- Runtime
	- cpu - the size of the processor
  	- ram - how much memory it has
	- disk - what is the size of disk
	- host_type - metal, vm, docker
    - network_zone - dmz, backend, core, database
	- environment - development, test, production
- Software Dependencies - Name, versions, licensing of the software behind each of the services.
- Custom extensions - Have your own keys in this configuration you can simply add your own key word/yaml file.

There are overlapping elements of Pivio and API.json, and you can accomplish man similar things with both API discovery formats, but Pivio brings to the table a serious technical view of APIs through a microservice lens. I am really interested in the context, dependencies, and like the runtime, and extension part as well. I think the lifecycle, VCS, and CI/CD aspects of the Pivio schema points to a more meaningful discovery approach in coming years.

Pivio has several supporting open source tools built on the microservices discovery schema which are available from the Github repository at: https://github.com/pivio/:

- Client: https://github.com/pivio/pivio-client
- Server: https://github.com/pivio/pivio-server
- Web: https://github.com/pivio/pivio-web    

I'm not that interested in the client, server, and web applications just yet. I'd like to think more about the context, dependencies, lifecycle, VCS, CI/CD, and the search mechanism they are employing. I'm also going to spend some cycles this week getting up to speed on [JSON Home](https://tools.ietf.org/html/draft-nottingham-json-home-03), as well as Pivio. I've been trying to make some time to learn more about JSON Home lately, but just haven't had the time. Now that I have Pivo on my desk, I'm kind of forced to make sure I can speak intelligenctly to both of these API discovery specification formats.

It is pretty easy to reference a pivio.yaml discovery document from within an APIs.json, and vice versa. They both allow for extensibility using links. After thinking about JSON Home a little bit, I want to try and establish some sort of Venn diagram of JSON Home, Pivio, and APIs.json to better understand where and when you'd want to use each format, and how they can overlap and work together. I feel like the world of APIs is finally maturing to a point where discovery is a growing pain point, so we are going to see more investment in a variety of approaches to helping make it easier to discover, and maintain rich catalogs of microservices and APIs.
