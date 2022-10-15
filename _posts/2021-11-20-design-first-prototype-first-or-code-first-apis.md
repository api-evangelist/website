---
published: true
layout: post
title: 'Design-First, Prototype-First, or Code-First APIs'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/docks-docks-light-dali.jpg
tags:
- Design
- Prototype
- Code
- API-First
---
I strongly believe in a design-first approach to delivering new APIs, and future iterations of existing APIs. Having an OpenAPI artifact to guide discussions, services, and tooling saves you time, money, and frustration across the API lifecycle. This isn’t opinion, this is fact. However, I also have grown to be very pragmatic in how I approach the API lifecycle, and fully grasp that adopting API-first effectively across teams isn’t something that all enterprise organizations will have the time, skills, and other resources to make happen. Resulting in me supporting design-first, prototype-first, and code-first approaches to delivering APIs.

I will keep investing in stories and demonstrations of what, why, and how API design-first makes sense because these three realities I see across the landscape keep me from getting too dogmatic on this subject.

- **Design-First** - Using an OpenAPI to document, mock, test, and iterate upon a new or existing API make sense if you have the time and skills, but when you don’t it is something that can become half-baked and causing problems throughout the API lifecycle, so make sure you are properly investing in API-first, and not just jumping on the bandwagon.
- **Prototype-First** - This one actually surprised me, but when I saw folks prototyping APIs using a Postman collection, which provides the ability to mock and document your API without an OpenAPI, but then generate an OpenAPI once you get to an agreed upon state, I began making sure prototype is part of the equation when it comes to delivering APIs.
- **Code-First** - Coding is what most developers get, and there are plenty of ways to use annotations and proxies to still ensure there is an OpenAPI for code-first projects. Using code-first approaches to rapidly prototyping while still adopting many of the iterative approaches to moving an API forward can be just as effective as many design-first approaches.

It would be nice if everyone could just stop what they are doing and learn OpenAPI as well as a design-first approach to delivering APIs. This is definitely what we should strive for, however it just isn’t always the reality on the ground within the enterprise in this moment. We can still do code-first, while also generating an OpenAPI, and stabilizing the documentation, testing, security, and feedback loop around our APIs. All while still making sure folks are exposed to design-first practices, so that at some point, when it makes sense, they can began shifting towards a design-first mindset. My goal in all of this is to make sure folks are moving towards a healthier and well-known API lifecycle, not just going design-first, and over the years I have learned that some times the resistance you get when you tell folks they are doing something wrong just isn’t worth the fight--we are better off meeting them where they are at.