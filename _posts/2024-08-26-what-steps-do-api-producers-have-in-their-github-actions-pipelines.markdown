---
published: true
layout: post
title: 'What Steps Do API Producers Have in Their GitHub Actions Pipelines'
tags:
  - Pain
  - Friction
  - Solutions
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/yellow-journalism-gears-pipes-plumbing.jpg
---
I have been studying the [GitHub repositories of API producers who choose to manage their OpenAPIs via a public repository](https://apievangelist.com/2024/07/08/more-examples-of-using-github-to-manage-your-openapi/). I have broken down all the properties of these repositories to help me better understand how producers are managing their OpenAPI, but also how they perceive or their consumers are requesting different things derived from and surrounding a valid OpenAPI definition for each API represented.

The next wave of work I am doing involves studying how these API producers are using their CI/CD pipelines, more specifically their GitHub Actions to validate and automate their work surrounding OpenAPI. I am refreshing my understanding of how GitHub Actions works, but also working to understand what matters to API producers, and the how and why of their GitHub Actions pipelines. Looking at the [Digital Oceans pipeline](https://github.com/digitalocean/openapi/pull/903), they have:

- Validate Their OpenAPI Spec
- Bundle Their OpenAPI Spec
- Generate Preview of OpenAPI Spec
- Run GitGuardian Security Checks
- Generate & Validate Python Client

I am going to go through all of the GitHub repositories I have documented as part of this research and evaluate their pipelines in a similar way. I will evaluate what the build steps are, what the purpose of each step is, and also what services or tooling that is in use by API producers. Then I will enhance my OpenAPI research, and produce a template that can help guide my work, but also others when it comes to using GitHub for managing not just OpenAPI, but any artifact. I have linting rules for my GitHub Action files, which I use to ensure I am not forgetting anything in the pipelines for my APIs.

I am a big proponent of having first-class private, partner, or public API portals for your APIs. It is a baseline for producing APIs these days. However, I think these portals tend to be focused on consumption, and there is a lot more going on from the producer-side in these GitHub repositories. I see portals being about distribution, and repositories being about operations. Meaning, you should have a single source of truth for the operations of your API, and then you can distribute your API to whatever portal is necessary, for your consumers to onboard and put to work--with only API producers and your most trusted API consumers engaging around the API repository.

The GitHub repositories I am evaluating are primarily focused on managing OpenAPI definitions--I am going wider than that. I am using APIs.json as the core artifact in my design, with OpenAPI being just one of potentially many artifacts that you may or may not have in your repository, and indexed via your APIs.json. I see APIs.json as the manifest for what is happening, and I am looking to develop a GitHub Action pipeline that reflects this. I envision a world where every API contract is managed via a GitHub repository, involving business and engineering producer stakeholders, but also throwing your most trusted API consumers into the mix. I feel like this approach is much more scrappier, and has potential higher velocity than just a portal strategy alone.