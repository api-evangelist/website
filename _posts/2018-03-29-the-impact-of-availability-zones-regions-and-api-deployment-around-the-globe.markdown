---
published: true
layout: post
title: 'The Impact Of Availability Zones, Regions, And API Deployment Around The Globe'
date: 2018-03-29T09:00:00.000Z
tags:
  - API Evangelist
  - Regions
  - Cloud
  - Performance
  - Reliability
  - Politics of APIs
image: 'https://s3.amazonaws.com/kinlane-productions/azure/azure-regions-map.png'
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>[Werner Vogels shared a great story looking back at 10 years of compartmentalization at AWS](https://www.allthingsdistributed.com/2018/03/ten-years-of-aws-compartimentalization.html), where he talks about the impact Amazon has made on the landscape by allowing for the deployment of resources into different cloud regions, zones, and jurisdictions. I agree with him regarding the significant impact this has had on how we deliver infrastructure, and honestly isn't something that gets as much recognition and discussion as it should. I think this is partly due to the fact that many companies, organizations, institutions, and governments are still making their way to the cloud, and aren't far enough in their journeys to be able to sufficiently take advantage of the different availability zones.

In Werner's piece he focuses on the availability, scalability, and redundancy benefits of operating in different zones. Which I think gets at the technical benefits of this benefit of operating infrastructure in the cloud, but there are also significant business, and even political considerations at play here. As the web matures, the business and political implications of being able to operate precisely within a specific region, zone, and jurisdiction is becoming increasingly important. Sure, you want your API infrastructure to be reliable, redundant, and failover when there has been an outage in a specific region, but increasingly clients are asking for APIs to be delivered close to where business occurs, and regulatory bodies are beginning to mandate that digital business gets done within specific borders as well.

Regions have become a top level priority for [Amazon](https://aws.amazon.com/about-aws/global-infrastructure/), [Azure](https://azure.microsoft.com/en-us/global-infrastructure/regions/), and [Google](https://cloud.google.com/about/locations/). Clearly, they are also becoming a top level priority for their customers who operate within their clouds. It is one of those things I notice evolving across the technology landscape and have felt the need to pay attention to more as I see more activity and chatter. I've begun documenting which regions each of the cloud providers are operating in, and have been increasing the number of stories I'm writing about the potential for API providers, as well as API service providers. So it was good to see Werner reflecting on the significant role regions have played in the evolution of the cloud, and backing up what I'm already feeling and seeing across the sector.

While Werner focused on the technical benefits, I think the political, legal, and regulatory benefits will soon dwarf the technical ones. While the web has enjoyed a borderless existence for the last 25 years, I think we are going to start seeing things change in the next decade. Making cloud regions more about maintaining control over your countries digital assets, how you generate tax revenue, and defend the critical digital infrastructure of your nation from your enemies. The cloud providers who are empowering companies, organizations, institutions, and government agencies to securely, but flexibly operate in multiple regions are going to be in a good position. Similarly, the API providers, and service providers who behave in a similar way, delivering API resources in a multi-cloud way, are going to emerge as the strongest players in the API economy.
