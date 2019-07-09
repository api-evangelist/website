---
published: true
layout: post
title: Teaching My Client Three Approaches To Modular UI Design Using Their APIs
date: 2017-10-05T13:00:00.000Z
tags:
  - API Evangelist
  - HSDA
  - User Interface
  - Static
  - Clients
image: >-
  ttps://s3.amazonaws.com/kinlane-productions/holmes-county/holmes-county-listing.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/holmes-county/holmes-county-listing.png" align="right" width="40%" style="padding: 15px;" /></p>I am working with a client to develop a simple user interface on top of a Human Services Data API (HSDA) I launched for them. They want a basic website for searching, browsing, and navigating the organizations, locations, and services available in their API. A part of this work is helping them understand how modular and configurable their web site is, with each page, or portion of a page being a simple API call. It is taking a while for them to fully understand what they have, and the potential of evolving a web application in this way, but I feel like they are beginning to understand, and are taking the reigns a little more when it comes to dictate what they want within this new world.

When I first published a basic listing of human services they were disappointed. They had envisioned a map of the listings, allowing users to navigate in a more visual way. I got to work helping them see the basic API call(s) behind the listing, and how we could use the JSON response in any way we wanted. I am looking to provide three main ways in which I can put the API data to work in a variety of web applications:

- **Server-Side** - A pretty standard PHP call to the API, taking the results and rendering to the page using HTML.
- **Client-Side** - Leveraging JavaScript in the browser to call the API and then render to the page using Jquery.
- **Static Push** - Calling the APPI using PHP, then publishing as YAML or JSON to a Jekyll site and rendering with Liquid and HTML.

What the resulting HTML, CSS, and JavaScript looks like in all these scenarios is up to the individual who is in charge of dictating the user experience. In this case, it is my client. They just aren't used to having this much control over dictating the overal user experience. Which path they choose depends on a few things like whether they want the content to be easily indexed by search engines, or if they want things to be more JavaScript enabled magic (ie. maps, transitions, flows). All the API does is gives them full access to the entire surface area of the human services schema they have stored in their database.

After moving past the public website, I'm beginning to show them the power of not just GETs via their API, I'm showing them the power of POST, PUT, and DELETE. I find it is easy to show them the potential in an administrative system using a basic form. I find people get forms. Once you show them that in order to POST they have to have a special token or key, otherwise the API will reject, they feel a whole lot better about the process. I find the form tends to put things into context for them, beyond displaying data and content, and allowing them to actually manage all this data and content. I find the modularity of an API really lends itself to giving business users more control over the user interface. They may not be able to do everything themselves, but they tend to be more invested in the process, and enjoy more ownership over the process--which is a good thing.
