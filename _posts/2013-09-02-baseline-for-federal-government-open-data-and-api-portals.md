---
layout: post
title: "Baseline for Federal Government Open Data and API Portals"
url: 'http://apievangelist.com/2013/09/02/baseline-for-federal-government-open-data-and-api-portals/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/bw-portal.jpg'
---

[<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-portal.jpg" alt="" width="200" align="right" />][1]

I have a whole list of projects around open data and APIs at the Department of Veterans Affairs (VA). Additionally I have numerous other open data and API projects I'd like to tackle across other federal agencies. As I do with other areas of my work, I needed a standardized way to stabilize the datasets and APis I will need for my projects, in the same way any open data and API provider should do for their consumers.

To help support my work, and hopefully the work of others I wanted to create a baseline portal that I could use at the VA, for showing what is possible when hanging open datasets and APIs, in a full featured portal. The success of any open data and / or API portal starts with the technical building blocks, like data and APIs, but have a set of business and political building blocks that are essential to their adoption and growth.

I've spent the last three years studying the business and politics of APIs. During these three years I've looked at almost 10,000 API developer portals, and I've established a [base set of what I consider the building blocks][2] of successful API portals, with a handful in which I consider essential to success. I've always wanted a simple API portal template that would reflect this research, and my new [Developer @ VA][1] portal is the first step towards achieving this.

[Developer @ VA][1] is an early stage prototype, whcih I've built to satisfy this need of mine, specifically for my VA projects. I will be polishing this portal and replicating it as a single template that can be used for any API and / or open data portal. This portal exists purely as a [Github repository][3] and runs on [Github Pages][4], using a [Jekyll for managing its pages and blog][5]. Everything else is HTML, CSS, Javascript and JSON, allowing it to be able to run on any server, including other cloud services like Dropbox or Amazon S3.

To start with I've included 20 of what I consider essential API building blocks:

  * Landing Page
  * Getting Started
  * APIs
  * Data
  * Interactive Docs
  * Code
  * Gallery
  * Support
    * Self-Service
      * Stack Exchange
      * Quora
    * Direct Support
      * Issue Management
      * Twitter
      * LinkedIn
      * Facebook
      * Google
  * Roadmap
  * Changelog
  * Blog
  * Terms of Use
  * Privacy Policy
  * Branding Guidelines

Beyond this project running using open formats and standards, and being deployable in common cloud environments like Github, Dropbox and Amazon S3, everything is machine readable by default. The portal starts with a [sitemap.json][6], which links  to other building blocks that make up the open data and API portal, including a data.json and api.json which provide programmatic access to all resources included in the site:

  * [data.json][7] \- Machine readable JSON file of all data assets using common core metadata for easy access to all data stored in the portal
  * [api.json][8] \- Machine readable JSON, using the Swagger format describing all API resources available within the portal

Next I wanted all essential building blocks of the portal to also be machine readable by default:

  * [Code][9] \- JSON library of all code available for use when integrating with datasets and APIs
  * [Gallery][10] \- A JSON gallery of web, mobile apps and visualizations, widgets, excel and other integrations on data and APis
  * [Support][11] - A JSON listing of self-service and direct support channels for the portal
  * [Roadmap][12] \- JSON listings of both the future with a roadmap, providing transparency into portal operations
  * [Changelog][13] \- A JSON listing documenting the past with all changes made to the portal
  * [Legal][14] \- A directory of the legal building blocks of the portal with links to terms of use, privacy and branding guidelines

This project is the product of 3 years of research, and 3 days worth of work. So it is rough. I was able to capture my initial vision in 3 days, but still a lot of work to do. I need to let it simmer a little bit, and round off some of the rough edges and apply some polish. Then the next step is to generate a generic template from it, that will become the baseline for any other portal I derive from this work.

If there is anything you'd like to see in the future, go ahead and use any of the [support channels available][15] on the site. Once I get the base template set up, I will use that as a top level project to guide the future of this baseline for open data and API portals.

   [1]: http://kinlane.github.io/va-developer/
   [2]: http://management.apievangelist.com/building-blocks.html
   [3]: https://github.com/
   [4]: http://pages.github.com/
   [5]: http://jekyllrb.com/
   [6]: http://kinlane.github.io/va-developer/sitemap.json
   [7]: http://kinlane.github.io/va-developer/api.json
   [8]: http://kinlane.github.io/va-developer/data.json
   [9]: http://kinlane.github.io/va-developer/code/code.json
   [10]: http://kinlane.github.io/va-developer/gallery/gallery.json
   [11]: http://kinlane.github.io/va-developer/support/support.json
   [12]: http://kinlane.github.io/va-developer/roadmap/roadmap.json
   [13]: http://kinlane.github.io/va-developer/roadmap/changelog.json
   [14]: http://kinlane.github.io/va-developer/legal/legal.json
   [15]: http://kinlane.github.io/va-developer/support/
