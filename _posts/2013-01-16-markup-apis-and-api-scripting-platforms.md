---
layout: post
title: "Markup APIs and API Scripting Platforms"
url: 'http://apievangelist.com/2013/01/16/markup-apis-and-api-scripting-platforms/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/markup-api.png'
---

<img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/scripting-platforms/markup-api.png" alt="" width="325" align="right" />

Over the holidays I added a [new section to API Evangelist called "trends][1]". One of the areas I’m tracking on is what I’m calling “[scripting platforms][2]”. While you can program against any API using the language of your choice, these platforms are aggregating APIs and make available through a custom language stack.

This approach is different than what I’m seeing from [aggregate APIs][3] like [Singly][4]. Scripting platforms may offer aggregate APIs, but are also providing a way to easily script against them, in new and abstracted ways. I’m [still trying to understand each company][5], as well as the nuances between each approach--so stay tuned.

In the last couple weeks, I’m seeing a possible new approach to programming against APIs come into focus, one that is using HTML instead of scripting--using Markup APIs.

After reading [Building Bridges Between GUIs and Code With Markup APIs][6] by Atul Varma ([@toolness][7]) from Mozilla, you can really start seeing not just the potential around rich media and content like Mozilla is with its [Webmaker platform][8], but deliver any API resource in abstracted, simplified markup anyone can put to use--without knowing programming.

Lyre Calliope takes this further discussing how, “Webmaker could be an opportunity to define an embeddable API strategy for the entire web”, and that “a Singly Markup API would lower the learning threshold for anyone interested in remixing all of their personal information together in new ways”, in [Markup APIs and the Read/Write Web][9].

I envision Markup APIs, at their simplest working like [Mustache Templates][10] where you can easily render data from JSON templates, or be as robust as what Mozilla is doing with their Webmaker platform.  Making the web embeddable and remixable like Lyre says. 

While scripting platforms are providing an important evolution in APIs for developers, by aggregating top APIs into new resources, the Markup API approach is an interesting evolution in APIs for everyone.  And with [browser based authentication solutions like Singly's][11], we can make this a very personalized experience.

I’m still working to understand all the possibilities, but I think both API scripting platforms and Markup APIs will bring us closer to a truly programmable web that is acceptable by everyone.

   [1]: http://apievangelist.com/trends/ (new section to API Evangelist called trends)
   [2]: /trends/scripting-platforms.php
   [3]: /trends/aggregation.php (aggregate APIs)
   [4]: http://singly.com (Singly)
   [5]: /2012/12/19/taking-apis-to-next-level-with-api-scripting-platforms/
   [6]: http://www.toolness.com/wp/2013/01/building-bridges-between-guis-and-code-with-markup-apis/ (Building Bridges Between GUIs and Code With Markup APIs)
   [7]: https://twitter.com/toolness
   [8]: https://webmaker.org/en-US/
   [9]: http://captaincalliope.net/2013/01/15/markup-apis-and-the-readwrite-web/
   [10]: http://mustache.github.com/
   [11]: https://singly.com/docs/data/authorization#Browser-based-Client-Apps
