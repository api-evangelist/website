---
published: true
layout: post
title: 'GraphQL, Just Get Out Of My Way And Give Me What I Want'
date: 2018-05-07T09:00:00.000Z
tags:
  - API Evangelist
  - GraphQL
  - Design
image: >-
  http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/16_38_600_500_0_max_1_0_-2.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>One of the arguments I hear for why API providers should be employing GraphQL is that they should just get out of developers way, and let them build their own queries so that they can just get exactly the data that they want. As an application developer we know what we want from your API, do not have us make many different calls, to multiple endpoints--just give us one API and let us ask for exactly what we need. It is an eloquent, logical argument when you operate and live within a "known bubble", and you know exactly what you want. Now, ask yourself, will every API consumer know what they want? Maybe in some scenarios, every API consumer will know what they want, but in most situations, developers will not have a clue what they want, need, or what an API does.

This is where the GraphQL as a replacement for REST argument begins breaking down. In a narrowly defined bubble, where every developers knows the schema, knows GraphQL, and knows they want--GraphQL can make a lot of sense. In the autodidact alpha developer startup world this argument makes a lot of sense, and gets a lot of traction. However, not everyone lives in this world, and in this real world, API design can become very important. Helping people understand what is possible, learn the schema behind an API, and become more familiar with an API, until they have a better understanding of what they might want. I'm not saying GraphQL doesn't have a place when you have a significant portion of your audience knowing what they want, I'm just saying that you shouldn't leave everyone else behind.

To further turn this argument on its head, as a developer, if I know what I want, why make me build a query at all? Just give me a single URL with what I want! Don't make me do the heavy lifting, and work to craft a query, just give me a single URL with minimal authentication, and let me get what I need in one click. Sure, it will take some time before you can craft enough URLs to meet everyone's needs, but it will be worth it for those who you can. You can always craft new paths based upon requests, and yes, you can also augment your web APIs with a GraphQL endpoint for those neediest, most demanding developers who love building queries, and know exactly what they want. I guess my point is that there are a lot of definitions of knowing what you want, and how APIs can satisfy that, and not everyone will be in the same mindset as you are.

Now I have to bury in this last paragraph the fact that I'm not anti-GraphQL. I am anti-GraphQL being sold as a replacement for simpler, resource centered web APIs (aka REST). So if you are going to come at me with the Y U HATE GraphQL response--don't. I'm just trying to show GraphQL believers that they are leaving some people behind with a GraphQL only approach, unless you are 100% sure that ALL your API consumers know GraphQL, know your schema, and now what they want. GraphQL is an important tool in the API toolbox, but it isn't the one size fits all tool it is often sold as. After much contemplation, and working on the ground within enterprise groups, I am trying to put GraphQL to work in more use cases where it makes sense, and before I can do this I have to push back much of the misinformation that has been peddled about it, and undo the damage I'me seeing on the ground.
