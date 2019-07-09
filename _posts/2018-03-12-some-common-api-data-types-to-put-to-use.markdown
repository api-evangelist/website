---
published: true
layout: post
title: Some Common API Data Types To Put To Use
date: 2018-03-12T13:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Standards
  - Definitions
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/carryload_dali_three.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I'm continuing my exploration of the API design guidance published by leading API providers. This time, I am taking a look at the API design guide publish by Adidas, [specifically the portion of it addressing what some of the common API types should be](https://adidas-group.gitbooks.io/api-guidelines/content/application/common-data-types.html). Providing some API design essentials, that all of us API providers should be baking into our APIs by default.

Here is the short list of [default standards Adidas](https://adidas-group.gitbooks.io/api-guidelines/) is supporting across their API operations:

- **Date and Time Format** - Date and Time MUST always conform to the [ISO 8601 format](https://en.wikipedia.org/wiki/ISO_8601) e.g.: 2017-06-21T14:07:17Z (date time) or 2017-06-21 (date), it MUST use the UTC (without time offsets).
- **Duration Format** - Duration format MUST conform to the [ISO 8601 format](https://en.wikipedia.org/wiki/ISO_8601) standard e.g.: P3Y6M4DT12H30M5S (three years, six months, four days, twelve hours, thirty minutes, and five seconds).
- **Time Interval Format** - Time Interval format MUST conform to the [ISO 8601 format](https://en.wikipedia.org/wiki/ISO_8601) standard e.g.: 2007-03-01T13:00:00Z/2008-05-11T15:30:00Z.
- **Standard Time Stamps** - Where applicable, a resource representation SHOULD contain the standard timestamps: createdAt, updatedAt, and finishedAt, using the [ISO 8601 format](https://en.wikipedia.org/wiki/ISO_8601).
- **Language Code Format** - Language codes MUST conform to [the ISO 639](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) e.g.: en for English.
- **Country Code Format** - Country codes MUST conform to [the ISO 3166-1](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) alpha-2 e.g.: DE for Germany.
- **Currency Format** - Currency codes MUST conform to [the ISO 4217](https://en.wikipedia.org/wiki/ISO_4217) e.g.: EUR for Euro.

These are the common data formats we are all using across our APIs. We should be working to support standard formats wherever possible, embracing the wider web, and investing in the longevity and usability of our API designs. Making our APIs sure that they speak to as wide of audience as they possibly can, and operate in a consistent way, no matter which API you are integrating with.

I want to also give a shout out to the [API Stylebook](http://apistylebook.com/), where I'm easily finding these API design guides that I'm using for these stories, and including in my API design guidance in my consulting work. Also, I'd like to encourage other API providers to reuse the patterns present in these guides, as well as publishing their own API design governance guidance whenever possible. It is critical that we all share these stories, so that we can learn from each other, and emulate the healthiest patterns already in use across the space.
