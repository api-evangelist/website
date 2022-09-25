---
published: true
layout: post
title: The Banking API Actors In The UK
date: 2018-02-26T09:00:00.000Z
tags:
  - API Evangelist
  - Banking
  - Ecosystem
image: 'https://s3.amazonaws.com/kinlane-productions/shakespeare/shakespeare.jpg'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/shakespeare/shakespeare.jpg" align="right" width="45%" style="padding: 15px;" /></p>I've been profiling [the work of the Open Banking Implementation Entity when nit comes to banking API standards in the UK](https://www.openbanking.org.uk/). As part of my getting up to speed on the banking ecosystem in the UK, and Europe, I've been posting a series of small blog posts, outlining different aspects of how things work, and who the players are. While going through the Open Banking documentation, I came across a great list of the "actors" int he Open Banking API ecosystem, which taught me a lot about who is involved, and was worth reposting here as a list.

The Open Banking eco-system consists of a number of actors, which may be a natural person or an entity:

- **Payment Service User (PSU)** - Person - Payment Services User is a natural or legal person making use of a payment service as a payee, payer or both
- **Payment Service Provider (PSP)** - Legal Entity - A legal entity (and some natural persons) that provide payment services as defined by PSD2 Article 4(11)
- **Account Servicing Payment Service Provider (ASPSP)** - Legal Entity - Account Servicing Payment Service Providers provide and maintain a payment account for a payer as defined by the PSRs and, in the context of the Open Banking Ecosystem are entities that publish Read/Write APIs to permit, with customer consent, payments initiated by third party providers and/or make their customers’ account transaction data available to third party providers via their API end points.
- **Third Party Providers / Trusted Third Parties (TPP)** - Legal Entity - Third Party Providers are organisations or natural persons that use APIs developed to Standards to access customer’s accounts, in order to provide account information services and/or to initiate payments. Third Party Providers are either/both Payment Initiation Service Providers (PISPs) and/or Account Information Service Providers (AISPs).
- **Payment Initiation Service Provider (PISP)** - Legal Entity - A Payment Initiation Services Provider provides an online service to initiate a payment order at the request of the payment service user with respect to a payment account held at another payment service provider.
- **Account Information Service Provider (AISP)** - Legal Entity - An Account Information Service provides account information services as an online service to provide consolidated information on one or more payment accounts held by a payment service user with one or more payment service provider(s).
- **TPP Primary Technical Contact (TPP-PTC)** - Person - A Primary Technical Contact is an individual nominated by a TPP to have access to the Directory and will be able to nominate other Directory technical users. This should be a main point of contact on technical configuration and a senior member of staff with responsibility for the management of the Open Banking digital identity.
- **TPP Secondory Technical Contact (TPP-STC)** - Person - A person that carries out technical operations on behalf of a TPP. A TPP-STC has the same permissions as a TPP-PTC except for the ability to nominate other Directory technical users.
- **ASPSP Primary Technical Contact (ASPSP-PTC)** - Person - A Primary Technical Contact is an individual nominated by the ASPSP to have access to the Directory and will be able to nominate other Directory technical users. This should be a main point of contact on technical configuration and a senior member of staff with responsibility for the management of the Open Banking digital identity.
- **ASPSP Secondory Technical Contact (ASPSP-STC)** - Person - A person that carries out technical operations on behalf of an ASPSP. An ASPSP-STC has the same permissions as a ASPSP-PTC except for the ability to nominate other Directory technical users.
- **Regulatory Bodies** - Legal Entity - Government or industry bodies that have a regulatory role in the payments industry. This includes, but is not limited to, the UK Competition & Markets Authority (CMA), HM Treasury (HMT), EBA, etc.	No
- **Member State Competent Authorities (MSCA)** - Legal Entity - Regulatory Body	The regulatory body (or bodies) in each of the EU member states that is responsible for maintaining a register of payment institutions.
- **Financial Conduct Authority (FCA)** - Legal Entity - The Financial Conduct Authority is the competent authority for the UK	No
- **Open Banking Limited (OB)** - Legal Entity - The Open Banking Implementation Entity is the delivery organization working with the CMA9 and other stakeholders to define and develop the required APIs, security and messaging standards that underpin Open Banking.
- **OB Directory Administrator** - Person - A person working for OB that is responsible for executing various technical processes related to the Directory on behalf of OB.

I wish I could find breakdowns of the actors within every industry I work in like this. I've been studying up on how the banking industry works, but my knowledge moved forward quite a bit after studying this. It is the best explanation of the acronyms I've been coming across lately, and is the best breakdown of everyone involved in an API ecosystem I have ever come across in my eight years of studying the space.

Open Banking is doing some really interesting work on the banking API front. This is just one of many artifacts I'm coming across that demonstrate they really have their act together when it comes to developing banking API specifications in the UK.
