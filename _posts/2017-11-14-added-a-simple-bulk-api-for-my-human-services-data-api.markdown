---
published: true
layout: post
title: I Added A Simple Bulk API For My Human Services Data API
date: 2017-11-14T09:00:00.000Z
tags:
  - API Evangelist
  - HSDA
  - Bulk
  - City Government
image: >-
  https://s3.amazonaws.com/kinlane-productions/open-referral/human-services-data-bulk-api.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/open-referral/human-services-data-bulk-api.png" align="right" width="45%" style="padding: 15px;" /></p>The core Human Services Data API allows for adding of organizations, locations, services, and contacts one by one using a single POST on the core API paths for each available resource. However, if you want to add thousands, or even hundreds of records, it can quickly become cumbersome to submit each of the calls, so I wanted to introduce a simple Human Services Bulk API for helping handle the adding of large quantity of data, on a one-time, or recurring basis. I know there job queuing solutions available out there, but my goal with this project is to focus on the API definition, as well as the backend system(s). For this round, I just want to get a simple baseline definition in place, with a simple API backend for orchestrating. I'll update to support AWS, and other queuing solutions as part of the road-map--further hammering out a consistent [HSDA Bulk API](http://developer.open.referral.adopta.agency/#HSDA Bulk).

The first dimension of this new HSDA Bulk API focuses on providing paths for POSTing large quantities of data across the core human service resources:

- organizations/ - POST complete organizations JSON records as array.
- locations/ - POST complete locations JSON records as array.
- services/ - POST complete services JSON records as array.
- contacts/ - POST complete contacts JSON records as array.

You can submit as many records to each of these paths (well, within reason), including the sub-resources for each object like physical address, phones, etc. When POSTed each record doesn't immediately go into the main HSDA database. Each entry is entered into a jobs system, which can be run on a schedule, based upon events, or maybe just wait until the middle of the night. The goal is to offload the bulk insert to a job system, which can spread things out over time, and minimize negative impact on resources strapped human services database. HSDA Bulk API runs as a separate microservice which can be run side by side with the core HSDA implementation, or possibly scaled on separate infrastructure to allow for handling of expected loads.

The next dimension of this new HSDA Bulk API allows for importing of [HSDS datapackage.json files](https://openreferral.readthedocs.io/en/latest/hsds/reference/), bringing things back to basics with the Human Services Data Specification(HSDS). [The JSON file contains a list of paths to individual HSDS CSV files](https://s3.amazonaws.com/kinlane-productions/open-referral/sample-datapackage/datapackage.json), which are then processed as individual resources, with each record inserted as a job, for running on schedule, event, or other approach. Adding a more comprehensive approach to loading up large datasets into any human services system using an HSDA API, while also continuing to smooth out the impact of the core system using jobs.

With both of these dimension, you can perform bulk uploads of data using the individual organizations, locations, services, and contacts page, as well as a complete datapackage.json file. Next I will be hammering on the demo API I have a bunch more, to harden the code, and see if I'm missing any details. After that I'll started looking at switching out the custom backend I have with an AWS API Gateway managed, and possibly AWS SQS or other jobs solution. I'm trying to keep [the HSDA Bulk API definition](https://github.com/human-services/portal/blob/master/_data/api-commons/openapi-hsda-bulk.yaml) simple, but also allow for scaling up with other more robust backend system. For now, I'd call this edition of [the HSDA Bulk API](http://developer.open.referral.adopta.agency/#HSDA Bulk) to be a decent v1.0 start for this new HDSA microservice.
