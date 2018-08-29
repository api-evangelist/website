---
published: true
layout: post
title: Reviewing The Department Of Veterans Affairs New Developer Portal
date: 2018-08-28T09:00:00.000Z
tags:
  - API Evangelist
  - Federal Government
  - Veterans
  - Portal
  - Review
image: >-
  https://s3.amazonaws.com/kinlane-productions/federal-government/va/va-developer-portal.png
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I wanted to take a moment and review t[he Department Of Veterans Affairs (VA) new developer portal](https://developer.va.gov/). Spending some time considering at how far they've come, what they published so far, and brainstorm on what the future might hold. Let me open by saying that I am working directly and indirectly with the VA on a variety of paid projects, but I'm not being paid to write about their API effort--that is something I've done since I worked there in 2013. I will craft a disclosure to this effect that I put at the bottom of each story I write about the VA, but I wanted to put out there in general, as I work through my thoughts on what is happening over at the VA.

**The VA Has Come A Long Way**<br />
I wanted to open up this review with a nod towards how far the VA has come. There have been other publicly available APIs at the VA, as well as a variety of open data efforts, but the VA is clearly going all in on APIs with this wave. The temperature at VA in 2013 when it came to APIs was lukewarm at best. With the activity I'm seeing at the moment, I can tell that the temperature of the water has gone way up. Sure, the agency still has a long way to go, but from what I can tell, the leadership is committed to the agencies API journey--something I have not seen before.

**Developer.VA.Gov Sends The Right Signal**<br />
It may not seem like much, but providing a public API portal at developer.va.gov sends a strong signal that the VA is seriously investing in their API effort. I see a lot of API programs, and companies who have a dedicated domain, or subdomain for their API operations are always more committed than people who make it just a subsection of their existing website, or existing as a help entry in a knowledge-base. It is important for federal agencies to have their own developer.[domain].gov portal that is actively maintained--which will be the next test for the VA's resolve, keeping the portal active and growing.

**The General Look And Feel Of The Portal**<br />
I like the minimalist look of the VA developer portal. It is simple. Easy on the eyes. I feel like the "site is currently under development" is unnecessary, because this should never cease to be. I like the "an official website of the United States government", it is clean, and official looking. I'm happy to see the "Get help from Veterans Crisis Line", and is something that should be on any page with services, data, or content for veterans. I like the flexible messaging area (FMA), where it says "Put VA Data to Work". I'd like to see this section become an evolving FMA, with a wealth of messages rolling through it, educating the ecosystem about what is happening across the VA developer platform at any given moment.

**Getting Started And Learning More**<br />
The learn more about VA APIs off the FMA area on home page drops me into benefits API overview, which happens to be the first category of APIs on the documentation page. I recommend isolating this to its own "getting started" page, which provides an overview of how to get started across all APIs. Providing background on the VA developer program, as well as the other building blocks of getting started with APIs, like requesting access, studying the API documentation, and the path to production for any application you are developing. The getting started for the VA developer portal should be a first class citizen, with its own page, and a logical presentation of exactly the building blocks developers will need to get started--then they can move onto documentation across all the API categories.

**There Are Valuable APIs Available**<br />
Once you do actually begin looking at the API documentation available within the VA developer portal, you realize that there are truly valuable APIs available in there. Don't get me wrong, the [Arlington National Cemetery API](https://www.arlingtoncemetery.mil/Developers) is important, which has been the only publicly available API from the VA for several years, but when I think about VA APIs, I'm looking for resources that make a meaningful and significant impact on a vets life today:

- [**Benefits Intake**](https://developer.va.gov/explore/benefits/docs/benefits) - Veterans Benefits Administration (VBA) document uploads.
- [**Appeals Status**](https://developer.va.gov/explore/benefits/docs/appeals) - Enables approved organizations to submit benefits-related PDFs and access information on a Veteran’s behalf.
- [**Facilities API**](https://developer.va.gov/explore/facilities/docs/facilities) - Use the VA Facility API to find relevant information about a specific VA facility. For each VA facility, you'll find contact information, location, hours of operation and available services.
- [**Veterans Health API**](https://developer.va.gov/explore/health/docs/argonaut) - [There is no concise description for this API, and what is there needs some serious taming, and pulling out as part of the portal.]
- [**Veteran Verification**](https://developer.va.gov/explore/verification) - We are working to give Veterans control of their information – their service history, Veteran status, discharge information, and more – and letting them control who sees it.

One minor thing, but will significantly contribute to the storytelling around VA APIs, is the consistent naming of APIs. Notice that only two of them have API in the title. I'm really not advocating for API to be in the title or not in the title. I am really advocating for consistency in naming, so that storytelling around them flows better. I lean towards using API in each title, just so that their titles in the documentation, OpenAPI contract behind, and everywhere these APIs travel are consistent, meaningful, and explain what is available.

I like the organizing of APIs into the three categories of benefits, facilities, and health. I'd say veteran verification is a little out of place. Maybe have a veteran category, and it is the first entry? IDK. I'm thinking there needs to be a little planning for the future, and what constitutes a category, and some guidance on how things are defined, broken down, and categories, so that there is some thought put into it the API catalog as it grows. A little separation of concerns in categorization, that can maybe begin to contribute the overall microservices strategy across the VA.

**The Path To Production For Alpha API Clients**<br />
I like the path to production information for alpha API clients, I felt like it should be its own dedicated page, as one building blocks of the getting started section. However, once I started scrutinizing, it seemed like it was a separate process potentially for each individual API or category of APIs. If it can be a standalone item, I'd make it one, and link to it from each individual API category, or individual API. It it can't be, I'd figure out to make it an expandable section, or subsection of the docs. It isn't something I want to have to scroll through when working with an API and its documentation. Sure, I want to be aware of it, and be able to understand it as part of on-boarding, and revisiting it at a later date, but I don't need it to be part of the core documentation page--I just want to get at the interactive API documentation.

**Self-Service Signup**<br />
The process for signing up seems smooth. I haven't been approved for access, and the review process makes a lot of sense. I'll invest time in a separate story taking a look at the signup and on-boarding process, as well as the path to production flow for API clients, but I wanted to lightly reference as part of the review. I'd say the one confusing piece was leaving the website for the signup form, and then being dropped back at https://www.oit.va.gov/developer/, without much of any information about what was happening. It was a little jarring, and the overall flow, and process needs some smoothing out. I get that we are just getting started here, so I'm too worried about this--I just wanted to make a note of it.

**The Essentials Are There**<br />
Overall, the essentials are present at the VA developer area. It is a great start, and has the making of a good developer API portal. It just isn't very mature, and you can tell things are just getting started. You can signup, get at API documentation, and understand what it takes to build an application on top of VA API resources. Adding to, refining, and further polishing what is there will take time, so I do not want to be too critical of what the VA has published--it is a much better start than I've seen out of other federal agencies.

There are some other random items I'd like to reference, as well as brainstorm a little on what I'd like see invested in next, helping ensure the VA API portal provides what it needed for developers to be successful:

- **Terms of Service** - It is good to see the basics of the TOS, and privacy policy there. I'd like to see more about privacy, security, and service level agreements (SLA).
- **Use Of GitHub Issues** - I like the submission GitHub issues to request production access, and think it is a healthy use of GitHub issues forms, and is something the brings observability to the on-boarding process across the community.
- **Email Support** - Beyond using GitHub issues for support and on-boarding, I see alex.yale-Loehr@va.gov a lot across the site. I get why you want to be at the center of things, but email support should be made generic, and enable group ownership of the email support workflow.
- **Road Map** - I'd like to see a roadmap of what is being planned, as well as a change log for what has already been accomplished.
- **Frequently Asked Questions** - I'd like to see an FAQ page, with questions and answers broken down by category, allowing me to browse some of the common questions as I'm getting up to speed.
- **Code Samples & SDKs** - I'd like to see some more code samples in a variety of programming languages, either baked into the interactive documentation, or available on its own SDK / Code Libraries pages. I get if the VA doesn't want to get in the business of doing this, but with an OpenAPI core, there are more options available out there to generate code samples, libraries, and SDKs. I think [this vets API client](https://github.com/department-of-veterans-affairs/vets-api-clients/) effort needs to be pulled onto a code samples and SDKs page, and there be more investment in projects like this.
- **OpenAPI Download** - I'd like to see a clear icon or button for downloading the OpenAPI 3.0 contract for each of the available APIs. I want to be able to use the OpenAPI definition for more than just documentation.
- **OpenAPI 3.0** - I'm very happy to see OpenAPI 3.0 powering the API documentation, which I think is a little detail that shows the VA API team has been doing their homework.
- **Postman Collections** - I'd like to see a Run in Postman button at the top right corner of each API's documentation, allowing me to quickly load up each API into my Postman API integration and development environment.
- **Communications** - I'd like to see a blog, a Twitter account, and emphasis on the VA Github account. As an API consumer I'd like to see that someone is home besides alex.yale-Loehr@va.gov, and be able to have regular asynchronous conversations, and may engage synchronously during API office hours, or other format.

I'll stop there. I have endless more ideas of what I'd like to see in the VA developer portal, but I'm just happy to see such a clean, informative portal up and running at developer.va.gov. I'm stoked they are working on delivering real APIs that offer value to the Veteran--that is why we are doing all of this, right? I'm curious to learn about what other APIs already exist and can just be hung within this portal, as well as what APIs are planned for the immediate road map. While there are still missing parts and pieces, what they've published is a damn fine start to the VA developer program.

Next, I'm going to do a deep dive into what I'd like to see in the getting started page, as well as the path to production guidance. I'd also like to do some deep thinking on the production application (regular) check-in and review processes. I have a short list of concepts I want to flesh out, and questions I would like to answer in future posts. I just wanted to make sure I took a moment to review [the VA's hard work on their new developer portal](https://developer.va.gov/). The publishing of their developer portal marks a significant milestone in the agency's API journey, marking the spot where their API platform is beginning to shift into a higher gear.
