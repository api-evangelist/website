---
published: true
layout: post
title: 'Postman Interceptor But for Product Managers'
image: https://kinlane-productions2.s3.amazonaws.com/postman-interceptor-add-on-screenshot.png
author:
 name: kinlane
tags:
- Products
- Product Management
- Gateway
- Observability
- Logs
- Usage
- Teams
- Consumers
---
I was talking to someone yesterday about the growing need to reverse engineer what is happening across this sprawling API landscape. While there is a lot of focus on having an API strategy, standardizing the API lifecycle, and investing in API governance, the greatest benefit Postman providers for developers is the ability to reverse engineer and make sense of the API chaos around us. You can turn on [Postman Interceptor](https://chrome.google.com/webstore/detail/postman-interceptor/aicmkgpgakddgnaphhhpliifpcfhicfo?hl=en), open up the desktop version of Postman, and you can browse and use any web application, and Interceptor will reverse engineer all of the APIs behind the application. Now, hold that picture in your head, but then think about the same functionality but for reverse engineering and surface area of things that a product manager will care about.

So what would a product manager care about? This is where I normally lean on my partner in crime [Deepa Goyal](https://www.linkedin.com/in/deepag/), but she is out of office on leave. So I am sure she’ll have a whole other list of what product managers will care about. But, let me take a crack. Here are a few things they might want to reverse engineer and surface to help them understand what is happening across the APIs they depend on.

- **Usage** - Tell me where to go to understand the usage of an API, and how many calls are being made by different consumers.
- **Logs** - Where do I find the logs for an API so that I can use to help me better understand what is actually happening with an API.
- **Observability** - How do I find where data is being piped in APM so that I can tune into dashboards and other observability metrics. 
- **Distribution** - Where an API distributed to portals, wikis, blog posts, videos, and other aspects of a modern API developer experience.
- **Engagement** - Usage API is a good start, but I also need more information on who is engaging with docs and other resources.
- **Teams** - I need to understand who is the owner of an API, revealing the team behind, understanding everyone who is involved.
- **Consumers** - Where do I go to find the consumers of an API, the companies, the human beings, and other details that will help me.
- **Feedback** - Where can I go to find the feedback loop for an API with consumers, allowing me to tap into what is being said. 

[Postman Interceptor](https://chrome.google.com/webstore/detail/postman-interceptor/aicmkgpgakddgnaphhhpliifpcfhicfo?hl=en) will reverse engineer the surface area of an API instance. What I want to reverse engineer the operational surface area of an API. I am given a new API or application to iterate and evolve, I want to be able to immediately map the operational and business landscape for an API. I want this done for all of the APIs used in an application, profiling private, partner, and public APIs. I need to know the technical details of each API, but I”ll leave that to the engineering team I’ll be leading. I am more interested in the operational and business considerations that existing teams sustaining an API are either not going to known about or care about.

This tool does not exist, but the data is out there. The integrations to API gateways usage and logs exists already. The integrations to APM solutions to make sense of observability already exist. We just need to keep connecting the dots on this using a platform mindset. I am already seeing observability evolve to meet the needs of product managers, and the API lifecycle begin shifting towards what product managers need. While I wish the ideal lifecycle and product manager environment could be setup fresh with each new API, but like the rest of the API landscape I spend my days studying, I am guessing product managers are going to have to come in and reverse engineer what is happening, and they are going to need a lot of help along the way.