---
layout: post
title: 'The White House Releases An Open Data Strategy'
url: 'http://apievangelist.com2013/05/11/the-white-house-releases-an-open-data-strategy/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/obama-white-house-open-data.jpg'
---
{% include JB/setup %}
<table cellspacing="3" cellpadding="5" align="right">
     <tbody>
          <tr>
               <td align="center">
                    <img src="https://s3.amazonaws.com/kinlane-productions/federal-strategy/obama-white-house-open-data.jpg" border="0" width="300" />
               </td>
          </tr>
          <tr>
               <td align="center">
                    <strong><a href="http://www.flickr.com/photos/whitehouse/8638883692/" target="_blank">Photo Credit - White House</a></strong>
               </td>
          </tr>
     </tbody>
</table>
<p>
     President Obama issued an Executive Order this last week - <a href="http://www.whitehouse.gov/the-press-office/2013/05/09/executive-order-making-open-and-machine-readable-new-default-government-">Making Open and Machine Readable the New Default for Government Information</a>. A move that will signficantly define the fast growing API economy.  But before I dive into what this means for open data and APIs, I wanted to recap the last year of progress in Washington when it comes to open data and APIs.
</p>
<p>
     If you recall, in May of 2012, the White House issued the <a href="http://www.whitehouse.gov/sites/default/files/uploads/2012digital_mem_rel.pdf">Memorandum on Building a 21st Century Digital Government</a>, which provided federal agencies with a 12-month roadmap to get familiar the concept of possessing a healthy digital strategy, which involves taking a strategic approach to using social, cloud computing and mobile, with open data and APIs as the core.
</p>
<p>
     After reading the directive from the White House in 2012, I wrote <a href="http://apievangelist.com/2012/06/01/barak-obama-directs-all-federal-agencies-to-have-an-api/">Barack Obama Directs All Federal Agencies to Have an API</a>, which is still one of the most viewed posts on API Evangelist, after <a href="http://apievangelist.com/2012/01/12/the-secret-to-amazons-success-internal-apis/">The Secret to Amazons Success Internal APIs</a>.
</p>
<p>
     While I am a believer in both APIs and the potential of healthy government leadership, I'm also very skeptical of blind API faith and of our federal government to deliver on open data. After reading the directive out of the White House last year, I got to work understanding, tracking and quantifying the potential and progress coming out of Washington when it comes to open data and APIs.
</p>
<p>
     The important thing to understand about the White House Digital Strategy, is that it doesn't just say open up APIs to support open data and mobile iniatives, it also says to make these efforts discoverable by providing a HTML, JSON and XML version of each agencies digital strategy--making their strategy and resulting data sets not just machine readable, but also machine discoverable. This is the critical aspect of the digital strategy, which will act as the gears in the government fueled API economy, but it also gave me an idea on how to measure the progress of each agency in the Digital Strategy and resulting open data efforts.
</p>
<p>
     All federal agency were directed to develop a digital strategy around open data and mobile, then publish it at their website in HTML, XML and JSON. So I got to work quantifying this. I wanted to understand which agencies had done this successfully. To begin I needed a list of federal agencies, which I was able to pull from the <a href="http://www.usa.gov/About/developer-resources/federal-agency-directory/index.shtml" target="_blank">Federal Agency Directory API</a>. Now I had a database of each agency name, abbreviation code and URL. Next I wrote a script that "pinged" each agencies URL and looked for http://[agencyname].gov/digitalstrategy.html, http://[agencyname].gov/digitalstrategy.xml and http://[agencyname].gov/digitalstrategy.json. I ran this script each night to see who had published their strategy.
</p>
<p>
     Coming up on a year after the release of <a href="http://www.whitehouse.gov/the-press-office/2012/05/23/presidential-memorandum-building-21st-century-digital-government">Memorandum on Building a 21st Century Digital Government</a>, we have <span >0 "agencies" that have published a digital strategy:
</p>