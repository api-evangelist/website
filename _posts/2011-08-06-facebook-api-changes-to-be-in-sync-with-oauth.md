---
layout: post
title: "Facebook API Changes to Be in Sync with OAuth"
url: 'http://apievangelist.com/2011/08/06/facebook-makes-change-to-be-in-sync-with-oauth-spec/'
image: ''
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/facebook/facebook-operation-developer-love.png" alt="" width="150" align="right" />In order to be compliant with the [OAuth spec][1], [Facebook is making changes to their auth APIs][2]. As part of this update, they will be deprecating 'code_and_token' and need developers to use 'code token'. Everything else is identical, just replace '_and_' with encoded' '.

For example, this call:

It will need to change to:

Developers are required to make this change by November 5th, 2011, and Facebook has [updated their roadmap][3] to reflect this.

The communication coming from Facebook Operation Developer Love, and their willingness to [open up their API roadmap][4] is something other API owners should consider in their own ecosystem.

   [1]: http://tools.ietf.org/html/draft-ietf-oauth-v2-20 (oAuth Spec)
   [2]: http://developers.facebook.com/blog/post/533/ (Facebook is making changes to their auth APIs)
   [3]: http://developers.facebook.com/roadmap/ (updated their roadmap)
   [4]: http://blog.apievangelist.com/2011/08/01/how-open-should-we-be-with-our-api-road-maps/ (open up their roadmap)
