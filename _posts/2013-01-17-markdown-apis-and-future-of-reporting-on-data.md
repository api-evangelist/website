---
layout: post
title: "Markdown APIs and Future of Reporting on Data"
url: 'http://apievangelist.com/2013/01/17/markdown-apis-and-future-of-reporting-on-data/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/markdown-icon.png'
---

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/markdown-icon.png" alt="" width="200" align="right" />

I just posted a story on [how I like the Guardian’s approach to data journalism][1], and spending time evolving on last nights [thoughts about the possibilities of Markup APIs][2].

As I’m [migrating much of the front-end of my websites to run on a home brew of Github Pages, Jekyll and JSON fueled Mustache Templates][3], I am seeing more of the potential of not just Markup APIs, but Markdown APIs that will run in a purely client side environment.

Imagine if I could go to a provider like the Guardian, US Census or other high value data provider, grab a link to a Markdown API JavaScript file that is relevant to a story or report you are working on.  With this Markdown API I would be given a whole dictionary of markdown you could use.

An example would be, that when I wanted the 2010 population for New York City, I could just write [population|New York|NY|US|2010], or something like that and would print out the actual population for that year in NYC, with a link to the source. Each time I used a markdown API it would add some sort of attribution to the source at the bottom of document.

Seems like we’d establish trusted, centralized sources of information, allowing anyone (even non-developers) to put open data and APIs to use via easy to implement markup or markdown APIs.

Think of the potential if facts around the web actually had the backing of trusted sources, and were able to be embedded anywhere on the web, via apps or digital documents.

It would be fun to create a markup and markdown API for API Evangelist, with a dictionary of terms, facts and other data that were relevant to the API industry.

   [1]: http://kinlane.com/2013/01/17/the-guardian-is-brilliant-in-supporting-relevant-events-with-open-data/ (how I like the Guardian’s approach to data journalism)
   [2]: /2013/01/16/markup-apis-and-api-scripting-platforms/ (Markup APIs)
   [3]: http://kinlane.com/2013/01/02/all-side-projects-are-now-hosted-on-github/
