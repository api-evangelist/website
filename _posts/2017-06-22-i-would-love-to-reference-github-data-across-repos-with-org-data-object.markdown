---
title: 'I Would Love To Reference Github Data Across Repos With [org].data.[object]'
date: 2017-06-22 13:00:00 Z
tags:
- Github
- API Evangelist
image: https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-github-icon.png
---

<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-github-icon.png" align="right" width="30%" style="padding: 15px;" /></p>I am a big fan of Jekyll and Github when it comes to managing data-driven projects. All of my research runs on Github, and I use Jekyll to serve up YAML and JSON representations of my research for a variety of purposes. I store all data that supports my research in the _data folder for each research project's repository. From there I will create HTML, Atom, and JSON representations for use in my API Evangelist storytelling.

When I am referencing any YAML data store I have in the _data folder I just use site.data.[object] to reference it. From there I can loop through collections, filter and show fields and other elements on the page using Liquid syntax. I love having all the data at my fingertips, but I'm thinking about the next step of data management at scale, as I work to build more data-driven repositories, housed within Github organizations, I want to be able to reach outside of each repo, into other repos stored within a single organization.

I would love it if Github allowed me to reference my data within an organization using [org].data.[object]. This way I could reference my [API design](http://design.apievangelist.com) research within my [hypermedia API](http://hypermedia.apievangelist.com) research. I have my API industry research segregated by topic for several reasons. Often it is just a logical separator, but sometimes the research is too big to fit into a single repository, and I'll shard thing by year, topic, or another logical separator. It would be nice if I could reach across the repository line, into other organizations within an organization, or maybe someday reach out into other organizations as well.

Just some thoughts as I'm working with YAML data at scale across hundreds of Github repositories. I handle this cross-repo access using JavaScript currently but would love it if it was natively built into Jekyll, allowing me to publish in a static way. The amount of Liquid YAML and JSON voodoo I could unleash would be pretty huge if I could reach across all my data drive projects and reference in a structured way.
