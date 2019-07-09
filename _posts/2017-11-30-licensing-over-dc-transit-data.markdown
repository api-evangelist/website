---
published: true
layout: post
title: >-
  Troubling Terms of Service Changes From Washington Metropolitan Area Transit
  Authority (WMATA) Data APIs
date: 2017-11-30T11:00:00.000Z
tags:
  - API Evangelist
  - Terms of Service
  - Transit
  - City Government
  - Transportation
  - Communication
image: >-
  https://s3.amazonaws.com/kinlane-productions/transit/wmata-transit-terms-of-service.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/transit/wmata-transit-terms-of-service.png" align="right" width="45%" style="padding: 15px;" /></p>[I was turned onto a developing problem within the Washington Metropolitan Area Transit Authority (WMATA) around a recent terms of service change made around the transit data API by Technically DC](https://technical.ly/dc/2017/11/22/developers-upset-wmatas-new-data-terms-use/). While the transit authority is saying the changes are business as usual and make sense for the platform, some of the developers, specifically one of the biggest API users [MetroHero](https://dcmetrohero.com/) says the changes are targeting them specifically.

MetroHero presented what they feel are the unreasonable changes to the WMATA API terms of service in a WMATA Board Meeting recently, focusing on four main areas:

- That no user or developer can mention “WMATA” in press releases without letting WMATA first review it.
- That WMATA can gain access to any user’s applications that use the data, can audit personnel information for anyone working on those applications, and WMATA can also create their own version at any time.
- That WMATA forbids users from claiming their data is accurate, complete or timely, or claiming it is more so than WMATA’s data.
- That the transit agency may now charge users in the future for using their data.

These are all common changes I've seen made to API terms of service before, and are usually signs that a platform operator that is pretty out of touch with what it is like to be an API consumer, and with their own API community. It is a sign of a broken or pernicious feedback loop which leads to API providers making decisions that do lasting damage to their communities like this. These types of changes [reflects the "rules of road" terms of service changes Twitter made to back in 2012](https://www.wired.com/2012/09/twitters-new-rules-of-the-road-means-some-apps-are-roadkill/). Which didn't fully kill off the Twitter API, but set such a bad tone in the community, the company is still working to dig out of it five years later. I know platform operators feel they need to assert this level of control, but in an API community you need to learn to let go a little, communicate, and work with your community, not against them.

I'm going to work through all of these bullet points as separate stories, and try to help other API providers, as well as the WMATA understand how they might be able to handle these types of requests better. Doing it in a way that doesn't cause irreparable damage to their communities, and still achieves their objectives. However, I will emphasize that I think if WMATA spent more time actually communicating with their developers, especially the leading ones like MetroHero, you'd probably see how ridiculous your requests area in the first place. APIs are not just about you opening up access to your data, it is about opening up access to your processes, and feedback loops, and collaborating with your community. It isn't about command and control, and broadcasting the rules of the road for you platform--Twitter showed us this does not work well in todays environment.
