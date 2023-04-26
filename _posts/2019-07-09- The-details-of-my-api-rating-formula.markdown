---
published: true
layout: post
title: 'The Details Of My API Rating Formula'
date: 2019-07-09T09:00:00.000Z
tags:
  - API Evangelist
  - Ratings
  - Ranking
image: >-
  https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/udnie-IMG_7559.jpg
author:
 name: kinlane
tags:
    - None
---
Last week I put some thoughts down about the basics of my API rating system. This week I want to go through each of those basics, and try to flesh out the details of how I would gather the actual data needed to rank API providers. This is a task I’ve been through with several different companies, only to be abandoned, and then operated on my own for about three years, only to abandon once I ran low on resources. I’m working to invest more cycles into actually defining my API rating in a transparent and organic way, then applying it in a way that allows me to continue evolving, while also using to make sense of the APIs I am rapidly indexing.

First, I want to look at the API-centric elements I will be considering when looking at a company, organization, institution, government agency, or other entity, and trying to establish some sort of simple rating for how well they are doing APIs. I’ll be the first to admit that ratings systems are kind of bullshit, and are definitely biased and hold all kinds of opportunity for going, but I need something. I need a way to articulate in real time how good of an API citizen an API provider is. I need a way to rank the searches for the growing number of APIs in my API search index. I need a list of questions I an ask about an API in both a manual, or hopefully automated way:

- **Active / Inactive **- APIs that have no sign of life need a lower rating.
    - **HTTP Status Code** - Do I get a positive HTTP status code back when I ping their URL(s)?
    - **Active Blog** - Does their blog have regular activity on it, with relevant and engaging content?
    - **Active Twitter** - Is there a GitHub account designated for the API, and is it playing an active role in its operations?
    - **Active GitHub** - Is there a GitHub account designated for the API, and is it playing an active role in its operations?
    - **Manual Visit** - There will always be a need for a regular visit to an API to make sure someone is still home.
- **Free / Paid** - What something costs impacts our decision to use or not.
    - **Manual Visit** - There is no automated way to understand API pricing.
- **Openness** - Is an API available to everyone, or is a private thing.
    - **Manual Review** - This will always be somewhat derived from a manual visit by an analyst to the API.
    - **Sentiment Analysis**  - Some sentiment about the openness could be established from analyzing Twitter, Blogs, and Stack Exchange.
- **Reliability** - Can you depend on the API being up and available.
    - **Manual Review** - Regularly check in on an API to see what the state of things are.
    - **Sentiment Analysis** - Some sentiment about the reliability of an API could be established from analyzing Twitter, Blogs, and Stack Exchange.
    - **Monitoring Feed / Data** - For some APIs, monitoring could be setup, but will cost resources to be able to do accurately.
- **Fast Changing** - Does the API change a lot, or remain relatively stable.
    - **Manual Review** - Regularly check in on an API to see how often things have changed.
    - **Change Log Feed** - Tune into a change log feed to see how often changes are Ade.
    - **Sentiment Analysis**   - Some sentiment about the changes to an API could be established from analyzing Twitter, Blogs, and Stack Exchange.
- **Social Good** - Does the API benefit a local, regional, or wider community.
    - **Manual Review** - It will take the eye of an analyst to truly understand the social impact of an API.
- ****Exploitative** - Does the API exploit its users data, or allow others to do so.
    - **Manual Review** - It will take a regular analyst review to understand whether an API has become exploitative.
    - **Sentiment Analysis** - Some sentiment about the exploitative nature of an API could be established from analyzing Twitter, Blogs, and Stack Exchange.
- **Secure** - Does an API adequately secure its resources and those who use it.
    - **Manual Review** - Regularly check in on an API to see how secure things are.
    - **Sentiment Analysis** - Some sentiment about the security of an API could be established from analyzing Twitter, Blogs, and Stack Exchange.
    - **Monitoring Feed / Data** - For some APIs, monitoring could be setup, but will cost resources to be able to do accurately, unless provided by provider.
- **Privacy** - Does an API respect privacy, and have a strategy for platform privacy.
    - **Manual Review** - Regularly check in on an API to see how privacy is addressed, and what steps the platform has been taking to address.
    - **Sentiment Analysis** - Some sentiment about the privacy of an API could be established from analyzing Twitter, Blogs, and Stack Exchange.
- **Monitoring** - Does a platform actively monitor its platform and allow others as well.
    - **Manual Review **- Regularly check in on an API to see how secure things are.
    - **Sentiment Analysis** - Some sentiment about the security of an API could be established from analyzing Twitter, Blogs, and Stack Exchange.
    - **Monitoring Feed / Data** - For some APIs, monitoring could be setup, but will cost resources to be able to do accurately, unless provided by provider.
- **Observability** - Is there visibility into API platform operations, and its processes.
    - **Manual Review** - It will always take an analyst to understand observability until there are feeds regarding every aspect of operations.
- **Environment** - What is the environment footprint or impact of API operations.
    - **Manual Review** - This would take a significant amount of research into where APIs are hosted, and disclosure regarding the environment impact of data centers, and the regions they operate in.
- **Popular** - Is an API popular, and something that gets a large amount of attention.
    - **Manual Review** - Analysts can easily provide a review of an API to better understand an APIs popularity.
    - **Sentiment Analysis** - Some sentiment about the presence of an API could be established from analyzing Twitter, Blogs, and Stack Exchange.
    - **Twitter Followers**** - The number of Twitter followers for an account dedicated to an API provides some data.
    - **Twitter Mentions** - Similarly the number of mentions of an API providers Twitter account provides additional data.
    - **GitHub Followers** - The number of GitHub followers provides another dimension regarding how popular an API is.
    - **Stack Exchange Mentions** - The question and answer site always provides some interesting insight into which APIs are being used.
    - **Blog Mentions** - The number of blog posts on top tech blogs, as well as independent blogs provide some insight into popularity.
- **Value** - What value does an API bring to the table in generalized terms.
    - **Manual Review ****- The only way to understand the value an API brings to the table is for an analyst to evaluate the resources made available. Maybe some day we’ll be able to do this with more precision, but currently we do not have the vocabulary for describing.

I am developing a manual questionnaire I can execute against while profiling every API. I have already done this for many APIs, but I’m looking to refine for 2019. I will also be automating wherever I can, leverage other APIs, feeds, and some machine learning to help me augment my heuristic analyst rank with some data driven elements. Some of these will only change when I, or hopefully another analyst reviews them, but some of this will be more dependent on data gathered each month. It will take some time for a ranking system based upon these elements to come into focus, but I’m guessing along the way I”m going to learn a lot, and this list will look very different in twelve months.

Next, I wanted to look at the elements of the rating system itself which I think are essential to the success of an API ranking system based upon the elements above. I’ve seen a number of efforts fail when it comes to indexing and ranking APIs. It is not easy. It is a whole lot of work, without an easy path to monetization like Google established with advertising. Many folks have tried and failed, and I feel like some of these elements will help keep things grounded, and provide more opportunity for success, if not at least sustainability.

- **YAML Core** - I would define the rating system in YAML.
    - **Rating Formula** - The rating formula is machine readable and available as YAML, taking everything listed above and automating the application of it across APIs using a standard YAML definition.
    - **Rating Results** - Publishing a YAML dump of the results of rating for each API provider, also providing a machine readable template for understanding how each API provider is being ranked.
- **GitHub Base** - Everything would be in a series of repositories.
    - **GitHub Repo** - A GitHub repository is the unit of compute and storage for the rating.
    - **Git Management** - I am using GitHub to apply the rating system across all APIs in my search index.
    - **GitHub API Management** - I am automating the granular editing of the YAML core using the GitHub API.
- **Observable** - The entire algorithm, process, and results are open.
    - **Search Transparency** - I will be tracking keyword searches, minus IP and user agent, then publishing the results to GitHub as YAML.
    - **Minimal Tracking** - There will be minimal tracking of end-users searching and applying the ranking, with tracking being provider focused.
- **Evolvable** - It would be essential to evolve and adapt over time.
    - **Semantic Versioned** - The search engine will be semantically versioned, providing a way of understanding it as it evolves.
    - **YAML** - Everything is defined as YAML which is semantically versioned, so nothing is removed or changed until major releases.
- **Weighted** - Anyone can weight the questions that matters to them.
    - **Data Points** - All data points will have a weight applied as a default, but ultimately will allow end-users to define the weights they desire.
    - **Slider Interface** - Providing end-users with a sliding interface for defining the importance of each data point to them, and apply to the search.
- **Completeness** - Not all the profiles of APIs will be as complete as others.
    - **Data Points** - The continual addition and evolution of data points, until we find optimal levels of ranking across industries, for sustained periods of time.
- **Ephemeral** - Understanding that nothing lasts forever in this world.
    - **Inactive** - Making sure things that are inactive reflect this state.
    - **Deprecation** - Always flag something as deprecated, reducing in rank.
    - **Archiving** - Archive everything that has gone away, keeping indexes pure.
- **Community** - It should be a collaboration between key entities and individuals.
    - **GitHub** - Operate the rating system out in the open on GitHub, leveraging the community for evolving.
    - **Merge Request** - Allow for merge requests on the search index, as well as the ratings being applied.
    - **Forks** - Allow for the workability of the API search, leveraging ranking as a key dimensions for how things can be forked.
    - **Contribution** - Allow for community contribution to the index, and the ranking system, establishing partnerships along the way.
- **Machine Readable** - Able for machines to engage with seamlessly.
    - **YAML** - Everything is published as YAML to keep things simple and machine readable.
    - **APIs.json** - Follow a standard for indexing API operations and making them available.
    - **OpenAPI** - Follow a standard for indexes the APIs, and making them available.
- **Human Readable** - Kept accessible to anyone wanting to understand.
    - **HTML** - Provide a simple HTML application for end-users.
    - **CSS** - Apply a minimalist approach to using CSS.
    - **JavaScript** - Drive the search and engagement with client-side JavaScript, powered by APIs.

This provides me with my starter list of elements I think will set the tone for how this API search engine will perform. Ultimately there will be a commercial layer to how the API search and ranking works, but the goal is to be as transparent, observable, and collaborative around how it all works. A kind of observability that does not exist in web search, and definitely doesn’t in anything API search related. I’ll give it to DuckDuckGo, for being the good guys of web search, which I think provides an ethical model to follow, but I want to also be open with the rating system behind, to avoid some of the illness that commonly exists within rating agencies of any kind.

Next stop, will be about turning the rating elements into a YAML questionnaire that I can begin systematically applying to the almost 2,000 APIs I have in my index. With most of it being a manual process, I need to get the base rating details in place, begin asking them, and then version the questionnaire schema as I work my way through all of the APIs. I have enough experience with profiling APIs to know that what questions I ask, how I ask them, and what data I can gather about API will rapidly evolve once I begin trying to satisfy questions again real world APIs. How fast I can apply my API rating system to the APIs I have indexed, as well as quickly turn around and refresh over time will depend on how much time and resources I am able to manifest for this project. Something that will come and go, as this is just a side project for me, to keep me producing fresh content and awareness of the API space.
