---
published: true
layout: post
title: Rules for Extending Your API With Each Version
date: 2018-03-14T09:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Versioning
image: >-
  http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/23_19_800_500_0_max_0_-5_-1.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I'm spending time learning from the API design guides of other leading API providers, absorbing their healthy practices, and assimilating them into my own consulting and storytelling. One API design guide I am learning a lot from is out of [the Adidas Group](https://adidas-group.gitbooks.io/api-guidelines/), which contains a wealth of wisdom regarding not just the design of your API, but also the deployment and evolution of the API resources we are publishing.

[One particularly interesting piece of advice I found within Adidas API design guidance were their rules for extending an API](https://adidas-group.gitbooks.io/api-guidelines/content/core-principles/rules-for-extending.html), which I think is pretty healthy advice for an API developer to think about.

_Any modification to an existing API MUST avoid breaking changes and MUST maintain backward compatibility._

_In particular, any change to an API MUST follow the following Rules for Extending:_

 - _You MUST NOT take anything away (related: Minimal Surface Principle , Robustness Principle)_
 - _You MUST NOT change processing rules_
 - _You MUST NOT make optional things required_
 - _Anything you add MUST be optional (related [Robustness Principle](https://en.wikipedia.org/wiki/Robustness_principle))_

_NOTE: These rules cover also renaming and change to identifiers (URIs). Names and identifiers should be stable over the time including their semantics._

First of all, I think many API developers aren't even thinking about what constitutes a breaking change most of the time. So having any guidance that makes them pause and think about this topic is a good thing. Second, I think we should be sharing more stories about when things break, helping folks think more about these elements--the problem is that many folks are embarrassed they introduced a breaking changes, and would rather not talk about it, let alone make it publicly known.

I am working my way through [the API Stylebook](http://apistylebook.com/), learning from all the API design guides it has aggregated. There is a wealth of knowledge in there to learn from, and contains topics that make for great stories here on the blog. I wish more API providers would actively publish their API governance strategy, so that we can keep aggregating, and learning from each other. Making the wider API space more consistent, and hopefully more reliable along the way.
