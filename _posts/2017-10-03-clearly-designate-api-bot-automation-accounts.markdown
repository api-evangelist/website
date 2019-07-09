---
published: true
layout: post
title: Clearly Designate API Bot Automation Accounts
date: 2017-10-03T15:00:00.000Z
tags:
 - API Evangelist
 - Bots
 - Automation
 - Observability
 - Social
 - Messaging
image: 'https://s3.amazonaws.com/kinlane-productions/shieldsquare/good-v-bad-bots.png'
---
<p><a href="https://www.shieldsquare.com/good-bots-and-bad-bots/"><img src="https://s3.amazonaws.com/kinlane-productions/shieldsquare/good-v-bad-bots.png" align="right" width="40%" style="padding: 15px;" /></a></p>I'm continuing [my research into bot platform observability](http://apievangelist.com/2017/07/17/bot-observability-for-every-platform/), and [how API platforms are handling (or not handling) bot automation on their platforms](http://apievangelist.com/2017/08/15/which-platforms-have-control-over-the-conversations-around-their-bots/), as I try to make sense of each [wave of the bot invasion on the shores of the API sector](http://apievangelist.com/2017/10/02/the-waves-of-api-driven-bots-invading-our-shores/). It is pretty clear that Twitter and Facebook aren't that interested in taming automation on their platforms, unless there is more pressure applied to them externally. I'm looking to make sure there is a wealth of ideas, materials, and examples of how any API driven platform can (are) control bot automation on their platform, as the pressure from lawmakers, and the public intensifies.

Requiring users clearly identify automation accounts is a good first place to start. [Establishing a clear designation for bot users has its precedents](https://api.slack.com/bot-users), and requiring developers to provide an image, description, and some clear check or flag that identifies an account as automated just makes sense. [Providing a clear definition of what a bot is, with articulate rules for what bots should and shouldn't be doing](https://medium.com/slack-developer-blog/the-bot-rulebook-a442d9fb21cb) is next up on the checklist for API platforms. Sure, not all users will abide by this, but it is pretty easy to identify automated traffic versus human behavior, and having a clear separation allows accounts to automatically turned off when they fit a particular fingerprint, until a user can pass a sort of platform Turing test, or provide some sort of human identification.

Automation on API platforms has its uses. However, unmanaged automation via APIs has proven to be a problem. Platforms need to step up and manage this problem, or the government eventually will. Then it will become yet another burdensome regulation on business, and there will be nobody to blame except for the bad actors in the space (cough Twitter & Facebook, cough, cough). Platforms tend to not see it as a problem because they aren't the targets of harassment, and it tends to boost their metrics and bottom line when it comes to advertising and eyeballs. Platforms like Slack have a different business model, which dictates more control, otherwise it will run their paying customers off. The technology, and practices already exist for how to manage bot automation on API platforms effectively, they just aren't ubiquitous because of the variances in how platforms generate their revenue.

I am going to continue to put together a bot governance package based upon [my bot API research](http://bots.apievangelist.com/). Regardless of the business model in place, ALL API platforms should have a public bot automation strategy in place, with clear guidelines for what is acceptable, and what is not. I'm looking to provide API platforms with a one-stop source for guidance on this journey. It isn't rocket science, and it isn't something that will take a huge investment if approached early on. Once it gets out of control, and you have congress crawling up your platforms ass on this stuff then it probably is going to get more expensive, and also bring down regulatory hammer on everyone else. So, as API platform operators let's be proactive and take the problem of bot automation on directly, and learn from Twitter and Facebook's pain.

_**Photo Credit:** [ShieldSquare](https://www.shieldsquare.com/good-bots-and-bad-bots/)_
