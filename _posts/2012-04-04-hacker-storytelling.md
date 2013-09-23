---
layout: post
title: "Hacker Storytelling"
url: 'http://apievangelist.com/2012/04/04/hacker-storytelling/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/ada-the-enchantress-of-numbers.jpg'
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/hacker-storytelling/ada-the-enchantress-of-numbers.jpg" alt="" width="150" align="right" />][1]

A big part of API evangelism, is storytelling. Storytelling about the API, the value it delivers, and the solutions it provides. Through my own hacking on an API, engaging with developers via email, a forum and social media, I gather ideas for projects that would help evangelize an API, while also educating users of how it works.

One example is a recurring question I get from [CityGrid API developers][2]\--how does CityGrid compare with other places APIs like Google Places and Yelp?

I set out to answer this question, quickly realizing it was easier said than done. I found 11 places APIs that fit my criteria, and they had many differences, so I started by writing a quick [overview of the 11 places APIs][3]. This helped me identify and quickly understand what each places API delivered.

Then I realized that I needed to actually hack on each API to truly understand how they work, and develop enough of an understanding where I could compare them in detail. To do this, I needed a project, to use as a anchor for my storytelling. Not just one blog post, but many, with code samples and starter kits to help support the project.

I chose to build an [Interactive Places API Comparison Tool.][4]

[<img class="c2" src="http://www.citygridmedia.com/developer/wp-content/uploads/2012/03/CityGrid-Google-Yelp-1024x189.png" alt="" width="500" align="center" />][4]

As a start, I chose 3 places APIs to compare: [CityGrid][5], [Google][6] and [Yelp][7]. The Interactive Places API Comparison Tool provides a what and where textual search as well as a latitude and longitude search, simultaneously across the 3 APIs.

Once I built the first prototype I [blogged about the comparison tool for the first time][8], as well as some of the research that went into it, like [Places API request format comparison][9]\--talking about how CityGrid, Google and Yelp each tailored their API requests.

Today I finished a report to support the what and where search and one for the latitude and longitude search. The report shows what was searched for, how many listings were pulled from each API and number of images, offers, reviews and tips for each place returned. I will be adding other reporting items in the future.

So far I’ve produced a lot of quality content from this hacker storytelling project:

  * 5 Blog Posts
  * Interactive API Comparison Web Application
  * Code Samples for Searching and Pulling Places Detail for 3 APIs
  * Code Libraries for Each of the 3 APIs

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/hacker-storytelling/Hyp3rL0cal-Interactive-Places-API-Comparison-Tool-Listing.png" alt="" width="250" align="right" />

All blog posts are syndicated out to Twitter, LinkedIn and Facebook as well as bookmarked at Reddit, StumbleUpon and Hacker News. All code samples live as Github Gists so I can embed in blog posts and other places, while code libraries live as Github repositories.

I’m about to post a bew blog post about the Interactive Places API Comparison reports I just finished, and will be adding Factual and Foursquare to the list of APIs that are compared as part of the tool. This will give me probably four or five more blog stories in the next couple days.

It is hard to tell where the project will go after that. The good hacker storytelling projects just keep living and producing blog posts, code samples, code libraries and starter kits. But there will always be new ideas for projects and stories when I engage with developers within the API community and on the open Internet.

   [1]: http://kinlane-productions.s3.amazonaws.com/api-evangelist/hacker-storytelling/ada-the-enchantress-of-numbers.jpg
   [2]: http://developer.citygridmedia.com/ (CityGrid API Developers)
   [3]: http://www.citygridmedia.com/developer/blog/overview-of-11-places-data-apis/ (overview of the 11 places apis)
   [4]: http://places-comparison-v1.hyp3rl0cal.com/index.php (Interactive Places API Comparison Tool)
   [5]: http://developer.citygridmedia.com/ (CityGrid)
   [6]: https://developers.google.com/maps/documentation/places/ (Google)
   [7]: http://www.yelp.com/developers/documentation/v2/overview (Yelp)
   [8]: http://www.citygridmedia.com/developer/blog/interactive-places-api-comparison-for-citygrid-google-and-yelp/
   [9]: http://www.citygridmedia.com/developer/blog/interactive-places-api-comparison-for-citygrid-google-and-yelp/ (places api comparison)
