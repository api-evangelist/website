---
published: true
layout: post
title: Monetizing Your Device Location Data With LotaData
date: 2018-07-11T09:00:00.000Z
tags:
  - API Evangelist
  - Monetization
  - Reclaim
  - Location
  - Data
image: 'https://s3.amazonaws.com/kinlane-productions/lotadata/lotadata-platform.png'
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>There are a lot of people making money off of the acquisition, organization, and providing access to data in our digital world. While I quietly tune into what the data monetization trends are, I am also actively looking for interesting approaches to generating revenue from data, but specifically with an eye on revenue sharing opportunities for the owners or stewards of that data. You know as opposed to just the exploitation of people's data, and generating of revenue without them knowing, or including them in the conversation. To help counteract this negative aspect of the data economy, I'm always looking to highlight (potentially) more positive outcomes when it comes to making money from data.

I was recently profiling the API of the [people intelligence platform LotaData](https://www.lotadata.com/), and I came across [their data monetization program](https://docs.lotadata.com/monetization.html), which provides an interesting look at how platforms can help data stewards generate revenue from data, but in a way that makes it accessible to individuals looking to monetize their own data as well. "LotaData's AI platform transforms raw location signals into 'People Intelligence' for monetization, usually based upon the follow key attributes: latitude, longitude, timestamp, deviceID, and accuracy."

<p><img src="https://s3.amazonaws.com/kinlane-productions/lotadata/lotadata_permits_panel_image.png" width="45%" align="right" style="padding: 15px;" /></p>Representing activity at a location and/or point in time, allowing LotaData's to understand what is happening at specific places at scale, and develop meaningful insights and behavioral segments that other companies and government agencies will want to buy into. Some of the examples they provide are:

- Commuting daily on CalTrain from Palo Alto to San Francisco
- Mid-week date night at Nopa on the way back from work
- Sweating it out at Soul Cycle on Saturday mornings
- Taking the dog out for a walk on Sunday afternoons
- Season ticket holder for Warriors games at the Oakland Arena

LotaData's location-based insights and segments are entirely inferred from raw location signals, emphasizing that they do not access or collect any personally identifiable information (PII) from mobile phones--stating that they "do not and never will collect PII such as name, email, phone number, date of birth, national identifier, credit cards, or other sensitive information". Essentially walking on the light side of the whole data acquisition and monetization game, and playing the honest card when it comes to the data economy.

When it comes to the monetization of data, LotaData enables marketers, brands, city governments and enterprise businesses to purchase location-based insights--providing an extensive network of data buyers who are ready to purchase the insights generated from this type of data. Then the revenue generated from the sale of an insight is split proportionately and shared with the app developers who contributed their app data. With the SDK agreement with LotaData governing the payment terms, conditions and schedule for sharing revenue. However, if you are unable to integrated LotaData's SDK in a mobile app for any reason, they can offer you alternative ways to share and monetize your location data:<p><img src="https://s3.amazonaws.com/kinlane-productions/lotadata/lotadata-ai-big-data-brain-platform.png" width="45%" align="right" style="padding: 15px;" /></p>

- **Geo-Context API** - The Geo-Context API is a simple script that you can embed in your mobile web sites and web apps. The script collects location data with explicit notice and permission obtained from end users.
- **Bulk Data Transfer** - Customers that are proficient in collecting location signals from their mobile apps, websites or other services, can easily upload their historical location archives to LotaData’s cloud for analyzing, inferring and monetizing mobile user segments. The data can be transferred to LotaData by configuring the appropriate access policies for AWS S3 buckets.
- **Integration** - LotaData can integrate with CRM and in-house data warehouse systems to ingest custom datasets or usage logs for deep analysis, enrichment and segmentation.
Questions?

Providing a pretty compelling model for data providers to monetize their location based data. It is something I'll be exploring more regarding how individuals can aggregate their own personal or professional data, as well as take advantage of the geo context API, bulk data transfer, or other integration opportunities. I have no idea how much money an individual or company could make from publishing data to LotaData, but the model provides an interesting approach that I think is worth exploring. It would be interesting to run a 30 to 90 test of tracking all of my location data, uploading it to LotaData, and then sharing the revenue details about what I can make with through a single provider like LotaData, as well as explore other potential providers so that you could sell your location data multiple times.

In a world where our data is the new oil, I'm interested in any way that I can help level the playing field, and seeing how we can put more control back into the device owners hands. Allowing mobile phone, wearable, drone, automobile, and other connected device owners to aggregate and monetize their own data in a personal or professional capacity. Helping us all better understand the value of our own bits, and potentially generating some extra cash from its existence. I don't think any of us are going to get rich doing this, but if we can put a little cash back in our own pockets, and limit the exploitation of our bits by other companies and device manufacturers, it might change the game to be a little more in our favor.
