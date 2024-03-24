---
published: true
layout: post
title: 'An Operational Fingerprint for a Public API'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/eugenics-gears-pipes-plumbing.jpg
author:
    name: kinlane
tags:
- APIs.json
- Discovery
- Crawler
- Fingerprint
- Profiling
---
I am pretty happy with [manually searching Google and Bing for APIs](https://explore.apis.io/tags/) across different spaces. The more APIs I add to my APIs.json index of APIs, the more words that appear as tags. So I regularly scroll through the list clicking on different keywords to see what comes up in the top 10 search results. I will be manually doing this on a regular basis, but I am looking to see what I can automate as well, so I wanted to see what the first couple of steps I could take to automate this recurring activity.

I tend to write scripts that mimic individual actions I take so I wanted to recreate myself by clicking on Google and Bing to search for an API. Google doesn’t provide a search API, but Big does. So I signed up for their API, and integrated it with the [vocabulary I am using to power my APIs.json work](https://github.com/apis-json/artisanal/blob/main/vocabulary.yml), saving each individual search results entry as an APIs.json, for further evaluation and fleshing out to see if there is an interesting API there. A lot of what gets returned will be Wikipedia, blog, and other noise about APIs-—but I am looking for the API signal. So, how do you mimic what my eye does as soon as I land on any web page from a Bing search? 

It turns out that APIs.json can be used as the fingerprint to potentially tell whether or not a URL I visit is potentially an API provider, let alone one that I would want to further profile and include in my APIs.json work. Meaning, all of the properties you can index with an APIs.json are how you tell If a website is a public API provider. I simply take the URL returned to me from my Bing search, parse all of the anchor properties from a page and compare the label for each link against my API property vocabulary to see if the link is documentation, plans, pricing, SDKs, and other common properties of public API operations. I give a variety of points to each property, giving 25 points for documentation, and 5 for terms of service. I can now automate the searching for new APIs using the Bing Search API, parse the content of the page, and rate the potential of there being an actual API there, or just a story about an API.

We’ll see how well my new API crawler works. I am sure I will have to refine the vocabulary used, as well as how I score. I notice it is finding duplicates and applying multiple points, but that is fine. It allowed me to automate two steps of my manual process, but I am skeptical it replaces my eye for what is an API and what is not an API, as well as what you profile using APIs.json. However, it was a fun exercise and we’ll see what I yield. I will leave it running for a week using the 500 or so words I have in my vocabulary. In the meantime I”ll be manually searching for interesting APIs and continuing to profile them and add them to [my APIs.json Artisanal work](https://github.com/apis-json/artisanal). I will be testing out each bit of work I do as part of this project to see where I can automate, but ultimately I will be pretty choosy about what I do actually automate because I am pretty particular about what the results are. We will see. Regardless, it is fun to explore.