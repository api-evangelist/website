---
published: true
layout: post
title: 'The Banking API Actors In The UK'
image: https://s3.amazonaws.com/kinlane-productions2/shakespeare/shakespeare.jpg
---

<p><img src="https://s3.amazonaws.com/kinlane-productions2/shakespeare/shakespeare.jpg" align="right" width="45%" style="padding: 15px;" />
<p>I’ve been profiling <a href="https://www.openbanking.org.uk/">the work of the Open Banking Implementation Entity when nit comes to banking API standards in the UK</a>. As part of my getting up to speed on the banking ecosystem in the UK, and Europe, I’ve been posting a series of small blog posts, outlining different aspects of how things work, and who the players are. While going through the Open Banking documentation, I came across a great list of the “actors” int he Open Banking API ecosystem, which taught me a lot about who is involved, and was worth reposting here as a list.

<p>The Open Banking eco-system consists of a number of actors, which may be a natural person or an entity:

<ul>
  <li><strong>Payment Service User (PSU)</strong> - Person - Payment Services User is a natural or legal person making use of a payment service as a payee, payer or both</li>
  <li><strong>Payment Service Provider (PSP)</strong> - Legal Entity - A legal entity (and some natural persons) that provide payment services as defined by PSD2 Article 4(11)</li>
  <li><strong>Account Servicing Payment Service Provider (ASPSP)</strong> - Legal Entity - Account Servicing Payment Service Providers provide and maintain a payment account for a payer as defined by the PSRs and, in the context of the Open Banking Ecosystem are entities that publish Read/Write APIs to permit, with customer consent, payments initiated by third party providers and/or make their customers’ account transaction data available to third party providers via their API end points.</li>
  <li><strong>Third Party Providers / Trusted Third Parties (TPP)</strong> - Legal Entity - Third Party Providers are organisations or natural persons that use APIs developed to Standards to access customer’s accounts, in order to provide account information services and/or to initiate payments. Third Party Providers are either/both Payment Initiation Service Providers (PISPs) and/or Account Information Service Providers (AISPs).</li>
  <li><strong>Payment Initiation Service Provider (PISP)</strong> - Legal Entity - A Payment Initiation Services Provider provides an online service to initiate a payment order at the request of the payment service user with respect to a payment account held at another payment service provider.</li>
  <li><strong>Account Information Service Provider (AISP)</strong> - Legal Entity - An Account Information Service provides account information services as an online service to provide consolidated information on one or more payment accounts held by a payment service user with one or more payment service provider(s).</li>
  <li><strong>TPP Primary Technical Contact (TPP-PTC)</strong> - Person - A Primary Technical Contact is an individual nominated by a TPP to have access to the Directory and will be able to nominate other Directory technical users. This should be a main point of contact on technical configuration and a senior member of staff with responsibility for the management of the Open Banking digital identity.</li>
  <li><strong>TPP Secondory Technical Contact (TPP-STC)</strong> - Person - A person that carries out technical operations on behalf of a TPP. A TPP-STC has the same permissions as a TPP-PTC except for the ability to nominate other Directory technical users.</li>
  <li><strong>ASPSP Primary Technical Contact (ASPSP-PTC)</strong> - Person - A Primary Technical Contact is an individual nominated by the ASPSP to have access to the Directory and will be able to nominate other Directory technical users. This should be a main point of contact on technical configuration and a senior member of staff with responsibility for the management of the Open Banking digital identity.</li>
  <li><strong>ASPSP Secondory Technical Contact (ASPSP-STC)</strong> - Person - A person that carries out technical operations on behalf of an ASPSP. An ASPSP-STC has the same permissions as a ASPSP-PTC except for the ability to nominate other Directory technical users.</li>
  <li><strong>Regulatory Bodies</strong> - Legal Entity - Government or industry bodies that have a regulatory role in the payments industry. This includes, but is not limited to, the UK Competition &amp; Markets Authority (CMA), HM Treasury (HMT), EBA, etc.	No</li>
  <li><strong>Member State Competent Authorities (MSCA)</strong> - Legal Entity - Regulatory Body	The regulatory body (or bodies) in each of the EU member states that is responsible for maintaining a register of payment institutions.</li>
  <li><strong>Financial Conduct Authority (FCA)</strong> - Legal Entity - The Financial Conduct Authority is the competent authority for the UK	No</li>
  <li><strong>Open Banking Limited (OB)</strong> - Legal Entity - The Open Banking Implementation Entity is the delivery organization working with the CMA9 and other stakeholders to define and develop the required APIs, security and messaging standards that underpin Open Banking.</li>
  <li><strong>OB Directory Administrator</strong> - Person - A person working for OB that is responsible for executing various technical processes related to the Directory on behalf of OB.</li>
</ul>

<p>I wish I could find breakdowns of the actors within every industry I work in like this. I’ve been studying up on how the banking industry works, but my knowledge moved forward quite a bit after studying this. It is the best explanation of the acronyms I’ve been coming across lately, and is the best breakdown of everyone involved in an API ecosystem I have ever come across in my eight years of studying the space.

<p>Open Banking is doing some really interesting work on the banking API front. This is just one of many artifacts I’m coming across that demonstrate they really have their act together when it comes to developing banking API specifications in the UK.


