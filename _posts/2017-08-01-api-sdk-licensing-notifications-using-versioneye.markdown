---
published: true
layout: post
title: API SDK Licensing Notifications Using VersionEye
date: 2017-08-01T11:00:00.000Z
tags:
  - API Evangelist
  - SDK
  - Licensing
  - Monitoring
image: >-
  https://s3.amazonaws.com/kinlane-productions/versioneye/01-veye-licenses-7679418f2968513011985476db94b59b0ab65abd5c030a6a92189fc0e1170722.png
---
<p><a href="https://www.versioneye.com/"><img src="https://s3.amazonaws.com/kinlane-productions/versioneye/01-veye-licenses-7679418f2968513011985476db94b59b0ab65abd5c030a6a92189fc0e1170722.png" align="right" width="40%" style="padding: 15px;" /></a></p>I have been watching [VersionEye](https://www.versioneye.com/) for a while now. If you aren't familiar, they provide a service that will notify you of security vulnerabilities, license violations and out-dated dependencies in your Git repositories. I wanted to craft a story specifically about their licensing notification services, which can check all your open source dependencies against a license white list, then notify you of violations, and changes at the SDK licensing level.

The first thing I like here, is the notion of an API SDK licensing whitelist. The idea that there is a service that could potentially let you know which API providers have SDKs that are licensed in a way that meets your integration requirements. I think it helps developers who are building applications on top of APIs understand which APIs they should or shouldn't be using based upon SDK licensing, while also providing an incentive for API providers to get their SDKs organized, including the licensing--you'd be surprised at how many API providers do not have their SDK house in order.

VersionEye also provides CI/CD integration, so that you can stop a build based on a licensing violation. Injecting the politics of API operations, from an API consumers perspective, into the application lifecycle. I'm interested in VersionEye's CI/CD, as well as security vulnerabilities, but I wanted to make sure this approach to keeping an eye on SDK licensing was included in my [SDK](http://sdk.apievangelist.com), [monitoring](http://monitoring.apievangelist.com), and [licensing](http://licensing.apievangelist.com) research, influencing my storytelling across these areas. Some day all API providers will have a wide variety of SDKs available, each complete with clear licensing, published on Github, and indexed as part of an [APIs.json](http://apisjson.org). We just aren't quite there yet, and we need more services like VersionEye to help build awareness at the API SDK licensing level to get us closer to this reality.
