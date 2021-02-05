---
published: true
layout: post
title: From CI/CD To A Continuous Everything (CE) Workflow
date: 2017-12-19T13:00:00.000Z
tags:
  - API Evangelist
  - Orchestration
  - Governance
  - Lifecycle
  - Documentation
  - Communication
  - Support
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/27_93_800_500_0_max_0_-1_-1.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/27_93_800_500_0_max_0_-1_-1.jpg" align="right" width="45%" style="padding: 15px;" /></p>I am evaluating an existing continuous integration and deployment workflow to make recommendations regarding how they can evolve to service their growing API lifecycle. This is an area of my research that spans multiple areas of my work, but I tend to house under what I call [API orchestration](http://orchestration.apievangelist.com/). I try to always step back and look at an evolving area of the tech space as part of the big picture, and attempt to look beyond any individual company, or even the wider industry hype in place that is moving something forward. I see the clear technical benefits of CI/CD, and I see the business benefits of it as well, but I haven't always been convinced of it as a standalone thing, and have spent the last couple of years trying understand how it fits into the bigger picture.

As I've been consulting with several enterprise groups working to adopt a CI/CD mindset, and having similar conversations with government agencies, I'm beginning to see the bigger picture of "continuous", and starting to decouple it from just deployment and even integration. The first thing that is assumed, not always evident for newbies, but is always a default--is testing. You alway test before you integrate or deploy, right? As I watch groups adopt I'm seeing them struggle with making sure there are other things I feel are an obvious part of the API lifecycle, but aren't default in a CI/CD mindset, but quickly are being plugged in--things like security, licensing, documentation, discovery, support, communications, etc. In the end, I think us technologists are good at focusing on the tech innovations, but often move right past many of the other things that are essential for the business world. I see this happening with containers, microservices, Kubernetes, Kafka, and other fast moving trends.

I guess the point I want to make is that there is more to a pipeline than just deployment, integration, and testing. We need to make sure that documentation, discovery, security, and other essentials are baked in by default. Otherwise us techies might be continuously forgetting about these aspects, and the newbies might be continuously frustrated that these things aren't present. We need to make sure we are continuously documenting, continuously securing, and continuously communicating around training, and our continuously evolving (and sharing) our road maps. I'm sure what I'm saying isn't anything new for the CI/CD veterans, but I'm trying to onboard new folks with the concept, and as with most areas of the tech sector I find the naming and on-boarding materials fairly deficient in possessing all the concepts large organizations are needing to make the shift.

I'm thinking I'm going to be merging my API orchestration (CI/CD) research with my overall API lifecycle research, thinking deeply about how everything from definition to deprecation fits into the pipeline. I feel like CI/CD has been highly focused on the technology of evolving how we deploy and integrate (rightfully so) for some time now, and with adoption expanding we need to zoom out and think about everything else organizations will need to be successful. I see CI/CD as being essential to decoupling the monolith, and changing culture at some of the large organizations I'm working with. I want these folks to be successful, and not fall into the trappings of only thinking about the tech, but also consider the business and political implications involved with being able to move from annual or quarterly deployments and integrations, to where they can do things in weeks, or even days.
