---
published: true
layout: post
title: 'What is Your API Lifecycle?'
image: https://kinlane-productions2.s3.amazonaws.com/api-lifecycle-tag-cloud.png
tags:
    - Lifecycle
---
I like asking questions on Twitter then leaving and coming back to see the great answers people leave. Sometimes I get crickets, but depending on how I phrase the question, and how people interpret my question, I might get a stream of interesting views of the world of APIs. I recently asked a simple question. What is your API lifecycle? This is one of the ubiquitous phrases that we use in the API space that has no concrete definition and means many different things to many different people. I was sitting on a call listening to a conversation, and figured I'd tweet and ask folks what their perspective was.

> What is your API lifecycle? Mine is, design, mock, document, test, deploy, manage, SDKs, secure, performance, monitor, evangelize.
> 
> — API Evangelist (@apievangelist) [February 24, 2021](https://twitter.com/apievangelist/status/1364632813643853824?ref_src=twsrc%5Etfw)

I really like Mike's view of the API lifecycle, but more importantly how he "codifies" his lifecycle. It isn't just about a linear set of stops along a lifecycle, and more about a healthy loop you can use to bring APIs to life.

> /\* w/ repeating interations \*/  
> /\* exit-any b4 deploy \*/  
> /\* YMMV \*/  
> do {  
> explore,  
> select,  
> model,  
> design,  
> describe,  
> sketch,  
> prototype,  
> build,  
> document,  
> test,  
> secure,  
> deploy  
> } until {  
> freeze,  
> redirect,  
> deprecate,  
> donate  
> }[#API360](https://twitter.com/hashtag/API360?src=hash&ref_src=twsrc%5Etfw)
> 
> — Mike Amundsen (@mamund) [February 25, 2021](https://twitter.com/mamund/status/1364736525762781185?ref_src=twsrc%5Etfw)

Then Mike v2.0 chimes in with his honest and precise view of the landscape and how all of this truly works, introducing one of the most important stops along a modern API lifecycle--regret.

> One I see often is develop, deploy, document, regret, forget, sunset.
> 
> — Mike Ralphson (@PermittedSoc) [February 24, 2021](https://twitter.com/PermittedSoc/status/1364652554450329606?ref_src=twsrc%5Etfw)

Then Mike v3.0 jumps in with a design heavy view of the lifecycle that occurs between human beings. Mike makes it more like having a conversation about what is needed, then quickly deprecating and deleting.

> Discover and Define vocab: is the thing/capability defined? If not define.  
>   
> Discover and enhance vocab: relationships/synonyms with other things / affordances.  
>   
> API Design by my 3 questions.  
>   
> Implement primary and aliases.  
>   
> Iterate on feedback and usage data.  
>   
> Deprecate.  
>   
> Delete.
> 
> — Michael Hibay (@hibaymj) [February 24, 2021](https://twitter.com/hibaymj/status/1364646611964620800?ref_src=twsrc%5Etfw)

Then Frank demonstrates that emojis are an essential tool in all of our API toolbox. He also brings the wine/dine to the API lifecycle which I vote we make a required part of every API lifecycle.

> understand - \[design - mock - review - (🗑️)\] - \[develop - secure - detailed docs - collections/flows\] - \[deploy - publish to dev portals\] - \[maintain - support devs - evolve\] - retire (🌇)  
>   
> last stage has several cycles of (set-deprecation - wine/dine - unset-deprecation) 😋
> 
> — Frank Kilcommins (@fkilcommins) [February 26, 2021](https://twitter.com/fkilcommins/status/1365262278933807104?ref_src=twsrc%5Etfw)

Next Marc contributes very sobering test-driven view of the API lifecycle, acknowledging that there will be bugs and tears. I really like his contribution of the challenge stop along the API lifecycle, which should also be required for all APIs.

> For the moment we only Design->Challenge internally->Document->Develop->Human Tests->Deploy->Bugfix. I would be glad to have the time to setup testing automation (more over for regression tests). Mocking+Challenging externally (public APIs) should be a must too !
> 
> — Marc LEVISSE (@LevisseMarc) [February 24, 2021](https://twitter.com/LevisseMarc/status/1364660357965479937?ref_src=twsrc%5Etfw)

> But it's already far better than we used to do 2 years ago : Develop->Tests (by devs)->Deploy->Bugfix->Deploy->Bugfix->Deploy... + cry at every step after publication for devs to have choosen bad route/property names (Frenglish :))
> 
> — Marc LEVISSE (@LevisseMarc) [February 24, 2021](https://twitter.com/LevisseMarc/status/1364661133836242950?ref_src=twsrc%5Etfw)

No API lifecycle conversation is complete without Mr. Reinbold being at the table, bring the letter D center stage. Helping provide an easy to remember and say approach to defining the API lifecycle, which has the potential to be stickier in people's minds.

> the "7 D's" of [#API](https://twitter.com/hashtag/API?src=hash&ref_src=twsrc%5Etfw) lifecycle  
>   
> \* Discover - does it already exist?  
> \* Define - metadata on who & what  
> \* Design - create a description following a spec  
> \* Develop - code the sucker  
> \* Deploy - open for business  
> \* Deprecate - time to move on  
> \* Delete - cradle to grave, birth to death
> 
> — 𝕞𝕒𝕥𝕥𝕙𝕖𝕨 𝕣𝕖𝕚𝕟𝕓𝕠𝕝𝕕 (@libel\_vox) [February 24, 2021](https://twitter.com/libel_vox/status/1364642200924155905?ref_src=twsrc%5Etfw)

> I include things like "mock" and "testing" as part of a healthy development process. Things like creating documentation are part of deployment. A communication plan straddles deployment, deprecate, and deletion, etc.
> 
> — 𝕞𝕒𝕥𝕥𝕙𝕖𝕨 𝕣𝕖𝕚𝕟𝕓𝕠𝕝𝕕 (@libel\_vox) [February 24, 2021](https://twitter.com/libel_vox/status/1364642838412165120?ref_src=twsrc%5Etfw)

Then Mike v1.0 tapped Mehdi on the shoulder, who jumped in with a nice separation based upon the maturitiy of the the process and APIs, providing us with another set of stops to consider as part of our API lifecycles.

> Strategy, Design, Documentation, Mocking, Development, Testing/Virtualization, Deployment, Securing, Monitoring, Promotion/Discovery, Managing Change/Version  
>   
> all of this in different maturity phases for each : Creation, Publication, Realization, Productization, Retirement
> 
> — Mehdi Medjaoui (@medjawii) [February 25, 2021](https://twitter.com/medjawii/status/1364945555751899137?ref_src=twsrc%5Etfw)

Then Miqui chimed in to say that they were also using the same lifecycle as me.

> ..trying same over here...
> 
> — miqui (@Mandibuleen) [March 3, 2021](https://twitter.com/Mandibuleen/status/1367100297252847624?ref_src=twsrc%5Etfw)

Then there was this guy, who I worry is stuck in his iPhone, reminding us that we shouldn't version and that once you put forth a an API contract you will need to support until the day you die!!

> [#teamneverversion](https://twitter.com/hashtag/teamneverversion?src=hash&ref_src=twsrc%5Etfw) [#contractsareforever](https://twitter.com/hashtag/contractsareforever?src=hash&ref_src=twsrc%5Etfw)
> 
> — Marsh Gardiner (@earth2marsh) [February 24, 2021](https://twitter.com/earth2marsh/status/1364637856333918208?ref_src=twsrc%5Etfw)

Then Toby provides what feels like an extremely common pattern for what I am seeing across the enterprise, and reflects a very practical approach to doing APis.

> For our public API we design in OpenAPI, gather feedback internally, we mock the endpoints, perform user research with developers to make sure it's intuitive, then flesh out documentation further, then actually build, and test what we built against spec in CI pipeline.
> 
> — Toby Urff (@tobyurff) [February 25, 2021](https://twitter.com/tobyurff/status/1365084709169082370?ref_src=twsrc%5Etfw)

Then Migo gets straight to the point, with what feels a little oversimplistic, but very inspirational view of how you do APIs.

> Design, Write, Refactor, Refactor, Refactor 😅
> 
> — Migo (@migo315) [February 24, 2021](https://twitter.com/migo315/status/1364640477782368256?ref_src=twsrc%5Etfw)

Then King James steps up and shares a extremely balanced look at how and why we are doing APIs. Making it simple to understand, while also providing a book to help you understand how to do all of this.

> From my upcoming book:  
>   
> Align - business and tech teams collaborate to align on user outcomes  
>   
> Define - find boundaries and API profiles to deliver outcomes  
>   
> Design - the API for the style(s) needed, sync and async  
>   
> Deliver - mock, doc, code, test  
>   
> Manage - protect and evolve
> 
> — LaunchAny / James Higginbotham (@launchany) [February 25, 2021](https://twitter.com/launchany/status/1364785307435032576?ref_src=twsrc%5Etfw)

Then Allen reveals a critical illness in how we describe stops along the API lifecycle as sweeping generalizations, which is one of the reasons it can be so hard for us to get on the same page about the API lifecycle.

> Is build/develop/implement implied in the "deploy" step?
> 
> — Allen Helton (@AllenHeltonDev) [February 25, 2021](https://twitter.com/AllenHeltonDev/status/1364727437184139267?ref_src=twsrc%5Etfw)

Then Yonderwire reminds us to always do our homework and make sure our APIs are well planned and not just something we throw out into the universe.

> Research research research first
> 
> — YonderWire (@YonderWire) [February 25, 2021](https://twitter.com/YonderWire/status/1364989350572875781?ref_src=twsrc%5Etfw)

Tom gets straight to the point, and adds another dimension to the every popular anxiety stop along the API lifecycle by introducing hair loss into the mix!

> design, mock, test, requirements rewrite, test, last second additions, deploy, break-fix, hair loss, maybe documentation
> 
> — tom zmijewski (@tomzmijewski) [February 24, 2021](https://twitter.com/tomzmijewski/status/1364634421421346817?ref_src=twsrc%5Etfw)

Then Jason concludes the thread with a pretty simpele but effective approach to describing the API lifecycle, while also reminding us to evangelize, while acknowledging it probably will also be the first thing to go as we find ourselves overworked.

> design, test, deploy; secure, perf, & monitor are constraints. wish i had time to evangelize!
> 
> — Jason Mulligan (@jasonmulligan) [February 25, 2021](https://twitter.com/jasonmulligan/status/1364733648205979649?ref_src=twsrc%5Etfw)

A lot of personalities here. Some very interesting takes on what the API lifecycle can be. It gets me thinking about how diverse we play this API game. If I take the words used across all of these contributors I ended up with this tag cloud, showing what the top stops along the API lifecycle are for these folks.

![](https://kinlane-productions2.s3.amazonaws.com/api-lifecycle-tag-cloud.png)

I would really like to do more work to define what the API lifecycle is, or at least help establish a consistent way of defining different stops along an API lifecycle, and as a couple folks did as part of this thread, organize these stops into a coherent set of flows that are meaningful on the factory floor of enterprise organizations. I am really tired of saying API lifecycle and not really being on the same page with folks I am talking to about how to do APIs. It feels like we can significantly stablize how we do things if we can establish a common vocabulary for how we describe the API lifecycle similar to how we've found ways to describe our individual APIs using OpenAPI, AsyncAPI, and JSON Schema.