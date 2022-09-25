---
published: true
layout: post
title: >-
  Concerns Around Managing Many Microservice Repositories And Going With A Mono
  Repo
date: 2018-07-09T09:00:00.000Z
tags:
  - API Evangelist
  - Microservices
  - Orchestration
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/lacloudydaypano_blue_circuit.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/lacloudydaypano_blue_circuit.jpg" width="100%" align="center"></p>About half of the teams I work with on microservices strategy are beginning to freak out about the number repositories they have, and someone is regularly bringing up the subject of having a mono repo. Which is usually a sign for me that a group is not ready for doing the hard work involved with microservices, but also shows a lack of ability to think, act, and respond to things in a distributed way. It can be a challenge to manage many different repositories, but with a decoupled awareness of the sprawl that can exist, and some adjustments and aggregation to your strategy it can be doable, even for a small team.
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/lacloudydaypano_blue_circuit_3.jpg" width="100%" align="center"></p>
The most import part of sticking to multiple repositories is for the sake of the code. Keeping services decoupled in reality, not just name is extremely important. Allowing the code behind each service to have its own repository, and build a pipeline that keeps things more efficient, nimble, and fast. Each service you layer into a mono repo will be one more chunk of time needed when it comes to builds, and understanding what is going on with the codebase. I know there are a growing number of strategies for managing mono repos efficiently, but it is something that will begin to work against your overall decoupling efforts, and you are better off having a distributed strategy in place, because code is only the first place you'll have to battle centralization, in the name of a more distributed reality.
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/lacloudydaypano_blue_circuit_4.jpg" width="100%" align="center"></p>
Github, Gitlab, and Bitbucket all have an API, which makes all of your repositories accessible in a programmatic way. If you are building microservices, and working towards a distributed way of doing things, it seems like you should be using APIs to aggregate and automate your reality. It is pretty easy to setup an organization for each grouping of microservices, and setup a single master or control repository where you can aggregate information, and activity across all repository--using Github Pages (or other static implementation) as a central dashboard, and command center for managing and containing microservice sprawl. Your repository structure should reflect your wider microservices organization strategy, and all the moving parts should be allowed to operated in a distribution fashion, not just the code, but also the conversation, support, and other essential elements.
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/lacloudydaypano_blue_circuit_5.jpg" width="100%" align="center"></p>
I'm spending more time learning about Kubernetes, and studying how microservices are being orchestrated. Like other aspects of the API world, I'm going to focus on not just the code, but also the other communications, support, dependencies, security, testing, and critical building blocks of delivering APIs. I feel like many folks Im talking with are getting hung up on the distributed nature of everything else, while trying to distribute and decouple their code base. Microservices are definitely not easy to do, and decoupling isn't an automatic solution to all our problems. From what I am seeing, it is opening up more problems than it is solving in some of the organizations I am working with, and causing a lot of anxiety about the scope of what teams will have to tackle when trying to find success with microservices across their increasingly distributed organizations.
