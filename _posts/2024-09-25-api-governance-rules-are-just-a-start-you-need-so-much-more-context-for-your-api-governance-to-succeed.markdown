---
published: true
layout: post
title: 'API Governance Rules Are Just a Start—You Need So Much More Context for Your API Governance To Succeed'
tags:
  - Governance
  - Rules
  - Context
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/gone-with-the-wind-emergency-third-rail-power-trip.jpeg
---
I am endlessly fascinated with the belief that enterprise leadership has in Spectral rules, and the number of companies I’ve seen just turn on Spectral rules in their CI/CD pipelines and other automation believing that they will “govern” their APis. Some Spectral rules you can use out of the box with the CLI or other tooling, but most you will have to tweak and adjust, and there will always come a time where you have to get to work crafting your own rules. Even with this reality and work, all of these rules will only get you so far, and you need a lot more context for your API governance to succeed.

These are the additional areas of context I invest in when it comes to the governance of HTTP APIs:

- **Domain** - What are the rules that apply and do not apply with the domain, line of business, where my team and APIs operates within.
- **Business** - What is the business context for why we have a rule and what is the provenance of these rules.
- **Lifecycle** - When should a rule be applied and when is it not necessary, helping me understand the right time.
- **Solutions** - What are downstream impacts of rules on solutions like documentation, mocking, and security.
- **Guidance** - What guidance is available to support me at the moment each rule is being applied to an API.
- **Exceptions** -  How can an exception be achieved to help reduce friction in unique scenarios involving my API.

If you are just turning on and enforcing API governance rules without more context you aren’t going to make the first impression you desire with your API governance efforts. This is my biggest frustration with any API governance solutions out there right now-—they don’t allow for this context. The Spectral rule schema doesn’t provide you with this context, and it is ultimately something you have to augment and organize your rules with, executing modular rulesets within these contexts during design, develop, and built times. These are the areas in which I link individual rules to the greater enterprise and strategic context, helping ensure your API governance will be successful.