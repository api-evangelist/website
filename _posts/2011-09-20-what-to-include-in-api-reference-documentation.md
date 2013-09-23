---
layout: post
title: "What to Include in API Reference Documentation"
url: 'http://apievangelist.com/2011/09/20/what-to-include-in-api-reference-documentation/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/SDKBridge-logo.gif'
---

_This post comes from the [SDK Bridge][1] newsletter.  I find so much value from what Peter and Jonathan do over at SDK Bridge, I asked them if I could repost their newsletter here and share with all of you._

* * *

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/SDKBridge-logo.gif" alt="" width="250" align="right" />][1]This article presents a series of questions that your writing should answer for each type of element you would typically find in reference documentation.

To begin with, think about what a new user needs to know. If you can write for a new user, then you'll cover everything that an existing user will need to know. Once you have that mindset, answer the questions below. For a given element, some of the answers will be obvious from the context and not need to be documented, so use your judgment. In general:

  * For collaborations or common interactions or scenarios, is there a conceptual topic that discusses this? If so, link to or reference the conceptual topic from the API topic.
  * For any elements that have a user interface component, is there a design guideline topic that discusses it? If so, link to or reference the design guideline from the API topic.

For classes or structures:

  * What function does it serve?
  * What other classes or structures does it interact with? What collaborations does it participate in?
  * What is its uninitialized state, if any?
  * In which ways can you obtain an initialized object or value?
  * Who is responsible for disposing of the item? Only an issue if the item is not garbage collected.

For methods or functions:

  * What does it operate on and what does it do?
  * What are valid inputs (or states), and what are its outputs?
  * Does it have any side effects?
  * Are there any corner or edge cases, and if so, what is its expected behavior in each?
  * What exceptions or error codes can it generate?

For constants or enumerations:

  * What does the value signify?
  * Refer back to the contexts in which it occurs or is used.

For Web API requests:

  * What does it do?
  * What are its query and header parameters?
  * What does it return?
  * Does it have any side effects?
  * Are there any corner or edge cases, and if so, what is its expected behavior in each?
  * What error codes can it generate?

If your company has an existing writing team, then the team will likely already have templates or guidelines for API reference documentation that address many of the issues discussed in this article. Just remember that the mindset of the people using your documentation is going to be a bit different that the mindset of the people designing or implementing the API. As a writer, you will need to translate between the two. If you keep these things in mind, it will be easier to write accessible and useable documentation.

* * *

_If you don't know who SDK Bridge is, they provide [API and SDK documentation services][2], that will truly help developers understand how to build on top of your API. You can find more information about them at the [SDK Bridge website][1]._

   [1]: http://sdkbridge.com/ (SDK Bridge)
   [2]: http://sdkbridge.com/ (API and SDK Documentation Services)
