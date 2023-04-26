---
published: true
layout: post
title: 'Avoiding Complexity and Just Deploying YAML, JSON, and CSV APIs Using GitHub or GitLab'
date: 2019-06-24T12:00:00.000Z
tags:
  - API Evangelist
  - Complexity
  - YAML
  - JSON
  - CSV
image: >-
  https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/meadowbutterfly-meadow-butterfly-internet-numbers.jpg
author:
 name: kinlane
tags:
    - None
---
I find that a significant portion of I should be doing when defining, designing, developing, and delivering an API is all of avoiding complexity. Every step away along the API journey I am faced with opportunities to introduce complexity, forcing me to constantly question and say no to architectural design decisions. Even after crafting some pretty crafty APIs in my day, I keep coming back to JSON or YAML within Git, as the most sensible API architectural decision I can make. 

Git, with JSON and YAML stored within a repository, fronted with a Jekyll front-end does much of what I need. The challenge with selling this concept to others is that it is a static publish approach to APIs, instead of a dynamic pull of relevant data. This approach isn’t for every API solution, I’m not in the business selling one API solution to solve all of our problems. However, for many of the API uses I’m building for, a static Git-driven approach to publishing machine readable JSON or YAML data is a perfect low cost, low tech solution to delivering APIs.

A Git repository hosted on GitHub or GitLab will store a significant amount of JSON, YAML, or CSV data. Something you can easily shard across multiple repositories within an organization / group, as well as across many repositories within many organization / groups. Both GitHub and GitLab offer free solutions, essentially letting you publish as many repositories as you want. As I said earlier, this is not a solution to all API needs, but when I’m looking to introduce some constraints to keep things low cost, simple, and easy to use and manage—a Git-driven API is definitely worth considering. However, going static for your API will force you to think about how you automate the lifecycle of your data, content, and other resources.

The easiest way to manage JSON, CSV, or YAML data you have on GitHub or GitLab is to use the GitHub or GitLab API, allowing you to update individual JSON, CSV, or YAML files in real-time. If you want to do it in batch process by checking out the repository, making all the changes you want and committing back as a single Git commit using the command line—I’ve automated a number of these to reduce the number of API calls I’m making. If you want to put in an editorial layer you can require submission via pull / merge request, requiring there be multiple eyes on each update to the data behind a static API. It is an imperative, and a declarative API, with an open source approval workflow by default—all for free.

Once you have your data in the Git repository you can make it available using the RAW links provided by GitHub or GitLab. However, I prefer to publish a Jekyll front-end, which can act as the portal landing page for the site, but then you can also manually or dynamically create neat paths that route users to your data using sensible URLs—the best part is you can add a cname and publish your own domain. Making your API accessible to humans, while also providing intuitive, easy to follow URLs to the static data that has been published using the GitHub or GitLab API, or the underlying Git infrastructure to do in bulk.

This is the cheapest, most productive way to deliver simple data and content APIs. The biggest challenges are that you have to begin thinking a little differently about how you manage your data. You have to move from a pull to a push way of delivering data, and embrace the existing CI/CD way of doing things embraced by both GitHub and GitLab. For me, using Git to deliver APIs provides a poor mans way to not just deliver an API, but also ensure it is secure, performant, and something I can automate the management of using existing tools developers are depending on. Over the last couple of years I’ve pushed the limits of this approach by publishing thousands of OpenAPI-driven API discovery portals, and it is something I’m going to be refining and using as the default layer for delivering simple APIs that allow me to avoid unnecessary complexity.
