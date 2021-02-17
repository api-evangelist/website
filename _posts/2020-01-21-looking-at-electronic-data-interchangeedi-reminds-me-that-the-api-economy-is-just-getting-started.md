---
published: true
layout: post
title: 'Looking at Electronic Data Interchange (EDI) Reminds Me that the API Economy is Just Getting Started'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/scream-IMG_8494.jpg
---
<p><img style="padding: 15px;" src="https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/scream-IMG_8494.jpg" alt="" width="40%" align="right" /></p>
<p class="p1">I am neck deep <a href="http://apievangelist.com/2020/01/21/expanding-my-api-toolbox-for-the-next-decade/">in the expansion of what I consider to be my API toolbox</a>, and I have been spending time mapping out the world of EDI. If you aren&rsquo;t familiar with&nbsp; <a href="https://en.wikipedia.org/wiki/Electronic_data_interchange">the Electronic Data Interchange&nbsp;(EDI)</a>, it &ldquo;is the electronic interchange of business information using a standardized format; a process which allows one company to send information to another company electronically rather than with paper. Business entities conducting business electronically are called trading partners.&rdquo;&nbsp; EDI is the original API by providing a, &ldquo;technical basis for automated commercial "conversations" between two entities, either internal or external. The term EDI encompasses the entire electronic data interchange process, including the transmission, message flow, document format, and software used to interpret the documents&rdquo;. EDI is everywhere, and truly the backbone of the global supply chain, but one that you only hear lightly about as part of the overall API conversation.</p>
<p class="p1">I have regularly come across the overlap between EDI and API over the last 10 years of doing API Evangelist, and while I have engaged in discussion around modernizing legacy EDI approaches in healthcare and commerce, most other fundamental building blocks of the global supply chain are entirely new to me. Revealing how little I know about the bigger picture of EDI, and how small my API world actually is. I don&rsquo;t claim to know everything about information exchange and interoperability, but EDI is something that should be a bigger part of my storytelling, and the fact that it isn&rsquo;t I think is revealing about how much more work we actually have in front of us when it comes to delivering on the promise of the API economy.<span>&nbsp;</span></p>
<p class="p1">Take a look at some of the major EDI standards to get a sampling of the scope I am talking about. These are the electronic data interchange standards that have governed commerce before the Internet was around, and continues to define how data moves around.</p>
<ol>
<li><strong><a href="https://www.edigas.org/">Edig@s (EDIGAS)</a></strong> - The Edig@s Workgroup decided to implement EDI messages to: Reduce the number of different messages currently used; Achieve a more efficient and more flexible way of handling the dispatching activities; Allow a faster reaction to a changed working environment. The EDI standard selected for those messages is the UN/EDIFACT standard and starting from Edig@s version 4 we introduced the XML standard.</li>
<li><strong><a href="https://en.wikipedia.org/wiki/GS1_EDI">GS1 EDI</a></strong> - GS1 EDI is a set of global electronic messaging standards for business documents used in Electronic Data Interchange (EDI). The standards are developed and maintained by GS1. GS1 EDI is part of the overall GS1 system, fully integrated with other GS1 standards, increasing the speed and accuracy of the supply chain. Examples of GS1 EDI standards include messages such as: Order, Despatch Advice (Shipping Notice), Invoice, Transport Instruction, etc.</li>
<li><strong><a href="https://en.wikipedia.org/wiki/Health_Insurance_Portability_and_Accountability_Act">HIPAA</a></strong> - The Health Insurance Portability and Accountability Act of 1996 was enacted by the 104th United States Congress and signed by President Bill Clinton in 1996. It was created primarily to modernize the flow of healthcare information, stipulate how Personally Identifiable Information maintained by the healthcare and healthcare insurance industries should be protected from fraud and theft, and address limitations on healthcare insurance coverage</li>
<li><strong><a href="https://www.hl7.org/">Hl7</a></strong> - Health Level Seven International (HL7) is a not-for-profit, ANSI-accredited standards developing organization dedicated to providing a comprehensive framework and related standards for the exchange, integration, sharing and retrieval of electronic health information that supports clinical practice and the management, delivery and evaluation of health services.</li>
<li><strong><a href="https://www.iata.org/en/publications/store/cargo-interchange-message-procedures--cargo-imp-/">IATA Cargo-IMP</a></strong> - Cargo data exchange automation between airlines and other parties works much more efficiently if messaging procedures and standards are applied. IATA's Cargo-IMP is the legacy standard for exchanging critical cargo operations information.</li>
<li><strong><a href="https://www.odette.org/">Odette</a></strong>- Odette is a pan-European collaboration and services platform working for the entire automotive network. We bring together supply chain professionals and technology experts to create standards, develop best practice and provide services which support logistics management, e-business communications and engineering data exchange throughout the world.<span>&nbsp;</span></li>
<li><strong><a href="https://en.wikipedia.org/wiki/SCRIPT_(medicine)">SCRIPT</a></strong> - SCRIPT is a standard promulgated by the National Council for Prescription Drug Programs (NCPDP) for the electronically transmitted medical prescriptions in the United States.</li>
<li><strong><a href="https://en.wikipedia.org/wiki/SWIFT_message_types">Swift</a></strong> - The Society of Worldwide Interbank Financial Telecommunication was formed in 1973 and is headquartered in Brussels. SWIFT operates a worldwide financial messaging network which exchanges messages between banks and financial institutions. SWIFT also markets software and services to financial institutions, much of it for use on the SWIFTNet Network.</li>
<li><strong><a href="https://en.wikipedia.org/wiki/TRADACOMS">TRADACOMS</a></strong> -<span>&nbsp; </span>Tradacoms is an early standard for EDI primarily used in the UK retail sector. It was introduced in 1982 as an implementation of the UN/GTDI syntax, one of the precursors of EDIFACT, and was maintained and extended by the UK Article Numbering Association.</li>
<li><strong><a href="https://en.wikipedia.org/wiki/EDIFACT">UN/EDIFACT</a></strong> - An international EDI standard developed under the United Nations, providing a set of syntax rules to structure data, an interactive exchange protocol (I-EDI), and standard messages which allow multi-country and multi-industry exchange.</li>
<li><strong><a href="https://en.wikipedia.org/wiki/ASC_X12">X12 Electronic data interchange (EDI)</a></strong> - The X12 Electronic data interchange (EDI) and Context Inspired Component Architecture (CICA) standards along with XML schemas which drive business processes globally. The membership of ASC X12 includes technologists and business process experts, encompassing health care, insurance, transportation, finance, government, supply chain and other industries.</li>
</ol>
<p class="p1">EDI is API. These standards employ FTP, SFTP, FTPS, Email, HTTP, AS1, AS2, and AS4 to move data around. If SOAP is the father of API, then EDI is the grandfather. Each of these standards provide the technical details of the exchange of data, and providers can use any of these protocols to move the data around between providers. Going beyond the standards themselves, you can look at some of the EDI efforts out of enterprise and federal government agencies who set the tone for how markets work each day.</p>
<ul>
<li><strong>Commerce</strong> 
<ul>
<li><a href="https://corporate.walmart.com/suppliers/merchandise-support-center">Walmart</a></li>
<li><a href="https://developer.amazonservices.com/index.html">Amazon</a></li>
</ul>
</li>
<li><strong>Automotive</strong> 
<ul>
<li><a href="https://www.gsec.ford.com/Hub">Ford</a></li>
<li><a href="https://www.vwgroupsupply.com/one-kbp-pub/en/kbp_public/information/electronic_data_interchange/electronic_data_interchange.html">Volkswagen</a></li>
</ul>
</li>
<li><strong>Healthcare</strong> 
<ul>
<li><a href="https://www.gsec.ford.com/Hub">Centers for Medicare &amp; Medicaid Services</a></li>
<li><a href="https://www.cigna.com/health-care-providers/coverage-and-claims/submit-claims/electronic-data-interchange-vendors">Cigna</a></li>
</ul>
</li>
<li><strong>Government</strong> 
<ul>
<li><a href="https://dodprocurementtoolbox.com/site-pages/ebusiness-data-standards-edi">Deparment of Defense</a></li>
<li><a href="https://www.eda.gov/edi/">Department of Commerce</a></li>
</ul>
</li>
<li><strong>Aerospace</strong> 
<ul>
<li><a href="http://www.boeingsuppliers.com/edi/PCOS_EDI_guidelines.pdf">Boeing</a></li>
<li><span class="s1"><a href="https://www.airbus.com/be-an-airbus-supplier.html">Airbus</a></span></li>
</ul>
</li>
<li><span class="s1"><a href="https://www.airbus.com/be-an-airbus-supplier.html"></a></span></li>
</ul>
<p class="p2">EDI is the supply chain API, orchestrating purchasing, fulfillment, logistics, invoices, and other elements of commerce, automative, healthcare, aerospace, and other top industries. If you want the road map for API industry over the next 30 years, take a look at the EDI space. If we want the backbone of the API economy to move into the future and use modern API practices, we are going to need to target this layer of the economy that governs how data is moved around and incentivize companies to employ HTTP, and HTTP/2 and standardize on XML, JSON, Avro, Protocol Buffers, and other common data exchange and serialization formats. If you map out the world of EDI, you could plot what is needed when it comes to API adoption in the next couple of decades.</p>
<p class="p1">The EDI space is messy and specialized, but it is very busy. There are many different agencies and governing bodies out there servicing the EDI layer of the global economy. Next, I will be diving more into each of the standards, as well as who are some of the dominant brokers when it comes to the certification and brokering of EDI discovery, integration, and ultimately evolution. If we want to modernize this legacy world of APIs we are going to have to focus on these power brokers, helping make them more aware of APIs, and why they represent the future of data interoperability. The most movement I have seen in this area to showcase is the work around HL7 and the FHIR specification for healthcare, but I&rsquo;m going to need to assess the other business sectors serviced by EDI to understand their current state. After studying the world of EDI for a few days it is painfully clear how early in this whole API journey we are, and that the way we move data around with APIs is just in its infancy when it comes to the maturity and scope of EDI. Demonstrating to me that I&rsquo;m going to be spending the rest of my career evangelizing APIs, and helping people understand the benefits of standardizing how we move bits and bytes around using HTTP.</p>
