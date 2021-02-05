---
published: true
layout: post
title: 'No More Scraping Of Banking Data In Europe According to PSD2, Only APIs'
date: 2017-12-19T11:00:00.000Z
tags:
- API Evangelist
- Banking
- Regulations
- Financial
- Scraping
image: 'https://s3.amazonaws.com/kinlane-productions/psd2/european-commission-press-release-psd2-scraping.png"'
---
<p><a href="http://europa.eu/rapid/press-release_MEMO-17-4961_en.htm"><img src="https://s3.amazonaws.com/kinlane-productions/psd2/european-commission-press-release-psd2-scraping.png" align="right" width="45%" style="padding: 15px" /></a></p>Part of my partnership with [http://streamdata.io](Streamdata.io) centers around me investing more time into studying the banking industry, starting with the rollout of PSD2 in Europe next month. I'll be working through each aspect of the regulations for the banking industry when it comes to APIs, but I wanted to highlight a recent change regarding scraping that is pretty monumental. In [a recent press release from the European Commission they further clarified guidance for third party payment services providers (TPPs)](http://europa.eu/rapid/press-release_MEMO-17-4961_en.htm), and whether or not they can be scraping data from bank still, instead of using the APIs being mandated by the commission.

Here is the section from the press release specifically addressing "what data can TPPs access and use via screen scraping":

> PSD2 prohibits TPPs from accessing any other data from the customer payment account beyond those explicitly authorised by the customer. Customers will have to agree on the access, use and processing of these data.
> With these new rules, it will no longer be allowed to access the customer's data through the use of the techniques of "screen scraping". Screen scraping means accessing the data through the customer interface with the use of the customer's security credentials. Through screen scraping, TPPs can access customer data without any further identification vis-à-vis the banks.
> Banks will have to put in place a communication channel that allows TPPs to access the data that they need in accordance with PSD2. The channel will also be used to enable banks and TPPs to identify each other when accessing these data. It will also allow them to communicate through secure messaging at all times.
> Banks may establish this communication channel by adapting their customer online banking interface. They may also create a new dedicated interface that will include all necessary information for the relevant payment service providers.
> The RTS specifies the contingency safeguards that banks shall put in place if they decide to develop a dedicated interface. This will ensure fair competition and business continuity for TPPs.

Banks will have to provide APIs for aggregators to access data. Aggregators will not be allowed to scrape, and are being forced to use the APIs. While there will be a rolling out period, and I'm sure there will still be the bad actors on both sides of the equation, it is the groundwork for a much more sensible and secure approach to providing access to banking customers data--cleaning up the current mess. It is an important step for the banking sector, as well as a significant precedent for the API space when it comes to requiring API access to users data, allowing them to take advantage of valuable 3rd party services.

I'm seeing hints of similar language out of the CFPB regarding banking in the United States, but we are still years behind this kind of regulations. While I would like optimistic that the EU regulations will have an impact on the US when it comes to banks who do business overseas, I'm not holding my breathe. Where I'm going to be placing bets is when it comes to forward thinking banks like Capital One leading the charge when it comes to access to customer data via APIs because it makes sense, not because the government is mandating it. I'm not a big fan of government dictating that industries do APIs, I'm more about companies doing APIs because they make sense.
