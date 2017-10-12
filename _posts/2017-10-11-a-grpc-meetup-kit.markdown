---
published: true
layout: post
title: The gRPC Meetup Kit
date: 2017-10-11T12:00:00.000Z
tags:
  - API Evangelist
  - API Events
  - Meetups
  - Workshops
  - Evangelism
image: 'https://s3.amazonaws.com/kinlane-productions/grpc/grpc-logo.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/grpc/grpc-logo.png" align="right" width="40%" style="padding: 15px;" /></p>[I wrote about Tyk's API surgery meetups last week](http://apievangelist.com/2017/09/29/tyk-is-conducting-api-surgery-meetups/), and adding a new approach to our API event and workshop toolbox, and next I wanted to highlight [the gRPC Meetup Kit](https://github.com/grpc-ecosystem/meetup-kit), a resource for creating your own gRPC event. gRPC is an approach out of Google for designing, delivering, and operating high performance APIs. If you look at the latest wave of APIs out of Google you'll see they are all REST and/or gRPC. Most of them are dual speed, providing both REST and gRPC. gRPC is an open source initiative, but very much a Google led effort that we've seen picking up momentum in 2017.

While I am keeping an eye on gRPC itself, this particular story is about the concept of providing a Meetup kit for your API related service or tooling, providing an "In a Box" solution that anyone can use to hold a Meetup. The gRPC team provides three groups of resources:

### gRPC 101 Presentation
- [Talk](https://www.youtube.com/watch?v=UVsIfSfS6I4) - A 15 minute course introduction video.
- [Slides](https://docs.google.com/presentation/d/1dgI09a-_4dwBMLyqfwchvS6iXtbcISQPLAXL6gSYOcc/edit?usp=sharing) - Slides that go along with the talk.
- [Codelab](https://codelabs.developers.google.com/codelabs/cloud-grpc/index.html) - A 45m codelab that attendees can complete using [Cloud Shell](https://cloud.google.com/shell/).

## Resources and community
- [**gRPC Website**](http://www.grpc.io/)
- **Codelab**
	- [Building a gRPC service with Node.js](https://codelabs.developers.google.com/codelabs/cloud-grpc/index.html)
    - [Building a gRPC service with C#](https://codelabs.developers.google.com/codelabs/cloud-grpc-csharp/index.html)
- [**GitHub Source**](https://github.com/grpc)
	- [Extended gRPC Ecosystem](https://github.com/grpc-ecosystem)
    - [Blog](http://www.grpc.io/blog/)
    - [Youtube Channel](https://www.youtube.com/channel/UCrnk1HWelWnYtF78YZX80fg)    
- **Ask Questions**
	- [Gitter Chat](https://gitter.im/grpc/grpc)
    - [Google Group](https://groups.google.com/forum/#!forum/grpc-io)
    - [Stack Overflow](http://stackoverflow.com/tags/grpc/)
- **Keep in Touch**
	- [Twitter](https://twitter.com/grpcio)

## Request Support for Your Event
- [gRPC Stickers](https://goo.gl/forms/C3TCtFdobz4ippty2)
- [Sign up for office hours with gRPC team](https://goo.gl/forms/pvxNwWExr5ApbNst2)

It provides a nice blueprint for what is needed when crafting your own Meetup Kit as well as some material you could weave into any other type of Meetup, or workshop that might contain gRPC. Maybe an API design and protocol workshop, where you cover all of the existing approaches out there today like REST, Hypermedia, gRPC, GraphQL, and others. If nothing else the gRPC Meetup Kit provides a nice forkable project, that you could use as scaffolding for your own kit.

As I mentioned in my piece about Tyk, I don't think Meetups are going anywhere as a tool for API providers, and API service providers to reach a developer audience. However, I think we are going to have to get more creative about how we organize, produce, and incentivize others to put them on. They are a great vehicle for brining together folks in a community to learn about technology, but we have to make sure they are delivering value for people who show up. I am guessing that a little planning, and evolving a toolkit using Github is a good way to approach putting on Meetups, workshops, and other small events around your products, services, and tooling.
