---
published: true
layout: post
title: 'Turning The Stack Exchange Questions API Into 25 Separate Tech Topic Streaming'
image: http://kinlane-productions2.s3.amazonaws.com/algorotoscope/builder/filtered/80_168_800_500_0_max_0_1_-1.jpg
---

<p><img src="https://kinlane-productions2.s3.amazonaws.com/algorotoscope/builder/filtered/80_168_800_500_0_max_0_1_-1.jpg" width="40%" align="right" style="padding: 15px;" />
<p><a href="http://streamdata.io">I’m turning different APIs into topical streams using Streamdata.io</a>. I have been profiling hundreds of different APIs as part of my work to build out the <a href="http://api.gallery.streamdata.io/">Streamdata.io API Gallery</a>, and as I’m creating OpenAPI definitions for each API, I’m realizing the potential for event and topical driven streams across many existing web APIs. One thing I am doing after profiling each API is that I benchmark them to see how often the data changes, applying what we are calling StreamRank to each API path. Then I try to make sure all the parameters, and even enum values for each parameter are represented for each API definition, helping me see the ENTIRE surface area of an API. Which is something that really illuminates the possibilities surrounding each API.

<p>After profiling <a href="https://api.stackexchange.com/docs/questions#order=desc&amp;sort=activity&amp;tagged=php&amp;filter=default&amp;site=stackoverflow&amp;run=true">the Stack Exchange Questions API</a>, I began to see how much functionality and data is buried within a single API endpoint, and was something I wanted to expose and make much easier to access. Taking a single OpenAPI definition for the Stack Exchange Questions API:

<script src="https://gist.github.com/kinlane/ab5c043fc2aa08fc233935e57e24d217.js"></script>

<p>Then exploding it into 25 separate tech topic streaming APIs. Taking the top 25 enum value for the tags parameter for the Stack Overflow site, and exploding into 25 separate streaming API resources. To do this, I’m taking each OpenAPI definition, and generating an AsyncAPI definition to represent each possible stream:

<script src="https://gist.github.com/kinlane/cab2b55c14b8fe0b6dab3ef9d198e2d2.js"></script>

<p>I’m not 100% sure I’m properly generating the AsyncAPI currently, as I’m still learning about how to use the topics and streams collections properly. However, the OpenAPI definition above is meant to represent the web API resource, and the AsyncAPI definition is meant to represent the streaming edition of the same resource. Something that can be replicated for any tag, or any site that is available via the Stack Exchange API. Turning the existing Stack Exchange API into streaming topic APIs, that people can subscribe to only the topics they are interested in receiving updates.

<p>At this point I’m just experimenting with what is possible with OpenAPI and AsyncAPI specifications, and understanding what I can do with some of the existing APIs I am already using each day. I’m going to try and turn this into a prototype, delivering streaming APIs for all 25 of the top Stack Overflow tags. To demonstrate what is possible on Stack Exchange, but also to establish a proof of concept that I can apply to other APIs like Reddit, Github, and others. Then eventually automating the creation of streaming topic APIs using the OpenAPI definitions for common APIs, and <a href="http://streamdata.io">the Streamdata.io service</a>.


