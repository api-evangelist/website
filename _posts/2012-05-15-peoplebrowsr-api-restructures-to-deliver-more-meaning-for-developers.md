---
layout: post
title: "PeopleBrowsr API Restructures to Deliver More Meaning for Developers"
url: 'http://apievangelist.com/2012/05/15/peoplebrowsr-api-restructures-to-deliver-more-meaning-for-developers/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/kr_pb_logo.png'
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/peoplebrowsr/kr_pb_logo.png" alt="" width="250" align="right" />][1]

Explaining to developers, what an API does, can be hard. How you describe your API, the underlying endpoints, can make or break user adoption. You shouldn’t be afraid to evolve, and keep trying to find the sweet spot in both the language and branding that you use in your API area.

I saw an example of this today, with the restructuring of [PeopleBrowsr's APis][2]. When I first starting playing with PeopleBrowsr's APIs, they were broken into 3 separate APIs:

  * PeopleBrowsr API
  * Kredentials API
  * Kred API

On the surface its really hard to know what each of these APIs does, but after I dove in I saw lots of value within individual methods, but I really had to spend time, getting to know each method, one by one. I saw the value, but the structure and presentation of the PeopleBrowsr API area, and the way the interfaces were assembled, didn’t immediately speak to this value.

Today they’ve restructured their three APis into a single API, dubbed the [PeopleBrowsr Kred API][1], and grouped all the API methods into four logical groups:

<img src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/peoplebrowsr/kred-dashboard.png" alt="" width="300" align="right" />

  * **[Find Influencers][3]** \- Pinpoints influential people on any subject or within communities connected by shared interests or affinities.
  * **[Deep Analytics][4]** \- Author-based analytics which includes Kredentials (a single-screen summary of anyone’s social presence), historical Kred scores, reach, and friends

   [1]: https://developer.peoplebrowsr.com/ (PeopleBrowsr Kred API)
   [2]: https://developer.peoplebrowsr.com/
   [3]: https://developer.peoplebrowsr.com/find (Find Influencers)
   [4]: https://developer.peoplebrowsr.com/deep (Deep Analytics)
