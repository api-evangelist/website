---
published: true
layout: post
title: 'A Spectrum of API Governance Rules Work'
tags:
  - Spectral
  - Rules
  - Governance
  - Linting
  - JSON Schema
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/yellow-journalism-construction-zone-claw.jpg
---
Creating Spectral rules to lint OpenAPI definitions is equal parts art and science. When you take any of the default rules or copy and paste some rules from the style guides of popular API producers you quickly end up hitting walls in how you can apply your rules. You can do a lot with the default functions that Spectral provides but it is tempting to go from default function to custom function without properly doing the work to understand the OpenAPI you are applying the rule to, as well as the shape of the “problem” you are linting for in the first place--here is the spectrum as I see it for crafting rules.

- **JSON Schema** - Consider JSON Schema and Spectral rules side by side, and always start with JSON Schema for governing your APIs.
- **Spectral Default Functions** - Learn and strengthen your usage of all the default Spectral functions and try to do your governance here.
- **Spectral JSON Schema Function** - Consider how you can get much more modular and pedantic with the Spectral JSON Schema function.
- **Spectral Custom Functions** - Writing that custom JavaScript to do what you want with Spectral rules applied as part of API governance.

I acknowledge this list is very Spectral based and I am working on expanding this Spectrum to include Redocly and Vacuum. But, this is what I have the most experience with right now, so it is what I am focused on. An important part of this discussion is having a strong understanding of where JSON Schema fits in, before you choose to apply a Spectral rule, but I also break out the Spectral JSON Schema function as a separate layer of the spectrum. The nuance between when you apply JSON Schema or Spectral or both is a place for perpetual discovery and learning.

I can’t express how important it is to learn JSON Schema. I also can’t urge enough for you to do the work with JSON Schema and default Spectral rules functions. This work is important to API governance and I see it continuing to be lost in the discussion. Understanding this spectrum and properly doing the JSON Schema work alongside Spectral is essential maturing your approach to API governance, and something you will have to consider when it comes to ensuring the governance team or teams producing APIs have proper JSON Schema and rules education.