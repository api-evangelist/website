---
title: Evolving API SDKs at Google With Storage, Logging and Analytics
date: 2017-05-19 16:00:00 Z
tags:
- SDK
- Logging
- Storage
- Analytics
image: https://s3.amazonaws.com/kinlane-productions/google/sdk/google-sdk-essential-tools.png
---

<p><img style="padding: 15px;" src="https://s3.amazonaws.com/kinlane-productions/google/sdk/google-sdk-essential-tools.png" align="right" width="35%" /></p>
[One layer of my API research is dedicated to keeping track on what is going on with API software development kits (SDK)](http://sdk.apievangelist.com/). I have been looking at [trends in SDK evolution as part of continuous integration and deployment](http://sdk.apievangelist.com/2016/10/05/evolving-the-api-sdk-with-apimatic-dx-kits/), increased [analytics at the SDK layer](http://sdk.apievangelist.com/2016/10/04/increased-analytics-at-the-api-client-and-sdk-level/), and [SDKs getting more specialized](http://sdk.apievangelist.com/2016/09/30/api-sdks-getting-more-specialized/) in the last year. This is a conversation that [Google is continuing to move forward by focusing on enhanced storage, logging, and analytics at the SDK level](https://cloudplatform.googleblog.com/2017/05/use-Google-Cloud-Client-Libraries-to-store-files-save-entities-and-log-data.html).

Google provides a nice example of how API providers are increasing the number of available resources at the SDK layer, beyond just handling API requests and responses, and authentication. I'll try to carve out some time to paint a bigger picture of what Google is up to with SDKs. All their experience developing and supporting SDKs across hundreds of public APIs seems to be coming to a head with [the Google Cloud SDK effort(s)](https://cloud.google.com/sdk/).

I'm optimistic about the changes at the SDK level, so much I'm even advising APIMATIC on their strategy, but I'm also nervous about some of the negative consequences that will come with expanding this layer of API integration--things like latency, surveillance, privacy, and security are top of mind. I'll keep monitoring what is going on, and do deeper dives into SDK approaches when I have the time and $money$, and if nothing else I will just craft regular stories about how SDKs are evolving.

**Disclosure:** I am an advisor of [APIMATIC](https://apimatic.io/).