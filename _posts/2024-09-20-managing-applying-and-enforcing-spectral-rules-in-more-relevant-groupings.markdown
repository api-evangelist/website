---
published: true
layout: post
title: 'Managing, Applying, and Enforcing Spectral Rules in More Relevant Groupings'
tags:
  - Spectral
  - Rules
  - Governance
  - Linting
  - Organization
  - Lifecycle
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/eugenics-lane-1-2-3.jpeg
---
Spectral has the ability to extend API governance rulesets by layering on the core default set that comes with additional layers.  If you have a strategy for how you craft your rulesets, and a layered approach to applying them you can start to get more sophisticated in how you apply and enforce API governance. However, there is no way to define the metadata, taxonomy, or other bounded context for rulesets making them pretty difficult to orchestrate in any meaningful way across the API lifecycle—-it tends to be all or nothing. This reality has pushed me to organize my rules in other more meaningful ways, providing more context to how and when Spectral rules get applied, and reducing the information overload for teams producing APIs.

I am experimenting with other ways to organize rules and add to the metadata rulesets have, but here are the ways in which I am grouping my rules to make more relevant:

- **Policies** - Using an additional policies schema to organize Spectral rules based upon business policies that define the how and why we are applying rules in the first place.
- **Lifecycle** - Using an additional lifecycle schema to organize Spectral rules based upon each stage of the API lifecycle, allowing teams to know when rules get applied.
- **Platform** - Organizing rulesets as part of another APIs.json definition that is dedicated to the business or engineering platform, associating with other services being used.
- **Solutions** - Using an additional solutions schema to organize Spectral rules based upon the solution being applied as part of a specific area  and need for API operations.

It is easy for me to orchestrate using many different rules across these dimensions. Policies allow me to organize by business strategy, the lifecycle allows me to make it time-based, platform is associated with the infrastructure and services I use to deliver my APIs, and solutions help teams focus on specific problem areas that need addressing. I also wish Spectral rules had more metadata for giving them names, descriptions, and applying tags. The need to discover, organize, and apply API governance rules in specific contexts is only growing, and I am a fan of providing a mix of options to help scratch this itch.

Platform is just an APIs.json that I will reference specific rulesets. However, policies, lifecycle, and solutions will be added to the API Commons, providing a common reusable schema that anyone can put to work. Once I finish more research in how Radically and Vacuum approach rules management, I will weave both of these options into my approach to grouping not rules Spectral rules, but any other rules in different ways. I am also considering how Open Policy Agent (OPA) can be woven into this mix as I expand API governance to touch on more aspects of the API run-time. My goal is to provide a flexible approach to managing many different rules, but have them organized so they can be intelligently applied and evolved over time.