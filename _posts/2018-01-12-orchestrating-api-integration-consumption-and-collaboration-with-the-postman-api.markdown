---
published: true
layout: post
title: >-
  Orchestrating API Integration, Consumption, and Collaboration with the Postman
  API
date: 2018-01-12T13:00:00.000Z
tags:
  - API Evangelist
  - Clients
  - Testing
  - Monitoring
image: 'https://s3.amazonaws.com/kinlane-productions/postman/the-postman-api.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/postman/the-postman-api.png" align="right" width="45%" style="padding: 15px;" /></p>You hear me say it all the time--if you are selling services and tooling to the API sector, you should have an API. In support of this way of thinking I like to highlight the API service providers I work with who follow this philosophy, and today's example is from (Postman](https://getpostman.com). If you aren't familiar with Postman, I recommend getting acquainted. It is an indispensable tool for integrating, consuming, and collaborating around the APIs you depend on, and are developing. Postman is essential to working with APIs in 2018, no matter whether you are developing them, or integrating with 3rd party APIs.

Further amplifying the usefulness of Postman as a client tool, [the Postman API](https://docs.api.getpostman.com) reflects the heart of what Postman does as not just a client, but a complete life cycle tool. The Postman API provides five separate APIs, allowing you orchestration your API integration, consumption, and collaboration environment.

- [**Collections**](https://docs.api.getpostman.com/#8ca888b7-ef54-f3b4-312f-3f3e2e2cf04e) - The /collections endpoint returns a list of all collections that are accessible by you. The list includes your own collections and the collections that you have subscribed to.
- [**Environments**](https://docs.api.getpostman.com/#a237ffbe-0444-b394-a2c4-b99f691931cf) - The /environments endpoint returns a list of all environments that belong to you. The response contains an array of environments' information containing the name, id, owner and uid of each environment.
- [**Mocks**](https://docs.api.getpostman.com/#ef6bef63-0b8e-1a70-dd88-c7c1b94f8dab) - This endpoint fetches all the mocks that you have created.
- [**Monitors**](https://docs.api.getpostman.com/#993648ea-7b28-9636-f532-1ef8a74ff093) - The /monitors endpoint returns a list of all monitors that are accessible by you. The response contains an array of monitors information containing the name, id, owner and uid of each monitor.
- [**User**](https://docs.api.getpostman.com/#1ddc0a3c-d5ff-b062-d0fb-9e6086be0536) - The /me endpoint allows you to fetch relevant information pertaining to the API Key being used.

The user, collections, and environments APIs reflect the heart of the Postman API client, where mocks and monitors reflects its move to be a full API life cycle solution. This stack of APIs, and the Postman as a client tool reflects how API development, as well as API operation should be conducted. You should be maintaining collections of APIs that exist within many environments, and you should always be mocking interfaces as you are defining, designing, and developing them. You should then also be monitoring all the APIs you depend--whether or not the APIs are yours. If you depend on APIs, you should be monitoring them.

I've long been advocating that someone development an API environment management solution for API developers, providing a single place we can define, store, and share the configuration, keys, and other aspects of integration with the APIs we depend on. The Postman collections and environment APIs is essentially this, plus you get all the added benefits of the services and tooling that already exist as part of the platform. Demonstrating why as an API service provider, you want to be following your own advice and having an API, because you never know when the core of your solution, or even one of the features could potentially become baked into other applications and services, and be the next killer feature developers can't do without.
