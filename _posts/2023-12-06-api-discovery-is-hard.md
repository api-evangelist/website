---
published: true
layout: post
title: 'API Discovery is Hard'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/america-immigration_dumping-ground-statue-facing-scrunched.jpg
author:
    name: kinlane
tags:
- API
- Search
- Ratings
- Scores
- Discovery
- Landscape
- Mapping
- Momentum
- Change
---
Providing useful API discovery solutions is hard. I have dedicated 15 years to understanding and trying to provide solutions to this problem. I regularly <a href="https://apievangelist.com/2021/02/11/gathering-my-thoughts-on-api-discovery/">gather my thoughts</a> on this subject and invest cycles in moving forward the solutions I feel are needed to help with API discovery. My solutions all revolve around my API discovery format—-[APIs.json](https://apisjson.org). As I move from the realm of API service provider to API platform governance, alongside some fresh pain around API discovery I have found new energy to invest in APIs.json, and the wider API operational discovery landscape. 

## Dimensions of API Discovery
API discovery is hard because there are so many dimensions to what APIs are, but also how and why you are searching for me. Some of the common questions I ask when it comes to separating out the API discovery are:

- **Who is searching?** An API producer or consumer, or possibly designer, architect, analyst, or possibly a product manager.
- **Where are they searching?** Are APIs being searched for internally within the enterprise, within specific groups, or is it external.
- **Why are they searching for APIs?** Why someone needs an API will vary widely based upon their role within the enterprise.
- **Is human searching, or is it a computer searching?** With a sprawling API landscape it is often another system doing the searching.
- **What is the popularity, quality, reliability of the API?** Are the APIs I find in my search the ones that I can depend on to use.

These questions get at what part of the API landscape someone is interested in, why they are searching for an API, as well as speak to why API discovery is such a difficult problem to solve. What Google did for HTML, PDF, and other types of documents making up the web doesn’t quite apply the same to the sprawling API landscape. I consider APIs to be the next iteration of the web, and when I talk about API discovery, I am talking about the surface area of the API landscape, not the content of the API landscape--which is very different from web search.

## Mapping the API Landscape
One of the main reasons API discovery is so hard is because the landscape needing discovery is so vast and ever changing, and is oftentimes a moving target that is on fire. To effectively discover something you need to be able to map it out, with a few areas I have covered in my API landscape mapping toolbox.

- **Specifications** - OpenAPI, AsyncAPI, and JSON Schema will continue to play a central role in the API discovery combination.
- **Vocabulary** - Having a formal vocabulary for discovering new APIs in an automated way, while also using it to markup meta data for APIs is important.
- **Domains** - Bounded contexts are critical for not just designing APIs, but also organizing and making them available as part of API discovery.
- **Semantics** - APIs need to be augmented with rich semantics that help us understand the resources and capabilities being made available to users.
- **Relationships** - Have a way of defining what the relationships are between your API resources and capabilities across internal and external domains.

We have only begun to understand how we can map the API landscape in motion. Linked data, semantic, and domain-driven design folks have been sounding this alarm for years, but if we are going to make any movement here, we are going to have to come up with ways to effectively map the landscape without any additional work while in motion.

## Access to the API Landscape
The divide between what is private, what is available to different lines of business and teams, as well as available to select partners, and the APIs that are open to the public is one of the most deciding reasons why we don’t have any comprehensive API discovery solutions—these dimensions make people nervous.

- **Public** - Despite concerns public APIs will continue to dominate and drive the API discovery conversation because it is the easiest to reference.
- **Private** - Private API discovery is where we are seeing the most growth and demand for API discovery solutions in the last five years.
- **Authentication** - Being able to apply or at least consider authentication at the API discovery layer will help reduce friction at the discovery layer.
- **Authorization** - Who you are and what credentials possess, and the policies applied to those credentials will keep driving the API discovery conversation.
- **Control** - Being able to edit API definitions, metadata, and other elements used in discovery seems to be a significant part of how we discover and work with APIs.

In my opinion, the bulk of APIs should be publicly available with identity and access management keeping us all safe and secure. API designs and even implementations should be in the public commons and easily mapped and discovered across, keeping access being defined by common IAM solutions.

## Mapping the State of the Landscape
The number one reason I see enterprises invest in API discovery is when it is in service of security, observability, and common trends to help us get a  handle on the API sprawl at scale. These areas often prompt business and technical leadership to invest more in API discovery, but it really should be wider than any single dimension of our API operations, otherwise it will continue to fall short.

- **Monitoring** - Including monitoring data for all APIs as part of API discovery plays a big role in understanding the uptime and availability of resources.
- **Testing** - Augmenting monitoring data, a range of testing data needs to be included as part of the search and discovery of each and every API.
- **Reliability** - You want to find the APIs that are reliable when searching for 3rd party or public APIs, and find those that aren’t reliable internally.
- **Quality** - The overall quality of each API across many dimensions has to be included in the overall API discovery index that powers what we discover.
- **Traceability** - We are in desperate need of the ability to trace out what is going on with the big ball of API yarn we’ve spread across our organizations.
- **Vulnerabilities** - Finding the vulnerabilities across our infrastructure before bad people do is a top priority for the API discovery conversation.
- **Security** - You can’t secure what you don’t know about, so security will continue to be one of the most important reasons why we do API discovery.

This is the hardest one to do, and there are API service providers who do this well. These providers should join forces to produce this data, but ultimately the access and control that exists across the API landscape, even when public, will always make this view of the landscape difficult. I will keep an eye on ways I can invest at this layer, but honestly, much of it is not my wheel house, and I'll need help from others.

## Mapping the Momentum of Landscape
Another aspect of the landscape that has to be factored in is the momentum that exists as things are changing, and how much we have the ability to keep up with and engage within that change using continuous integration and deployment techniques, and automate how we map and understand the API landscape.

- **Change** - Managing change across the enterprise is the biggest challenge teams face, and API discovery needs to consider how things change or not.
- **Forkability** - The ability to fork the APIs we are discovering, and sort and rank based upon what we’ve forked and merged will continue to drive search.
- **Automated** - API discovery in all forms has to be automated. It is clear that we can’t count on humans to catalog and make APIs available for discovery.

Change across the landscape makes discovery extremely difficult. Do you have the latest version? Is your work automated? Momentum works against and with us in the right situations. Mapping the landscape with change in mind is important to be able to find what you need to keep moving forward.

## Governing the Landscape
Aside from security, regulation is the primary drive of API discovery, otherwise enterprises are generally pretty happy operating in the API chaos that exists today. Most business and technical leadership couldn’t care less about finding their APIs, unless there is someone in government telling them they need to find APIs, or at least the data they serve up.

- **Policies** - Defining what operating policies are already in place, while effectively applying, evolving, and deprecating policies when the time is right.
- **Regulation** - When it comes to GDPR and other regulations emerging, we are increasingly going to be able to discover exactly the resources we need.
- **Compliance** - Being compliant when it comes to our API operations is a central concern for those in charge, especially as things keep expanding.
- **Rating** - Augmenting policies with points which accumulate on any API they are applied to, providing a weight that can be used to enhance API search.

This is the area where I work, and one of the important areas I think for moving the API discovery conversation forward. In order for us not to get lost and drown in the sprawling landscape of APIs that exist inside and outside of the enterprise, we are going to need more policies, regulations, and compliance in place to govern what is happening.

## Searching the Landscape
Now we actually get to where we are actually discovering APIs. A whole lot has to be in place for this layer to be possible. Search and discovery of APIs across the increasingly sprawling landscape requires investment in mapping the landscape, having proper identity and access management in place, as well as being able to understand the state and momentum of the landscape, and being able to govern how things work. Once you have this in motion, you will need a little bit more to find what you need.

- **Context** - The narrative for each API and its consumers and applications play a big role - in helping us discover what is going on around each API.
- **Rating** - We are going to need a multi-part sophisticated approach to rating APIs so that we can focus on just what matters to use when it comes to discovery.
- **Search** - Having a search box handy is central to API discovery, whether that is in application, via local network, or on the open web using a search engine.
- **SEO** - The search engine optimization game will continue to drive the API discovery conversation, and keep shaping how we describe the APIs we have.
- **Ease** - API discovery has to be easy no matter who you are, and something that has to consider personas, context, and much more under the hood.

I feel like a lack of investment in all the areas above contributes to people not being able to find what they need, rendering it very difficult to provide any single solution to API discovery. There are a lot of API discovery solutions littering the side of the road we used to get here. I feel like there are a number of things on this list that are introducing friction, with other things helping incentivize forward motion in the API discovery conversation—the question is, how do we do all of this in motion without adding more work.

## Multidimensional API Search
We launched the alpha version of the [APIs.io search engine](https://apis.io) where we indexed 215 individual APIs across 72 top API producers. This is the landscape we have mapped so far, and we have developed a set of policies and ratings to help govern this landscape. Then we stood up a simple search engine on top of the landscape. Next we’ll keep expanding the landscape map and strengthening the governance, but then think about how we can use search to better understand who is searching, why they are searching, and what they are searching for. One could imagine a quick way to set the context of your search to accommodate who, what, and why before you perform the search—-resulting in very different outcomes.

This post is a continuation of my APIs.json and APIs.io open source work, but it is also the next step after <a href="https://apievangelist.com/2021/02/11/gathering-my-thoughts-on-api-discovery/">I gathered my thoughts on API discovery in 2021</a>. The access, state, and momentum of the API landscape are much harder problems I want to identify and leave on the back burner. However, I think we can really move the conversation forward when it comes to mapping, governing, and searching the landscape across multiple dimensions of who, what, why, and how. Now that I have a map with governance in place, and my search, I can work on a blueprint for search that helps us develop the easiest to use search for API developers, consumers, producers, and product managers across industries, and any other facet that is relevant. First I think I will need to organize the API properties I’ve been indexing by role and other dimensions that will lend itself to better discovery. 