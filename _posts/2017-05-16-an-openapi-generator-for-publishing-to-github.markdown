---
title: An OpenAPI Generator For Publishing To Github
date: 2017-05-16 09:00:00 Z
tags:
- OpenAPI
- Generator
- Github
---

The folks behind the OpenAPI Spec driven, interactive API documentation ReDoc, have also [developed an OpenAPI generator that helps you manage your OpenAPI Spec deployment](https://github.com/Rebilly/generator-openapi-repo) using Yeoman. If you aren't familiar with Yeoman, it is modern scaffolding for web apps, which is all about helping you manage the quick and consistent deployment of APIs following existing best practices.

<p><img style="padding: 5px;" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/redoc/redoc-yeoman-generator-github.png" align="center" width="98%" /></p>

ReDoc's Yeoman generator leverages all the benefits of pushing your OpenAPI Specs and API documentation on Github:

* Community Engagement - Allows for engagement with API consumers via Github's native infrastructure, and issue management.
* Hosting on GitHub Pages - You are offloading the hosting and bandwidth to Github, and their CDN, significantly reducing overhead.
* Exposure in Github Community - Your API documentation and presence is available on Github, via trending, search, and other discovery mechanisms.
* Life Cycle Management - Github provides you with version history, branching, and continuous integration options, matching with your existing workflows.
* Familiar Environment - People increasingly understand Github as an environment where you can engage with code, as well as the community around the tooling and content published in this environment.

ReDoc's Yeoman generator helps to create a GitHub repo with the following features:

* Possibility to split a big Swagger spec into smaller files and bundle it for deployment
* Continuous integration/deployment on Travis
* Code samples as separate files
* Swagger spec is validated after each commit
* Swagger spec + ReDoc deployed to Github Pages
* Live editing in your editor or swagger-editor

<p><img style="padding: 5px;" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/redoc/yeoman-generator-wizard-image.png" align="center" width="98%" /></p>

[All the documentation for ReDoc's Yeoman generator is available on the Github repository](https://github.com/Rebilly/generator-openapi-repo). The Yeoman generator demonstrates how OpenAPI Spec operates as more than just a machine readable core to API documentation. It acts as a machine-readable core to all stops along the API life cycle defining how you design, deploy, manage, and document your APIs.

ReDoc shows us the role OpenAPI Spec can play in driving your APIs documentation, but then turns things up a notch or two, demonstrating that when you publish your OpenAPI Spec to Github and drive your documentation, it can become a Github-driven engine for any services and tooling you will need as part of API operations---from design all the way to deprecation. [ReDoc's OpenAPI Spec generator](https://github.com/Rebilly/generator-openapi-repo) will help you bootstrap the deployment your OpenAPI, which will end up being the heartbeat of your API.