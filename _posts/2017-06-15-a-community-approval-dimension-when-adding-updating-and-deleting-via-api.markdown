---
title: A Community Approval Dimension When Adding, Updating, And Deleting Via API
date: 2017-06-15 11:00:00 Z
tags:
- Design
- API Evangelist
- Governance
- Community
image: https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-community-join.png
---

<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-community-join.png" align="right" width="30%" style="padding: 15px;" /></p>One of the projects I'm working on as part my [Human Services API](https://openreferral.github.io/api-specification/definition/) work is trying to define the layer that allows developers to add, update, and delete data via the API. We ultimately want to empower 3rd party developers, and external stakeholders to help curate and maintain critical human services data within a community, through trusted partners.

The Human Services API allows for the reading and writing of organizations, locations, and services for any given area. I am looking to provide guidance on how API implementors can allow for POST, PUT, PATCH, and DELETE on their API, but require approval before any changing transaction is actually executed. Requiring the approval of an internal system administrator to ultimately give the thumbs up or thumbs down regarding whether or not the change will actually occur.

A process which immediately begs for the ability to have multiple administrators or even possibly involving external actors. How can we allow organizations to have a vote in approving changes to their data? How can multiple data stewards be notified of a change, and given the ability to approve or disprove, logging every step along the way? Allowing any change to be approved, reviewed, audited, and even rolled back. Making public data management a community affair, with observability and transparency built in by default.

I am doing research into different approaches to tackling this, ranging from community approaches like Wikipedia, to publish and subscribe, and other events or webhook models. I am looking for technological solutions to opening up approval to the API request and response structure, with accompanying API and webhook surface area for managing all aspects of the approval of any API changes. If you know of any interesting solutions to this problem I'd love to hear more, so that I can include in my research, future storytelling, and ultimately the specification for [the Open Referral Human Services Data Specification and API](https://openreferral.org/).