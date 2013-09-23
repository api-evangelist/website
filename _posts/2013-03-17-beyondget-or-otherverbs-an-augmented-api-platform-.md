---
layout: post
title: "BeyondGET or OtherVerbs, an Augmented API Platform "
url: 'http://apievangelist.com/2013/03/17/beyondget-or-otherverbs,-an-augmented-api-platform-/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/augmented-post.png'
---

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/augmented-post.png" alt="" width="300" align="right" />

I have a idea for a new API platform. Since I do not have any startup aspirations, I prefer setting my ideas free, for anyone to use, instead of acting on them myself.

This idea is an evolution from an earlier one, which I had while working with the CityGrid API, called “augmented places”.  While at CityGrid I constantly had people asking if they could submit data back to the API. Stating they had a better list of pizza places in Brooklyn or vegan restaurants in Santa Cruz. I had to always turn these folks away, and one morning I sketched out “augmented places”. It would be a service where anyone could submit their own meta data about a place, either adding an entirely new place, updating an existing one, or even remove a listing. It would provide an external service that could augment all places APIs, not just CityGrid.

Fast forward to the other night, I did some data journalism for my girlfriend Audrey ([@audreywatters][1]), which included [pulling data from the Crunchbase API][2]. I pulled 3000 education startups from around the world, then after delivering to her in a JSON object and Google Spreadsheet, I immediately used the script to pull any API related startup, for my own needs. I quickly compared a handful of results with my existing API database and in many cases, I have much better information on some of these companies than CrunchBase. Yet I have no way to submit this data back to CrunchBase, to correct or add to what they have.

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/augmented-put.png" alt="" width="300" align="right" />

This is common in the open API space. Most data APIs only allow you to /GET. Allowing for the other verbs /POST, /PUT, and /DELETE, usually require not just more resources to deploy and manage, but also a certain mindset that is open to receiving information from your API consumers, which could range from internal and partner users, to the general public. Some places I’ve worked, are just scared shitless of repercussions of doing something like this.

Which brings me to my idea for a new API service. Let’s call it **BeyondGET** or **OtherVerbs**. A service that would allow people to add API resources they’d like to augment with the ability to POST, PUT and GET. So I could add an entry for Crunchbase using api.crunchbase.com/v/1/company/. I would define each entry with a Swagger definition, and the system would create a basic data store for the entry. You could now submit changes to existing records, as well as entirely new records or mark a record for deletion--providing an augmented, external, crowdsourced layer on top of potentially distributed API resources.

Developers could use a primary API resource as well as the augmented version of the API if they choose. You would have to add some sort of trusted user layer, so developers could only show data submitted by trusted sources.  Seems like some sort of Git layer for versioning would be needed as well.

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/augmented-delete.png" alt="" width="330" align="right" />

API owners could also choose to use an augmented layer as a sort of crowdsource queue for their API. The API owner could decide which users they trust and what data was relevant enough to let back in. It could act as a DMZ for your API.

There would also need to be a data licensing layer to all of this, that if well crafted, could open up the potential for revenue sharing or at least virtual credits to use against other API services. I know CityGrid was discussing how they could reward API consumers for their contributions, and I could see this being a way to deliver on that across the API space.

Anyways, I’d love to hear thoughts on this. Or run with building a version of it yourself. It would be awesome to see a whole breed of augmented API service providers pop up, allowing me to add a new section about it at API Evangelist. :)

   [1]: https://twitter.com/audreywatters
   [2]: /2013/03/16/using-the-crunchbase-api/
