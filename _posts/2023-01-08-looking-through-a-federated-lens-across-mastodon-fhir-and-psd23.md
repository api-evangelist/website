---
published: true
layout: post
title: 'Looking Through a Federated Lens Across Mastodon, FHIR, and PSD2/3'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/bf-skinner-docs-cranes-waterfront.jpg
author:
 name: kinlane
tags:
- Mastodon
- Social
- Federated
- FHIR
- PSD2
---
I am immersed in the federated Mastodon universe the last month, and I’ve been immersed in the federated universes of [FHIR](https://www.hl7.org/fhir/overview.html), [PSD2/PSD3](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=celex%3A32015L2366), and [UK Open Banking](https://www.openbanking.org.uk/) for a number of years. It is unlikely that anyone involved in the Mastodon universe right now would consider what is happening could be related to the financial and healthcare sectors, but those in the financial and healthcare space would also not see the expansion of the Mastodon universe as having anything to do with their worlds. Mastodon is about social networking, but PSD2 is about banking, and FHIR about healthcare, while all three are about defining one dimension of our personal and professional lives that is being shaped by open source federated APIs.

Let’s recap what each of these federated approaches to solving real world problems using federated Apis:

- **Mastodon**  - An open source API developed to support a federated approach to social networks, looking to replace Twitter, and potentially other social networks with a distributed version that would leverage protocols to rival the hold platforms have on our digital social networks. 
- **FHIR** - An open source API developed by the US federal government to standardize the exchange of electronic health care data, providing a data model, and standard set of Apis that healthcare providers can implement to deliver applications and integrations.
- **PSD2/PSD3** - An open source API mandated by the European Commission, mandating a single payer market in Europe using a common API definition that all banks in Europe will be using to deliver applications and make people’s payments available to aggregators and other stakeholders.
- **UK Bankin**g - Emulating, but going further than PSD2, the UK has implemented their own banking APIs, leveling the playing field for banks in the UK by mandating that they all use the same set of public and private APIs for making peoples data available to applications, integrations, and aggregators.

I have public workspaces setup for [Mastodon](https://www.postman.com/api-evangelist/workspace/mastodon/overview), [FHIR](https://www.postman.com/api-evangelist/workspace/fast-healthcare-interoperability-resources-fhir/overview), [PSD2/3](https://www.postman.com/api-evangelist/workspace/payment-service-directive-psd2/overview), and [UK banking](https://www.postman.com/api-evangelist/workspace/uk-public-banking/overview), publishing OpenAPI definitions and collections for each API standard, with as many environments as I can for each instance of the API. I have a lot more work to do on FHIR and PSD2, but Mastodon and UK Banking workspaces are excellent examples of how federated APIs can applied to any industry. One common API definition, with collection generated for making calls to APIs, and environments to abstract away the base URL and other data needed to work with each API.

There are other federated examples of APIs designed to serve a specific industry. These are just four federated APIs that are top of mind for me, ad represent industries that are top of mind for many other people right now. This moment provides an opportunity for us to learn about the potential of federated APIs as well as some of the challenges. Financial and healthcare people stand to learn a lot from what is happening in the Mastodon universe right now, which is why I am taking this opportunity to tell some stories. As I learn and document the federated lessons happening in the Mastodon universe I am going to take the moment to look through the federated lens of FHIR and PSD2/3 movements. I am guessing we are all going to learn a lot in coming years.
