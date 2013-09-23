---
layout: post
title: "Hunch's Clear Vision of Privacy and OAuth"
url: 'http://apievangelist.com/2011/06/13/hunchs-clear-vision-of-privacy-and-oauth/'
image: ''
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/hunch/hunch-logo.png" alt="" align="right" />Having a [privacy policy on your API][1] is an important part of making it clear to developers and end-users, where your company stands in regard to their data and personal privacy.

Just having a privacy policy is not enough, make sure it truly reflects your companies values, whats important to your users, and is in line with how you deploy your technology.

One shining example of this in the API space, is [Hunch][2]. Hunch's provides a 'Taste Graph' of the entire web, providing information on what people like; anything, from books to electronic gadgets to fashion or vacation spots.

Hunch is combining algorithmic machine learning with user-curated content, with the goal of providing better recommendations for everyone. The information they provide through their web application and API, is extremely valuable, as well as potentially very private.

[Hunch's API privacy policy][3] articulates their position very clearly:

> _Hunch takes our users' privacy very seriously. When using the API, Hunch returns predictions for users within the Taste Graph. Certain API calls can be made for any user, while other calls require the user to Hunch Connect before predictions will be returned. Our guiding principle for this distinction is whether the user's likes or facts about themselves are already made public on the internet._

Obviously the privacy of their users is very important, and they back this up by using [OAuth][4] as it is meant to be used. Giving users granular level control over who has access to their sensitive data, while still providing other, non-sensitive, rich data without authentication.

Hunch has a clear vision of API and data privacy in a space, where there is a lot of potential for abuse. An example that many other API providers should follow.

Also make sure and check out the [privacy policy for their main site][5], they really lay it out honestly, and in plain english. I wish more technology providers would approach privacy this way.

**Update:** From my girl [Audrey Watters][6] @ [RWW][7]: [Dixon made it clear that despite Hunch's ability to predict users' tastes that the company would never sell that data. "We have never made a data deal," said Dixon. Furthermore, people can only get predictive information about themselve][8]s.

   [1]: http://www.apievangelist.com/ecosystem-building-blocks-detail.php?Building_Block_ID=165 (privacy policy on your API)
   [2]: http://hunch.com/ (Hunch)
   [3]: http://hunch.com/developers/v1/docs/privacy/ (Hunch's API Privacy Policy)
   [4]: http://www.apievangelist.com/ecosystem-building-blocks-detail.php?Building_Block_ID=184 (OAuth)
   [5]: http://hunch.com/info/privacy-policy/ (privacy policy on their main site)
   [6]: http://www.hackeducation.com (Audrey Watters)
   [7]: http://www.readwriteweb.com (RWW)
   [8]: http://www.readwriteweb.com/archives/chris_dixon_hunch_taste_graphs_the_link_between_le.php
