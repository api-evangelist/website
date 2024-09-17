---
published: true
layout: post
title: 'Do We Build Tooling for API Product Managers or Project API Operations Into Tools They Already Use?'
tags:
  - Business
  - Products
  - Product Managers
  - Services
  - Tooling
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/citizenship-old-tools.jpeg
---
I keep [coming across discussions around how we get more API product managers involved in the API lifecycle](https://www.linkedin.com/posts/francoislasne_oas-tooling-oas-tooling-are-activity-7239668047412695042-TJ1e), and one thing that keeps coming up involves the creation of tooling that is accessible to these business stakeholders. I agree, I’d been investing a lot in getting product managers to work with YAML and GitHub, and keep asking what other tools they use, but the conversation always seems to go back to building something new to make APIs accessible to stakeholders, but I am always skeptical when we speak of new technical solutions rather than using the ones we already have.

There was a lot of rhetoric around OpenAPI making YAML available back in 2016, and that this would make the specification more accessible to business stakeholders. I’ve seen only light evidence to support this, but it is still an uphill battle to convince non-developers to use YAML, and GitHub for editing still has strong resistance. I personally don’t think editing YAML (outlines) via GitHub (social network) is outside the realm of a serious API product manager, but I understand that we still need to bridge this divide with other solutions. I am interested in discussing what new API services or tooling will look like for API product managers, but I feel like we should be looking for API-driven integration and automation via the tools they already use before we add new ones into the mix.

I have piped the parts and pieces of an OpenAPI into Jira, Confluence, GitHub issues, and Google Sheets over the years. I am sure there are more intelligent ways we could keep the source of truth for an API machine-readable via YAML in GitHub, but then use CI/CD, APIs, and web hooks to engage API product managers in the tools they already depend on, rather than introducing something new into the stack. I am looking for ways to project API contracts (APIs.json + OpenAPI) into other tools at each stage of the life cycle. I am exploring how we can kick off the name, description, and use cases for an API in average everyday tools like Jira, Notion, or even a Google Sheet template, then produce the initial APIs.json and OpenAPI from there. As much as I’d like business stakeholders to feel comfortable creating an APIs.json or OpenAPI in YAML, I just don’t think it is going to always fly.

The immediate startup and venture fueled impulse is always to create a new technology solution for API product managers to engage across the API lifecycle—-maybe. But, I want to exhaust all interesting integrations between API contracts (APIs.json + OpenAPI) YAML in a GitHub repository and common everyday business tooling via APIs and Webhooks first. I want to explore more conversations with API product managers about what tooling they already depend on, and which aspects of API operations they need more engagement with. I have a lot of historical notes from enterprise API product managers I’ve talked to over the years, books that folks I know have written, but I’d like to have some fresh conversations with business stakeholders about where I should be investing. If you are an API product manager, [feel free to ping me directly](mailto:kin@apievangelist.com), share any thoughts via social media, or via your own blog. I’d love to learn more about how to be more pragmatic about building bridges between product and engineering across API operations, closing the divide that I see exist across almost every business sector.

