---
published: true
layout: post
title: 'Positive and Negative Spectral Rules for API Governance'
tags:
  - Spectral
  - Rules
  - Governance
  - Linting
  - Behavioral
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/america-immigration_dumping-ground-dandelions-in-rocks.jpg
---
One of the biggest challenges I encounter using Spectral rules (and linting) is that it focuses primarily on what is wrong. I’ve seen enterprise after enterprise turn on many Spectral rules for teams instantly telling them hundreds of things they’ve done wrong. Fun. There is a lot of research out there that will tell you that you won’t get very far in your API governance efforts if you just sit there and tell people what they’ve done wrong. Which is why I work to always have a positive and negative version of a rule that helps guide teams rather than just throw problems their way.

A negative rule focuses on what is missing from an API, things like schema descriptions or operation unique identifiers. These are rules that will impact real-world things like documentation and SDK generation, so you want to be governing when they are missing. However, you shouldn’t stop there. You should also have a positive version that will tell you when schemas have descriptions and when operations have unique identifiers. Then you can show teams all the work they have already done, and better contrast what has been done and what still needs to be done.

Both positive and negative rules provide an opportunity to turn every encounter with API governance into a learning opportunity. Rules should always provide a simple message in the moment, but provide a more comprehensive description that could also link to details about the underlying schema being listed as well as guidance helping educate teams producing APIs. Governance shouldn’t just be enforced, it should also guide teams. Positive and negative Spectral rules is how I am mapping the landscape of where governance is applied, but also focusing on the patterns and anti-patterns I am looking to exist across this landscape.