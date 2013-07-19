---
layout: post
title: 'Providing Full Data Download vs API'
url: 'http://apievangelist.com/2013/07/19/providing-full-data-download-vs-api/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/download.png'
---

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/bw-icons/download.png" alt="" width="250" align="right" />

I've had so many discussions on this topic, I felt like I had written a post on it, but when the topic came up again today, I realized I hadn't. This is a regular conversation I get into with open data folks, regarding whether you should deploy open data as download vs an API.

I'll spare you having to read my entire rant, the answer is if you can, both. You should always provide a full data download, and additionally API access when the resources are available. There is no versus argument, there are scenarios where both are valuable and offer benefits over the other.

As a developer, I just want quick, complete access to data. I'm always in a hurry to just get to work, and I have the skills to parse, store, transform this data for whatever reason I will need. So let's just get to work. Give me a download and get the hell out of my way. Pretty straight forward logic. This is all true, but it is a very short-sighted, narrowly focused perspective and shouldn't impede larger, long term goals around data acquisition, management and access.

Taking your data, keying it up, and asking users to request a key and access via an API, might be a wall for the eager alpha dev, but there are many that could benefit from well thought out API end points, search &amp; filtering tools and the ability to offload all operations to someone else. Not all developers will be equipped to deal with the overhead of a full download.

Looking at it from a different vantage point, as a steward of data, an API can provide you with some very granular analytics on how people are using your data or even, not properly using your data. This valuable insight can provide an extreme amount of value in the future of how you gather your data, organize and make accessible. This is something you will never get from a single bulk download.

Many data folks argue that you can just rely on forums, IRC, Twitter to get feedback on this, no API needed. Again this is the single perspective from an alpha developer who will actively participate in these channels and offer insight. In reality, this is a small percentage of any ecosystem, and in my experience users don't usually offer feedback.

Secondarily if you are dealing with large datasets and large user bases, dealing with human feedback channels are expensive, something that can also done with API analytics in a cost effective, scalable way. And don't think I'm arguing for not using these channels, I'm saying don't overburden them unnecessarily. They are still very important.

The best example of this, that I use in the wild, is with U.S. Census Data. A couple years ago I had conversations with database folk at the Census, and asked them their thoughts on how innovators like Google are using census data for flu tracking, and news outlets are merging with their data to track on politics, immigration and other relevant issues. The response was, "we are familiar with some of this, but honestly haven't heard of many of these usage scenarios".

I asked why they don't launch an API alongside of downloads, require developers to get a key, then utilize API analytics to provide insight into other use cases around census data. You still don't have visibility into all use cases, but you'd get another group of interesting integrations.

The response was quickly, NO! The Census has to balance the trust of being gatherers and keepers of this data, we can't lock it up or apply any interpretation on top of the data. We need to remain a neutral party. (They now have an API, but that is another story)

Ok. I get that. But don't you want to make the census a more efficient process? Possibly completely digital? Or be able to gather new data points that could help people better understand health, educational, race or other issues that are reflected in our society? An API isn't always about control (it can be), an API can be about understanding and empower sensible stewardship of data, providing the insight you might need to make the process better.

Every person I've had this discussion with is coming from an alpha developers perspective, who quickly wants access to data and has the skills and resources to get it done. They are not thinking about the rest of developers, or the stewards of this data and the lifelong process that goes into making data acquisition, transformation and publishing better for everyone involved.

So when you are thinking about data download vs. API, remember, if you have the resources, you should do both. A download is a great place to start, but the overall health of your data will be better off if you can introduce the more granular level access and the measurement that an API can deliver.
