---
published: true
layout: post
title: 'Governing the Title of Your APIs With Spectral Rules'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/citizenship-satellite-dish-pointing-upwards.jpg
author:
    name: kinlane
tags:
- Governance
- Spectral
- Policies
- Rules
---
I enjoy how developing Spectral rules to govern an API slows us down to think about what matters. Really this is the biggest problem I see with people building APIs—-they are just moving too fast, and they refuse to slow down and think too deeply about things. I enjoy the frame rate in which Spectral rules attach themselves to the contracts we are producing for our APIs, and I figured I’d further expand on the opportunity to tell some stories around these machine-readable API policies we are applying, or often times not applying consistently across our API operations.

The place to start with any API governance rules storytelling is around the name of our APIs. It seems so simple, but over my 13+ years of doing this API hustle, it never surprises me to see how people refuse to provide a useful name for their APIs. Acronyms and extraneous words litter the API landscape, with many names barely even letting you know what an API does. Sometimes a name will focus more on it being REST and from a database than it will speak of the resources being made available, and other times you have to unpack several acronyms to even know what is going on—very appropriate for an API world. 

When you have read as many titles of APIs as I have, you can tell most people do not leave their own head space when naming an API. They have spent zero time thinking about how someone who knows nothing about an API will interpret the name. Most API names lack any empathy. I wanted to explore the usage of Spectral rules when it comes to shaping this most important of API properties, the name. Something that is described by the info title property in OpenAPI and AsyncAPI. I really think the Spectral rule landscape is ripe with storytelling opportunities like this, but the name of our APIs set the stone for almost everything else.

## Make Sure an API Title Exists
When it comes to governance you always begin with making sure your API has a title, which is expressed as an OpenAPI info object title property. This is a simple Spectral rule that checks to see if an API has it’s title defined—-providing an entry point for anyone looking to standardize their API catalog.
```
openapi-v3-info-title:
  description: Ensures that all OpenAPIs have a information object title.
  message: The info object should have an intuitive title for consumers.
  given: "$.info"
  severity: error
  formats:
  - oas3
  then:
    field: title
    function: truthy
```
Making sure there is a title is just the beginning. It is a good start, but really there is are multiple dimensions you should consider when it comes to an API title, not just that it exists. However, this rule should get you started with learning about how you govern an OpenAPI using Spectral, by listing the JSON or YAML contract for your API. 

## Make Sure API Title Follows a Certain Casing
When you see APIs in a list within a catalog or API discovery format, the casing of the titles of APIs really matter. If some are all caps, and others are all lowercase, then you can throw the layout off. It is a small thing, but it matters at scale when you have hundreds or thousands of APIs, contributes to the overall experience of discovering APIs for users. Here is a simple Spectral rule that ensures your titles are Kebab case, providing one possible way you can go with governing titles.
```
openapi-v3-info-title-in-kebab-case:
  description: Ensures that all OpenAPIs information title are in Kebab case.
  message: The info object title needs to be in Kebab case.
  severity: error
  formats:
  - oas3
  given: "$.info.title"
  then:
    function: pattern
    functionOptions:
      match: "^[a-z][a-z0-9\\-]*$"
```
You don’t have to go with Kebab case for your API titles, but pick a casing and work to enforce, and educate people on why it matters. Come up with examples of how it looks better in layouts. Find ways of demonstrating the business value of clean, consistent, and agreed upon casing for your APIs. It is simple, but something that will make a big difference down the road as you publish more APIs. 

## Make Sure Your API Title Is Not Too Long
Another dimension of API title governance is considering how long you want your titles to be. Like the casing, there are many reasons why you’d want them to be shorter or longer, and it helps to think about why the length matters as you are shaping this policy. Here is another rules that shows how you can set a max number of characters and govern the length of API titles along with casing.
```
openapi-v3-info-title-max-length:
  description: Ensures that all OpenAPIs information titles are not longer than 50
    characters.
  message: The info object title should not be more than 50 characters.
  given: "$.info"
  severity: error
  formats:
  - oas3
  then:
    field: title
    function: length
    functionOptions:
      max: 50
```
I recommend going to look at how other top APIs that you use or respect craft their titles. You will start seeing how their portals and other constraints help define how they name things. This rule is set to 50 as a max length, but this is arbitrary, so make sure and do your own research, and talk to others before you set the length for your rule.

## Make Sure You Do Not Have Certain Words in the Title of Your API
APIs are notorious for having useless and redundant words in the title. You see REST, Data, Database, Resource, and other common phrases in the title. Developers are good at dancing around the core value that their API delivers and talk about the things they know, and what matters to them when producing an API. This rule helps you monitor what words are used in your API titles.
```
openapi-v3-info-title-word-check:
  description: Ensures that all OpenAPIs info object title do not contain certain
    words.
  message: The info object title should not contain the words REST, Public, and Developer.
  given: "$.info.title"
  severity: error
  recommended: true
  type: style
  formats:
  - oas3
  then:
    function: pattern
    functionOptions:
      notMatch: "\\b(REST|Public|Database|Developer|Resource)\\b"
```
This list of words can get as long as you want, but nothing beats having another human, or multiple humans weigh in on what words should be used. But, this rule helps automate away some of the most common useless words you will come across. You really want to make the title 100% about the resource and capabilities being made available, so choose the words that get at this in as few words as possible.

## Naming Matters and Naming is Hard
The presence of, casing, length, and words we use in the title of our APIs sets the tone for any API discovery and onboarding experience. I am perpetually amazed by the names people choose for their APIs, as well as choosing not to give their APIs a title. APIs are hard to see, but they are even harder to see if they do not have a name. Nothing says you haven’t thought about the consumers of your more than not naming your API, or describing it in a way that doesn’t properly articulate why someone would want to use it. I get it, naming is hard, and takes muscles you probably don’t exercise often, but it is really important to name your API creations, otherwise you are just getting right up to the finish line and choosing to walk away.

These four Spectral rules provide one policy you can adopt as part of your API governance. Using Spectral you can manually or automatically lint your API contracts for these characteristics. It really is the low hanging fruit of API governance and the place everyone should begin. Personally I’d even recommend enforcing these rules for internal APIs, as well as external APIs. You can turn down the volume and make them just warnings instead of errors, and play with the message phrasing that developers see when they encounter these rules. Words matter. Naming matters. The name of the API will speak volumes when it comes to the success or failure of your API, and the tone you set will govern not just the design of your API but the relationship you have with your API consumers.
