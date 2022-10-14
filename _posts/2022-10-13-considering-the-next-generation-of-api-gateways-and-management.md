---
published: true
layout: post
title: 'Considering the Next Generation of API Gateways and Management'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/san-francisco-skyline-night-san-francisco-skyline-night-blue-circuit-3.jpg
author:
 name: kin
tags:
- Management
- Gateway
- Regions
- Protocols
- Federated
- Edge
- Policies
- Identity
- GitOps
---
I am trying to write nightly here on API Evangelist, capturing at least one thought from my work with APIs. One of the areas of API operations I am doing a deep dive into right now is the familiar and well-known area of API management and specifically the increasingly commoditized API gateway. API management was the original catalyst for this blog back in 2010, and a space I have followed closely over the last twelve years. While I haven’t been down in the weeds of API Management while at Postman, I have been helping shape our gateway strategy, resulting in me diving deeply into the API management realm to understand what has changed, and explore what the signals are regarding what the future holds. While evaluating different API gateways today I was connected to Josh Twist (<a href="https://twitter.com/joshtwist">@joshtwist</a>), the CEO of <a href="https://zuplo.com/">Zuplo</a> today, and had an interesting conversation with him about what is next when it comes to API Management and gateways.
 
While I still have a lot of research, discussions, and contemplating what the future holds when it comes to API Management and gateways, some of the areas I’ve been noodling about from conversation via my Breaking Changes podcast are centered around these areas:
 
- **Multi-Protocol** - Allowing us to deliver web, GraphQL, WebSockets, gRPC, and other types of APIs via the same gateway.
- **Multi-Cloud** - Abstracting away the complexities of delivering APIs across any of the cloud platforms that we will need to.
- **Federated** -  Leveraging centralized guidance, policies, and other resources, while supporting distributed teams to have autonomy.
- **Product Management** - Using the gateway layer to define, iterate, and ensure our digital resources meet the needs of consumers.
- **Edge** - Making it dead simple to deploy APIs as close to your consumers as possible, helping improve performance and quality.
- **Regional** - Shadowing edge deployments with the ability to deliver across the regions we need to meet regulatory needs.
- **Policies** - Standardizing, federating, and automating how policies are applied across gateways by any team delivering Apis.
 
These are just some of the leading areas I am seeing gateway providers work to meet the needs of API producers across many industries, but during my conversation with Zuplo, I was enlightened when it comes to a handful of other areas I feel are shaping what is happening at this layer of our API Operations:
 
- **Identity** - Simplifying identity and access management across APIs, leveraging modern approaches to this essential dimension.
- **GitOps** - Meeting developers where they are when it comes to developing APIs, building on what they know via source control and CI/CD.
- **Programmable** - Leveraging the APIs behind API gateways to ensure that our API operations are always programmable.
- **Simplicity** - Keeping things simple and doing exactly what teams need, making capabilities accessible across business and technical teams.
 
During our discussion about how Zuplo views API management around the API gateways, and similar to my discussion with CloudFlare, we talked about the growing importance of delivering APIs at the edge. But it was the GitOps and programmable belief that accompanied this that really caught my attention. When I combine multi-protocol, multi-cloud, federated gateway solutions deployed at the edge within regions you need to operate in, while being able to programmatically govern, audit, configure, scale, evolve, and shape the delivery of APIs—-I find myself getting closer to a coherent vision of what could be next for API gateways. I am still hyper focused on the gateway, and will also zoom out to more management capabilities like portals, documentation, and other solutions as part of my research in coming weeks.
 
While I have been very focused on multi-protocol and the ability to deliver HTTP, TCP, and other types of APIs, as well as RESTful, GraphQL, WebSockets, gRPC and other patterns across gateways due to my work on API specifications as part of Postman Open Technologies, I find federated, edge, GitOps, and programmable approaches to managing our API landscape via gateways very compelling and worth pondering more. I’ll be digging in more into these topics, reaching out to more people I know about their thoughts, evaluating other leading gateway solutions, and working towards a more opinionated view of what is coming when it comes to this well-established aspect of how we do APIs. Then I’ll publish some more formal work via Postman channels, taking my rough ideas here and bringing them home when it comes to a wider audience.