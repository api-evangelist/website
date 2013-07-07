---
layout: post
title: 'API Ecosystem Tracking with StatsD and Graphite'
url: 'http://apievangelist.com2011/06/23/api-ecosystem-tracking-with-statsd-and-graphite/'
image: ''
---
{% include JB/setup %}
<img src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/graphite-stats-d.png"  width="250" align="right" />When managing an API and its ecosystem, we are all making this up as we go along. We have to constantly try new things, build them out, test, measure, and readjust.
Measuring being the most important, and when considering your API analytics, it shouldn't be just about tracking usage of your API. You should measure every aspect of your <a title="API ecosystem" href="http://www.apievangelist.com/ecosystem.php">API ecosystem</a>.
Applying metrics, gathering data, and reporting on this should be easy, and be part of your development DNA. Your metrics should be flexible and change as your ecosystem evolves. Any engineer, evangelist or other team member should be able to implement, gather and measure as the need arises.
I was introduced to StatsD and Graphite reporting last week, by <a title="Flip" href="http://twitter.com/!/mrflip">Flip</a> from <a title="InfoChimps" href="http://www.infochimps.com/">Infochimps</a>, while at the <a title="O'Reilly Velocity conference" href="http://velocityconf.com/velocity2011">O'Reilly Velocity Conference</a>.
<a title="StatsD" href="https://github.com/etsy/statsd">StatsD</a> is a dead simple NodeJS daemon that listens for messages over a UDP port. When a message is received, it parses the messages, and extracts metrics data.
<a title="Graphite" href="http://graphite.wikidot.com/faqtoc0">Graphite</a> is a highly scalable real-time graphing system. Data can be sent to Graphite's processing back-end, carbon, which stores the data in Graphite's specialized database. The data can then be visualized through graphite's web interfaces.
StatsD lets you define what you want to track, throw it at the StatsD over a UDP port, once processed you can schedule it to dump to Graphite for further processing and visualization.
Using StatsD + Graphite, you can provide any metric you wish, and Graphite will just report on it, with no management overhead. This type of flexibility provides the perfect agile environment measuring anything in an API ecosystem.
For example you can introduce new tracking for each deployment of an account sign-up widget using: StatsD::increment("widget.accountsignup.deploy");
StatsD will accept and process the new data, where Graphite will begin receiving, processing and provide a visualization for this new data set.
Since the StatsD interface is over UDP you don't have to worry about what this will do to your API or application performance, you just throw data at it....and let StatsD and Graphite do the rest.
StatsD and Graphite introduces a very flexible environment for analytics, allowing you to track anything and everything as you roll it out. You can track your API, widgets, forum activity, virtually anything you implement as part of your API ecosystem.
This type of deploy and measure strategy can help you understand whether your succeeding or failing in real-time. In the volatile world of APIs, this can mean the difference between overall success or failure with your API.
