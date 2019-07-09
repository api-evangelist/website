---
published: true
layout: post
title: Bot Observability For Every Platform
date: 2017-07-17T11:00:00.000Z
tags:
  - API Evangelist
  - Bots
  - Social
  - Observability
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-bot-showcase.png'
---
<p><a href="http://bots.apievangelist.com/"><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-bot-showcase.png" align="right" width="45%" style="padding: 15px" /></a></p>[I lightly keep an eye on the world of bots, as APIs are used to create them](http://bots.apievangelist.com/). In my work I see a lot of noise about bots usually in two main camps: 1) pro-bot - bots are the future, and 2) anti-bot - they are one of the biggest threats we face on the web. This is a magical marketing creating formula, which allows you to sell products to both sides of the equation, making money off of bot creation, as well as bot identification and defense--it is beautiful (if you live by disruption).

From my vantage point, I'm wondering why platforms do not provide more bot observability as a part of platform operations. There shouldn't be services that tell us which accounts are bots, the platform should tell us by default, which users are real and which are automated (you know you know). Platforms should embrace automation and providing services and tooling to assist in their operation, which includes actual definitions of what is acceptable, and what unacceptable bot behavior. Then actually policing this behavior, and being observable in your actions around bot management and enforcement.

It feels like this is just another layer of technology that is being bastardized by the money that flow around technology so easily. Investment in lots of silly useless bots. Investment in bot armies that inflate customer numbers, advertising, and other ways of generating attention (to get investment), and generate revenue. It feels like Slack is the only leading bot platform that has fully embraced the bot conversation. Facebook and Twitter lightly reference the possibilities, and have made slight motions when it comes to managing the realities of bots, but when you Google "Twitter Bots" or "Facebook Bots", neither of them dominate the conversation around what is happening--which very telling around how they view the world of bots.

Slack has [a formal bots directory](https://openreferral.slack.com/apps/category/At0MQP5BEF-bots), and has [defined the notion of a bot user](https://api.slack.com/bot-users), separating them from users--setting an example for bot developers to disclose who is bot, and who is not. They talk about [bot ethics](https://medium.com/slack-developer-blog/hard-questions-about-bot-ethics-4f80797e34f0), and [rules for building bots](https://medium.com/slack-developer-blog/the-bot-rulebook-a442d9fb21cb), and [do a lot of storytelling about their vision for bots](https://slackhq.com/a-beginner-s-guide-to-your-first-bot-97e5b0b7843d). Providing a pretty strong start towards getting a handle on the explosion of bots on their platform--taking the bull by the horns, owning the conversation, and setting the tone.

I'd say that Slack has a clearer business model for bots--not that people are actually going to pay for your bot (they aren't), but a model is present. You can some smell of revenue strategies on Facebook, but it just feels like all roads lead to Facebook, and advertising partners there. I'd say Twitter has no notion of a botlike business model for developers. This doesn't mean that Facebook and Twitter bots don't generate revenue for folks targeting Facebook and Twitter, or play a role in influencing how money flows when it comes to eyeballs and clicks. Indirectly, Twitter and Facebook bots are making folks lots of money, it is just that platforms have chosen not to observable when it comes their bot practices and ecosystems.

Platform observability makes sense for not just platform, and bot developers, as Slack demonstrates it makes sense for end-users. Incentivizing bots generating value, instead of mayhem. I'm guessing advertising-driven Facebook and Twitter have embraced the value of mayhem--with advertising being the framework for generating their revenue. Slack has more of a product, with customers they want to make happy. With Facebook and Twitter the end-users are the product, so the bot game plays to a different tune.
