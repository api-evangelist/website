---
published: true
layout: post
title: >-
  Providing Minimum Viable API Documentation Blueprints To Help Guide Your API
  Developers
date: 2018-09-13T09:00:00.000Z
tags:
  - API Evangelist
  - Documentation
  - Portals
  - GitHub
  - Blueprints
  - Federal Government
  - Veterans
image: >-
  https://s3.amazonaws.com/kinlane-productions/federal-government/va/va-definitions-support.png
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I was taking a look at the Department of Veterans Affairs (VA) API documentation for the VA Facilities API, and intending on providing some feedback on the API implementation. The API itself is pretty sound, and I don't have any feedback without having actually integrated it into an application, but following on the heals of [my previous story about how we get API developers to follow minimum viable API documentation guidance](http://apievangelist.com/2018/08/27/how-do-we-get-developers-to-follow-the-minimum-viable-api-documentation-guidance/), I had lots of feedback on the overall deliver of the documentation for [the VA Facilities API](https://developer.va.gov/explore/facilities/docs/facilities), helping improve on what they have there.

**Provide A Working Example of Minimum Viable API Documentation**<br />
One of the ways that you help incentivize your API developers to deliver minimum viable API documentation across their API implementations is you do as much of the work for them as you can, and provide them with a forkable, downloadable, clonable API documentation that meets the minimum viable requirements. [To help illustrate what I'm talking about I created a base GitHub blueprint for what I'd suggest as a minimum viable API documentation at the VA](https://va-working.github.io/api-documentation/). Providing something the VA can consider, and borrow from as they are developing their own strategy for ensuring all APIs are consistently documented.

**Covering The Bare Essentials That Should Exist For All APIs**<br />
I wanted to make sure each API had the bare essentials, so I took what the VA has already done over at [developer.va.gov](https://developer.va.gov/), and republished it as a static single page application that runs 100% on GitHub pages, and hosted in a GitHub repository--providing the following essential building blocks for APIs at the VA:

- **Landing Page** - Giving any API a single landing page that contains everything you need to know about working with an API. The landing page can be hosted as its own repo, and subdomain, and the linked up with other APIs using a facade page, or it could be published with many other APIs in a single repository.
- **Interactive Documentation** - Providing interactive, OpenAPI-driven API documentation using Swagger UI. Providing a usable, and up to date version of the documentation that developers can use to understand what the API does.
- **OpenAPI Definition** - Making sure the OpenAPI behind the documentation is front and center, and easily downloaded for use in other tools and services.
- **Postman Collection** - Providing a Postman Collection for the API, and offering it as more of a transactional alternative to the OpenAPI.

That covers the bases for the documentation that EVERY API should have. Making API documentation available at a single URL to a human viewable landing page, complete with documentation. While also making sure that there are two machine readable API definitions available for an API, allowing the API documentation to be more portable, and useable in other tooling and services--letting developers use the API definitions as part of other stops along the API lifecycle.

**Bringing In Some Other Essential API Documentation Elements**<br />
Beyond the landing page, interactive documentation, OpenAPI, and Postman Collection, I wanted to suggest some other building blocks that would really make sure API developers at the VA are properly documenting, communicating, as well as supporting their APIs. To go beyond the bare bones API documentation, I wanted to suggest a handful of other elements, as well as incorporate some building blocks the VA already had on the API documentation landing page for the VA Facilities API.

- **Authentication** - Providing an overview of authenticating with the API using the header apikey.
- **Response Formats** - They already had a listing of media types available for the API.
- **Support** - Ensuring that an API has at least one support channel, if not multiple channels.
- **Road Map** - Making sure there is a road map providing insights into what is planned for an API.
- **References** - They already had a listing of references, which I expanded upon here.

I tried not to go to town adding all the building blocks I consider to be essential, and just contribute couple of other basic items. I feel support and road map are essential and cannot be ignored, and should always be part of the minimum viable API documentation requirements. My biggest frustrations with APIs are 1) Up to date documentation, 2) No support, and 3) Not knowing what the future holds. I'd say that I'm also increasingly frustrated when I can't get at the OpenAPI for an API, or at least find a Postman Collection for the API. Machine readable definitions moved into the essential category for me a couple years ago--even though I know some folks don't feel the same.

**A Self Contained API Documentation Blueprint For Reuse**<br />
To create the minimum viable API documentation blueprint demo for the VA, I took the HTML template from [developer.va.gov](https://developer.va.gov/), and deployed as a static Jekyll website that runs on GitHub Pages. The landing page for the documentation is a single index.html page in the root of the site, leverage Jekyll for the user interface, but [driving all the content on the page from the central config.yml for the API project](https://github.com/va-working/api-documentation/blob/master/_config.yml). Providing a YAML checklist that API developers can follow when publishing their own documentation, helping do a lot of the heavy lifting for developers. All they have to do is update the OpenAPI for the API and add their own data and content to the config.yml to update the landing page for the API. Providing a self-contained set of API documentation that developers can fork, download, and reuse as part of their work, delivering consistent API documentation across teams.

The demo API documentation blueprint could use some more polishing and comments. I will keep adding to it, and evolving it as I have time. I just wanted to share more of my thoughts about the approach the VA could take to provide function API documentation guidance, as a functional demo. Providing them with something they could fork, evolve, and polish on their own, turning it into a more solid, viable solution for documentation at the federal agency. Helping evolve how they deliver API documentation across the agency, and ensuring that they can properly scale the delivery of APIs across teams and vendors. While also helping maximize how they leverage GitHub as part of their API lifecycle, setting the base for API documentation in a way that ensures it can also be used as part of a build pipeline to deploy APIs, as well as manage, testing, secure, and helping deliver along almost every stop along a modern API lifecycle.

The website for this project is available at: https://va-working.github.io/api-documentation/
You can access the GitHub repository at: https://github.com/va-working/api-documentation
