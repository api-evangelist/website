---
published: true
layout: post
title: 'The Data Agency Registry'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/copper-circuit-capital_36728420065_o.jpg
tags:
 - Lifecycle
 - OpenAPI
---


I have had a side project going with [Pascal Heus](https://www.linkedin.com/in/pascal/?originalSubdomain=ca) , my partner in data crime over at [Metadata Technology North America (MTNA) for a a few months now called the ](https://www.mtna.us/)[Data Agency Registry](https://github.com/integrateddatasvc/agency-registry). It is an Jekyll and Github powered open data registry of government agencies, data archives, research centers, and other organizations producing and publishing statistical and scientific data. I talked Pascal into learning about Jekyll (painful), and he’s been data from a variety of sources there as YAML and JSON, and I am working on a public API workspace, some RSS feed automation, and other work on the project. But we don’t want to wait until we have everything done before we just put out there and see what others have to say about the data, which you can tune into on the Jekyll and Github Pages powered website, or via the Github README with the following areas:


    
- [**Progress**](https://github.com/integrateddatasvc/agency-registry#progress) - Providing details of the progress we have made.
    
- [**Road Map**](https://github.com/integrateddatasvc/agency-registry#roadmap) - Sharing what the future holds using the road map.
    
- [**Contribute**](https://github.com/integrateddatasvc/agency-registry#how-to-contribute) - Instructions for when you want to contribute.
    
- [**Edit the Content**](https://github.com/integrateddatasvc/agency-registry#how-to-contribute) - Details when you want to edit data.
    
- [**Generate the Content**](https://github.com/integrateddatasvc/agency-registry#how-to-contribute)
    
- [**Identifiers and Basic Information**](https://github.com/integrateddatasvc/agency-registry#identifiers-and-basic-information) - Details on how Pascal has structured the data.
    
- [**Workspace**](ttps://api-evangelist.postman.co/workspace/Agency-Registry~5faa4717-763b-4bd0-9e16-94272b2313af/overview) - A Postman public API workskpace where we'll be automating the project.
    
- [**Sponsors**](https://github.com/integrateddatasvc/agency-registry#sponsors) - Some love for everyone who is helping out.


We chose this approach to building the registry so that anyone could fork the project and use, or contribute back. The goal is to provide a single machine and human readable place to find the best data and APIs across not just government, but also NGOs, Universities, and other places where research is going on. Pascal is working hard on evolving the data in the registry, while I am working on making the data more useful by integrating with, orchestrating, and automating around the data in the following ways:


    
- [**Agency Directory Feeds**](https://github.com/integrateddatasvc/agency-registry/tree/main/feeds/agencies) - I am publishing static feeds from the agency data, making it available via simple URLs, applying the business logic using Liquid within the Jekyll framework, but published as JSON.
    
- **Agency RSS Feeds** - I am publishing a feed for all of the RSS feeds across the agencies, providing a single URL where you can pull all the news and blog RSS from across the agencies, for use in automation.
    
- **Agency APIs** - I am publishing a list of APIs from my recent inventory of US federal government agencies, augmenting the valuable data Pascal has published with API URLs and public API workspaces for agencies.


Once I have the agency feeds, agency RSS and Atom feeds published, and the updated list of federal agency APIs I will see if I can as many of the APIs represented as OpenAPI and collections. Some agencies have Swagger and OpenAPI, or even Postman collections, but most will have to be scraped or reverse engineered using a proxy while playing the API in Postman. It is time consuming but totally worth it to have the functional collection that you can use to manually make calls to each government API, as well as automate with monitors or as part of CI/CD pipelines.


I like Pascal’s approach to the data and super happy to have him defining how the data is structured, and stored, and I will just build on top of that with Jekyll, Github, and Postman workspaces and collections. [The Agency data Registry website](https://integrateddatasvc.github.io/agency-registry/) is in very early stages, so there is a lot of work to be done, but we wanted to put it out there early on so we can [gather feedback from other folks](https://github.com/integrateddatasvc/agency-registry/issues). If there are other types of data you’d like to see represented in the Agency Data Registry, or would like to roll up your sleeves and help improve on the data that is there, let us know. You can engage with the project via [the Github repository](https://github.com/integrateddatasvc/agency-registry) or the [Postman public API workspace](https://api-evangelist.postman.co/workspace/Agency-Registry~5faa4717-763b-4bd0-9e16-94272b2313af/overview)-—there is lots of work to be done, so would love to have your input and help.