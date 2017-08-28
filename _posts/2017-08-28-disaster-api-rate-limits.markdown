---
published: true
layout: post
title: Disaster API Rate Limit Considerations
date: 2017-08-28T11:00:00.000Z
tags:
  - API Evangelist
  - Mapping
  - Rate Limits
  - Management
  - Support
  - Disasters
image: >-
  https://s3.amazonaws.com/kinlane-productions/google-maps/google-maps-hurricane-harvey.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/google-maps/google-maps-hurricane-harvey.png" align="right" width="40%" style="padding: 15px;" /></p>This API operations consideration won't apply to every API, but for APIs that provide essential resources in a time of need, I wanted to highlight an API rate limit cry for help that came across my desk this weekend. [Our friend over at Pinboard alerted me](https://twitter.com/Pinboard/status/901658084002713600) to someone in Texas asking for some help in getting Google to increase the Google Maps API rate limits for an app they were depending on as Hurricane Harvey:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Hey <a href="https://twitter.com/Google">@google</a> <a href="https://twitter.com/googlemaps">@googlemaps</a> <a href="https://twitter.com/GoogleMapsAPI">@googlemapsapi</a> can you please remove the limit on api access for <a href="https://twitter.com/ATXfloods">@atxfloods</a>? This is an emergency and we rely on it.</p>&mdash; Jen Savage (@savagejen) <a href="https://twitter.com/savagejen/status/901656342213033984">August 27, 2017</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

The app they depended on had ceased working and was showing a Google Maps API rate limit error, and they were trying to get the attention of Google to help increase usage limits. As Pinboard points out, it would be nice if Google had more direct support channels to make requests like this, but it would be also great if API providers were monitoring API usage, aware of applications serving geographic locations being impacted, and would relax API rate limiting on their own. There are many reasons API providers leverage their API management infrastructure to make rate limit exceptions and natural disasters seems like it should be top of the list.

I don't think API providers are being malicious with rate limits in this area. I just think it is yet another area where technologists are blind to the way technology is making an impact (positive or negative) on the world around us. Staying in tune to the needs of applications that help people in their time of need seems like it will have to components, 1) knowing your applications (you should be doing this anyways) and identifying the ones that have a public service, and 2) staying in tune with natural and other disasters that are happening around the world. We see larger platforms like Facebook and Twitter rolling out permanent solutions to assist communities in their times of needs, and it seems like something that other smaller platforms should be tuning into as well.

Disaster support and considerations will be an area of API operations I'm going to consider adding into my research, and spending more time to identify best practices, and what platforms are doing to better serve communities in a time of need using APIs.
