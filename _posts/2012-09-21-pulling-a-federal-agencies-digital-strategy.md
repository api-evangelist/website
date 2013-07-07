---
layout: post
title: Pulling a Federal Agencies Digital Strategy
url: http://apievangelist.com2012/09/21/pulling-a-federal-agencies-digital-strategy/
source: http://apievangelist.com2012/09/21/pulling-a-federal-agencies-digital-strategy/
domain: apievangelist.com2012
image: 
---
{% include JB/setup %}<p>
     <img src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/federal-government/whitehouse-seal.png"  width="125" align="right" />
</p>
<p>
     Back in May, when the White House CIO has released a strategy, entitled "<a title="Digital Government: Building a 21st Century Platform to Better Serve the American People" href="http://www.whitehouse.gov/sites/default/files/omb/egov/digital-government/digital-government-strategy.pdf">Digital Government: Building a 21st Century Platform to Better Serve the American People</a>", which directs all federal agencies to publish HTML, JSON and XML versions of their digital strategy, I wrote a PHP script to monitor the progress. 
</p>
<p>
     To date, 25 federal agencies have successfully published their digital strategy, and I have been updating my script regularly to keep up. And while a few of the agencies still have querks with their HTTP Codes and with JSON formatting, the code is starting to stabilize.  So I decided to start <a title="Publishing to Github" href="https://github.com/kinlane/digital-strategy">sharing it on Github</a>, allowing others to put it to use.
</p>
<p>
     The first sample script I'm publishing is a <a href="https://github.com/kinlane/digital-strategy/blob/master/pull-agency.php">basic example of how to pull the JSON version of a single agencies digital strategy</a>.  Once it pulls the JSON, it then loops through each item and field on the strategy, and renders to screen.  It doesn't make any assumptions on what you wish to do with data.
</p>
<p>
     Next I will publish a more sophisticated version that stores values in a database.  Here is the pull federal agency digital strategy PHP script:
</p>
