---
layout: post
title: Facebook API Changes to Be in Sync with OAuth
url: http://apievangelist.com2011/08/06/facebook-makes-change-to-be-in-sync-with-oauth-spec/
source: http://apievangelist.com2011/08/06/facebook-makes-change-to-be-in-sync-with-oauth-spec/
domain: apievangelist.com2011
image: 
---
{% include JB/setup %}<p>In order to be compliant with the OAuth spec, Facebook is making changes to their auth APIs.As part of this update, they will be deprecating code_and_token and need developers to use code%20token.Everything else is identical, just replace _and_ with encoded%20.For example, this call: It will need to change to: Developers are required to make this change by November 5th, 2011, and Facebook has updated their roadmap to reflect this.The communication coming from Facebook Operation Developer Love, and their willingness to open up their API roadmap is something other API owners should consider in their own ecosystem.</p>
<center><p><a href="http://apievangelist.com2011/08/06/facebook-makes-change-to-be-in-sync-with-oauth-spec/" style='padding:25px; font-sze:18px; font-weight: bold;'>Read Full Story</a></p></center>
