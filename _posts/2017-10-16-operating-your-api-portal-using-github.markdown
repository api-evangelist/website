---
published: true
layout: post
title: Operating Your API Portal Using Github
date: 2017-10-16T11:00:00.000Z
tags:
  - API Evangelist
  - Portal
  - Github
  - Jekyll
image: 'https://s3.amazonaws.com/kinlane-productions/jekyll/jekyllrb.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/jekyll/jekyllrb.png" align="right" width="40%" style="padding: 15px;" /></p>Operating on Github is natural for me, but I am regularly reminded what a foreign concept it is for some of the API providers I'm speaking with. Github is the cheapest, easiest way to launch a public or private developer portal for your API. With the introduction of [Github Pages](https://pages.github.com/), each Github repository is turned into a place to host any API related project. In my opinion, every API should begin with Github, providing a place to put your API definition, portal, and other elements of your API operations.

If you are just getting going with understand how Github can be used to support your API operations, I wanted to provide a simple checklist of the concepts at play, that will lead you being able to publish your API portal to Github.

- **Github Account** - You will need an account to be able to use Github. Anything you do on Github that is public will be free. You can do private portals on Github, but this story is about using it for a public API portal.
- **Github Organization** - I recommend starting an organization for your API operations, instead of under just a single users account. Then you can make the definition for the API the first repository, and possibly the portal your second repository you create.
- **Github Repo** - A Github repository is basically a folder on the platform which you can start the code, pages, and other content used as part of API operations.
- [**Github Pages**](https://pages.github.com/) - Each Github repository has the ability to turn on a public project site, which can be used as a hosting location for a developer portal.
- [**Jekyll**](https://jekyllrb.com/) - Github Pages allows any Github repository to become a website hosting location which you can access via your Github user account, or even provide an address using your own domain.

I recommend every API provider think about hosting their API portal on Github. The learning curve isn't that significant to get up and running, and if your portal is public, it is free. You can version control, and leverage other key aspects of Github for evolving and managing your API portal. There are a growing number of examples of [forkable API portals like from the GSA](https://apievangelist.com/2017/06/14/gsa-api-standards-with-working-prototype-api-and-portal/), or [an interesting minimum viable API documentation template](http://portal.apievangelist.com/2017/09/05/a-new-minimumviable-documentation-jekyll-template-for-apis/) from my friend James Higginbotham ([@launchany](https://twitter.com/launchany)). Demonstrating that the practice is growing, with the number of healthy examples to build on diversifying.

If you need help understanding how to use Github for hosting your API developer portal, feel free to reach out. I am happy to see where I can help. Another thing to note is that this approach to running a Jekyll static website isn't limited to Github. You can always start the project there, and move off to any Jekyll enabled hosting provider. I run my entire network of websites and API project this way, leveraging Github as my plan A, and AWS as my plan B, with a server image ready to go when I need. Github just provides a number of bells and whistles that make it much more usable, as well as something others can collaborate around, enjoying the network effects that come with using the platform.
