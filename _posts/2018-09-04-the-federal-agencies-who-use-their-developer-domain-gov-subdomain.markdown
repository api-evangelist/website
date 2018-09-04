---
published: true
layout: post
title: 'The Federal Agencies Who Use Their developer.[domain].gov Subdomain'
date: 2018-09-04T09:00:00.000Z
tags:
  - API Evangelist
  - Federal Government
  - DNS
  - Portals
image: >-
  https://s3.amazonaws.com/kinlane-productions/federal-government/federal-goverment-portals.png
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I was reviewing the new developer portal for the Department of Veterans Affairs (VA), and one of things I took notice of, was their use of the developer.va.gov subdomain. In my experience, the API efforts that invest in a dedicated subdomain, and specifically a developer dot subdomain, tend to more invested in what they are doing than efforts that publish to a subfolder, or subsection of their website. As I was writing this post, I had a question in arise in my mind, regarding how many other federal agencies use a dedicated subdomain for their developer programs--something I wanted to pick up later, and understand the landscape a little more.

I took a list of current federal agency domains from the GSA and wrote a little script to append developer. to each of the domains, and conduct an HTTP status code check to see whether or not these pages existed. Here are the dedicated developer areas I found for the US federal government:

- **Department of Veterans Affairs (VA)** - https://developer.va.gov/
- **Department of Labor** - https://developer.dol.gov
- **International Trade Administration (ITA)** - https://developer.trade.gov & https://developer.export.gov
- **United States Patent and Trademark Office** - https://developer.uspto.gov
- **National Renewable Energy Laboratory** - https://developer.nrel.gov
- **Centers for Medicare & Medicaid Services** - https://developer.cms.gov
- **The Advanced Distributed Learning Initiative** - http://developer.adlnet.gov & http://developers.adlnet.gov
- **United States Environmental Protection Agency** - http://developer.epa.gov
- **USA Jobs** - http://developer.usajobs.gov

These nine agencies have decided to invest in a subdomain for their developer portals. I have to recognize two others who provide these subdomains, but then redirect to a subsection of their websites:

- **National Park Service** - http://developer.nps.gov redirect to https://www.nps.gov/subjects/developer/index.htm
- **Data.gov** - http://developer.data.gov redirects to https://www.data.gov/developers/

Additionally, there is a single domain I noticed that used the plural version of the subdomain:

- **Code.gov** - https://developers.code.gov (plural)

Along the way, I also noticed that many agencies would redirect their subdomain, and I assume all subdomains to the root of their agency's domain. Ideally, all federal agencies would have a Github account, and publish a developer portal using Github Pages, and publish the developer.[agencydomain].gov as the address for the portal. Even if they just provide access to the agency's data inventory, it is important to lay down the foundation for a developer platform across data, APIs, and open source software out of all federal agencies, providing a common, well-known location develop upon the government platform.

As part of my larger API discovery work I am going to keep lobbying that federal agencies work to publish a common developer.[agencydomain].gov portal. It would begin to transform how applications are built if you knew that you could automatically find a government agency's data, APIs, and open source tooling at a single location. Especially if it was something that was default across ALL federal agencies, who were also actively publishing their public data assets, entire API catalog, and showcase of open source solutions they depend on and produce.
