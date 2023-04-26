---
published: true
layout: post
title: Organizing My APIs Using OpenAPI Tags
date: 2019-06-19T12:00:00.000Z
tags:
  - API Evangelist
  - OpenAPI
image: >-
  https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/aws-s3-stories-containership-copper-circuit.jpg
author:
 name: kinlane
tags:
    - None
---
I like my OpenAPI tags. Honestly, I like tags in general. Almost every API resource I design ends up having some sort of tagging layer. Too help me organize my world, I have a centralized tagging vocabulary that I use across my JSON Schema, OpenAPI, and AsyncAPI, to help me group, organize, filter, publish, and maintain my catalog of API and schema resources.

The [tag object for the OpenAPI specification](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.2.md#tagObject) is pretty basic, allowing you to add tags for an entire API contract, as well as apply them to each individual API method. Tooling, such as API documentation uses these tags to group your API resources, allowing you to break down your resources into logical bounded contexts. It is a pretty basic way of defining tags, that can go a long ways depending on how creative you want to get. I am extending tags with an OpenAPI vendor extension, but I also see that there is [a issue submitted suggesting they move the specification forward by allowing for the nesting of tags](https://github.com/OAI/OpenAPI-Specification/issues/1367)--potentially taking OpenAPI tagging to the next level.

I'm allowing for a handful of extensions to the OpenAPI specification to accomplish the following:

- **Tag Grouping** - Help me nest, and build multiple tiers of tags for organization APIs.
- **Tag Sorting** - Allowing me to define a sort order that goes beyond an alphabetical list.

I am building listing, reporting, and other management tools based up OpenAPI tagging to help me in the following areas:

- **Tag Usage** - Reporting how many resources are available for each tag, and tag group.
- **Tag Cleanup** - Helping me de-dupe, rename, deal with plural challenges, etc.
- **Tag Translations** - Translating old tags into new tags, helping keep things meaningful.
- **Tag Clouds** - Generating D3.js tag clouds from the tags applied to API resources.
- **Packages** - Deployment of NPM packages based upon different bounded contexts defined by tags.

I am applying tags to the following specifications, stretching my OpenAPI tagging approach to be more about a universal way to organize all my resources:

- **JSON Schema** - All schema objects have tags to keep organized.
- **OpenAPI** - Each API method have tags, for easy grouping.
- **AsyncAPI** - Each pub/sub, event, and message API have APIs.
- **APIs.json** - Collections of APIs have tags for discoverability.

Tags are an important dimension of API discoverability when it comes to my API definitions. They provide rich metadata that I can use to make sense of my API infrastructure. Without them, the quality of my API definitions tend to trend lower. By evolving the tagging schema, and investing in tooling to help me make sense across the API definitions I'm depending on, I can push the boundaries of how I tag, and evolve it to be the core of how I manage my API definitions.

I'll keep watching how others are tagging their APIs, although I don't see too much innovation, and low levels of usage by other API providers as part of their API definitions. I'll also keep an eye out for other ways in which tag schema are being extended, helping potentially define the future of how the leading API specifications enable tagging. I have a short list of tooling I am developing to help make my life easier, but I'm working hard to just make sure I'm applying tags across my API resources in a consistent way. I find this is the most valuable aspect of API tagging, but eventually I'm guessing that the tooling will make the real difference when it comes to slicing and dicing, and making sense of my API infrastructure at scale.
