---
published: true
layout: post
title: Synthetic Healthcare Records For Your API Using Synthea
date: 2018-05-01T09:00:00.000Z
tags:
  - API Evangelist
  - Virtualization
  - Data
  - Sandbox
  - Federal Government
image: 'https://s3.amazonaws.com/kinlane-productions/synthea/synthea-patient-data.png'
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I have been working on several fronts to help with API efforts at the Department of Veterans Affairs (VA) this year, and one of them is helping quantify the deployment of a lab API environment for the platform. The VA doesn't want it called it a sandbox, so they are calling it a lab, but the idea is to provide an environment where developers can work with APIs, see data just like they would in a live environment, but not actually have access to live patient data before they can prove their applications are reviewed and meet requirements.

One of the projects being used to help deliver data within this environment is called [Synthea](https://synthetichealth.github.io/synthea/). Providing the virtualized data will be made available through VA labs API--here is the description of what they do from their website:

> Synthea is an open-source, synthetic patient generator that models the medical history of synthetic patients. Our mission is to provide high-quality, synthetic, realistic but not real, patient data and associated health records covering every aspect of healthcare. The resulting data is free from cost, privacy, and security restrictions, enabling research with Health IT data that is otherwise legally or practically unavailable.

Synthea data contains a complete medical history, including medications, allergies, medical encounters, and social determinants of health, providing data can be used without concern for legal or privacy restrictions by developers to support a variety of data standards, including HL7 FHIR, C-CDA and CSV. Perfect work loading up into sandbox and lab API environments, allowing to developers to safely play around with building healthcare applications, without actually touching production patient data.

I've been looking for solutions like this for other industries. [Synthea even has a patient data generator available on Github](https://github.com/synthetichealth/synthea), which is something I'd love to see for every industry. Sandbox and labs environment should be default for any API, especially APIs operating within heavily regulated industries. I think Synthea provides a pretty compelling model for the virtualization of API data, and I will be referencing it as part of my work in hopes of incentivizing someone to fork it and use to provide something we can use as part of any API implementation.
