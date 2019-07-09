---
published: true
layout: post
title: Providing Embeddable API Integrations For Non-Developers With Zapier
date: 2017-09-25T09:00:00.000Z
tags:
  - API Evangelist
  - Embeddable
  - iPaaS
image: 'https://s3.amazonaws.com/kinlane-productions/zapier/zapier-embeddable-zaps.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/zapier/zapier-embeddable-zaps.png" align="right" width="40%" style="padding: 15px;" /></p>I'm regularly working to make APIs more accessible to non-developers, and [Zapier](https://zapier.com/app/explore) is the #1 way I do this. Zapier provides ready-to-go API integration recipes for over 750 APIs, providing IFTTT-like functionality, but in a way that actual pays the whole API thing forward (Zapier has APIs, IFTTT does not). One of the benefits of having APIs is you can build embeddable tooling on top of them, and [Zapier has some basic embeddable tools available to anyone](https://zapier.com/developer/documentation/v2/shared-zaps/#embedding-your-zaps), with some more advanced options for [partners via their partner API](https://zapier.com/developer/documentation/v2/zap-templates-partners-api/).

Using the Zapier basic embeddable widget you can list one or many Zaps, providing recipes for any user to integrate with one or many APIs, that can be embedded into a web page, or within an application:

&#x3C;script type=&#x22;text/javascript&#x22; src=&#x22;https://zapier.com/zapbook/embed/widget.js?guided_zaps=2618,1035,977&#x22;&#x3E;&#x3C;/script&#x3E;

All you do is add the id for each of the Zaps you wish to list, under the "guided_zaps" variable, and it will list the icon, title, and "use this zap" functionality, all wrapped in the appropriate powered by Zapier branding. I'm developing lists of useful Zaps ranging from working with Google Sheets, to managing social media presence on Twitter and Facebook. Everyday, useful things that the average user might find valuable when it comes to automating, and taking control over their online presence. Anytime I reference possible API integration use cases in a story, I'm going to start embedding a widget of actual Zaps you can use to accomplish whatever I'm talking about below.

I'm also trying to carve out time to develop some of my own Zaps, and sign up to become a Zapier partner, so I can begin to develop some more advanced editions of embeddable tooling. I want to make my own JavaScript library that will spider any text in a story, and turn references to API integration into popup tooltips, with API literacy, training, and action links. I have a handful of API 101 style solutions I'd like to see exist, but at this point it is a matter of carving out the time to make happen. I'm working to invest more in my guidance for my power user, non-developer audience, continuing to put APIs within reach for everyone--not just the developer, IT, and startup community.
