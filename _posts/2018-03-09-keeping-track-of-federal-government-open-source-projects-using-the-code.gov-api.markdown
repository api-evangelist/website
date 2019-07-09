---
published: true
layout: post
title: >-
  Keeping Track Of Federal Government Open Source Projects Using The Code.gov
  API
date: 2018-03-09T09:00:00.000Z
tags:
  - API Evangelist
  - Federal Government
  - Open Source
  - Github
  - Blueprint
image: >-
  https://s3.amazonaws.com/kinlane-productions/federal-government/code-gov/code-gov-screenshot.png
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>Open source software is increasingly driving the federal government, [despite the wishes of companies like Oracle](https://fcw.com/articles/2017/10/04/oracle-rips-18f-usds.aspx). I've been watching an interesting project grow within the federal government to help quantify open source across the federal government called Code.gov, which "leverages the power of code sharing and collaboration to help the US Government cut down on duplicative software development and save millions of taxpayer dollars for the American people." Something I think we can all get behind, when it comes to the collision of technology and government we are seeing play out.

Code.gov allows you to [browse open source projects by government agency](https://code.gov/#/explore-code), see the details for the project, visit the repository, and contact the project owners. The project even has [a help wanted section where you can roll up your sleeves and actually contribute to specific projects](https://code.gov/#/help-wanted), and help agencies push forward their project. You can follow up on what is happening using [the Code.gov roadmap](https://code.gov/#/roadmap), and stay in tune with whats next for the very important project. However, the aspect I'm most interested in, is the evolution of the Code.gov API.

There is [an open source API behind the Code.gov project](https://github.com/GSA/code-gov-api), providing programmatic access to government agencies repositories, the code, types of programming languages used, status, and other critical details for projects. There is [an OpenAPI-driven, Swagger UI documentation for the project](https://api.code.gov/docs/), providing a nice look at the programmatic surface for the project. You can use the API they have provided, or [you can fork the API and operate yourself](https://github.com/GSA/code-gov-api), providing an interesting look at delivering open source APIs that span multiple federal agencies--a blueprint that should be considered for other types of projects.

Code.gov reflects what I want to see come out of the federal government when it comes to technology. Open source. API-driven. Doing on thing, and doing it well. I can see spinoffs of the project emerge, focusing on just the environment, transportation, healthcare, and other verticals, helping shine a light on important projects going on across the federal government, attract and orchestrate talent and partnerships around those projects. Then build valuable dashboards, visualizations, and other applications on top of the APIs behind the project(s). I'll be continuing to document Code.gov's approach, and the API behind it, so that I can have the blueprint ready as part of my federal government API toolbox.
