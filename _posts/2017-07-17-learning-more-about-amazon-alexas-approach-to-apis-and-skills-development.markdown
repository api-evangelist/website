---
published: true
layout: post
title: Learning More About Amazon Alexas Approach to APIs And Skills Development
date: 2017-07-16T16:00:00.000Z
tags:
  - API Evangelist
  - Voice
  - Skills
  - Management
  - Review
image: >-
  https://s3.amazonaws.com/kinlane-productions/amazon/alexa/avs_getting_started_1.png
---
<p><a href="https://developer.amazon.com/alexa"><img src="https://s3.amazonaws.com/kinlane-productions/amazon/alexa/avs_getting_started_1.png" align="right" width="40%" style="padding 15px" /></a></p>I have had [Amazon Alexa](https://developer.amazon.com/alexa) in my cross hairs for some time now. I regularly digest stories about what Amazon is up to with Alexa, but haven't had the time to think deeply about voice enablement, and their approach to developing what they call "skills". I'm not 100% convinced voice enablement is the future of human compute interfaces, but I do see the role they can play in some situations, for some people. Plus, all the actions involved with Alexa and it's ecosystem are all driven using APIs, which will almost always make me perk up, and pay a little more attention--I have a serious problem.

The Amazon Alexa platform centers around two specific areas of development:

- **Alexa Voice Service** - The actual voice enablement, and baking Alex voice into applications, devices, your home, car, and other physical objects in our world.
- **Alexa Skills Kit** - The things that you can say to your Alex that will tigger specific actions, which make calls to APIs, and return something useful (or not).

Its all about baking Alex Voice Service baked into as many devices you possibly can, and develop the catalog of skills that the voice enabled application can put to use. Ok. Well, my next question(s) are 1) what is a skill, and 2) what can you actually do with skills? Amazon provides some resources to help with the basics:

- [**Understanding the Different Types of Skills**](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/understanding-the-different-types-of-skills)
- [**Understanding How Users Interact with Skills**](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/understanding-how-users-interact-with-skills)
- [**Requirements to Build a Skill**](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/requirements-to-build-a-skill)

Ok, helps me grasp what is their definition of a skill a little bit, and how it delivers their view of a voice enabled user interaction. Next, what can a skill really do? Or, what types of "skills" does Amazon want you to build? They start with the lofty perspective of "anything", or "[custom  skills](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/overviews/understanding-custom-skills)", to hook us technologists who like to think about at this level and fill in the gaps with our magical technological skills--a fundamental building block of API culture.

- Look up information from a web service
- Integrate with a web service to order something (order a car from Uber, order a pizza from Domino’s Pizza)
- Interactive games

This is API Evangelism 101. You start with everything and anything is possible, and work your way down from there. After lighting the imagination with custom skills, the focus in on a couple of specific types of actions, serving very specific purposes:

- [Smart Home Skill API](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/overviews/understanding-the-smart-home-skill-api)
	- Turn lights on and off
	- Change the brightness of dimmable lights
	- Change the color or color temperature of a tunable light
	- Change the temperature on a thermostat
	- Query a lock to see if it is currently locked
	- Ask for a smart home camera feed
- [Entertainment Device Control in the Smart Home Skill API](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/building-smart-home-skills-for-entertainment-devices)
	- Change the volume
	- Change the channel
	- Pause, rewind or fast forward music or video content
- [Video Skills API](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/understanding-the-video-skill-api)
	- Play a movie
	- Find a TV show
	- Change a channel
	- Pause, rewind, or fast forward video content
- [Flash Briefing Skill API](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/understanding-the-flash-briefing-skill-api)

Now the concept of a skill comes into focus a little more for me. Amazon really wants to encourage developers to develop features that deliver in a home environment, entertaining us. Alexa performance and entertainment skills. So far I have just pulled references from Amazon Alexa's documentation, if you want to see what has been developed by the community, you can head over [to the Alex skills catalog](https://www.amazon.com/b?node=13727921011). I also recommend [checking out a pretty robust 3rd party skills list](https://github.com/dale3h/alexa-skills-list), which gives a view of skills from the outside-in.

Alexa Voice Service and Skills Kit are the two core services, but when you browse the documentation, you see there is a 3rd area given just as much prominence--the [Alexa Fund](https://developer.amazon.com/alexa-fund), which "provides up to $100 million in investments to fuel voice technology innovation". This is an important aspect of the skills development conversation, an opportunity to get funding to support the creation of skills. While Slack doesn't use the word skills, [they also have a fund for investing in conversational interfaces](https://slack.com/developers/fund) (messaging, chat, and bot). One thing to note here, [Amazon has additional rewards program where developers can earn rewards when developing specially game skills for the Alexa platform](https://developer.amazon.com/public/solutions/alexa/rewards-for-skill-developers)--providing another glimpse into their strategy.

I am writing this post to support our Contrafabulist podcast, but I'm also doing it to feed my wider voice research as the API Evangelist. So I have to highlight some of the common building blocks of the Alexa approach to API management, helping me better understand Amazon's approach to this set of API resources.

- **Glossary** - https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/alexa-skills-kit-glossary
- **Forum** - http://forums.developer.amazon.com/forums/category.jspa?categoryID=60
- **FAQs** - https://developer.amazon.com/public/solutions/alexa/alexa-voice-service/docs/alexa-voice-service-developer-preview
- **Blog** - https://developer.amazon.com/blogs/alexa/tag/AVS
- **Terms of Service** - https://developer.amazon.com/public/solutions/alexa/alexa-voice-service/support/terms-and-agreements

Beyond the common building blocks for operating their developer portal, supporting their APIs, they have some interesting design elements available for developers. Helping direct Alex developers to develop skills and voice-enabled applications that fit in with their objectives:

- **Designing for AVS** - https://developer.amazon.com/public/solutions/alexa/alexa-voice-service/content/designing-for-the-alexa-voice-service
- **Functional Design Guide** - https://developer.amazon.com/public/solutions/alexa/alexa-voice-service/content/alexa-voice-service-functional-design-guide
- **UX Design Guidelines** - https://developer.amazon.com/public/solutions/alexa/alexa-voice-service/content/alexa-voice-service-ux-design-guidelines
- **Marketing Brand Guidelines** - https://developer.amazon.com/public/solutions/alexa/alexa-voice-service/content/marketing-brand-guidelines

These design elements tell an interesting story regarding how Amazon is aligning the concept of skills development with their voice enabled API strategy. It also provides an interesting approach to design guides that other API providers might want to consider. After the design guides, Amazon provides some interesting code and hardware to help developers, providing starter kits to get going developing skills as well as actual physical voice integration:

- **Projects and Sample Code** - https://github.com/alexa/alexa-avs-sample-app
- **API and Reference** - https://developer.amazon.com/public/solutions/alexa/alexa-voice-service/content/avs-api-overview
- **Development Kits for AVS** - https://developer.amazon.com/dev-kits
- **Development Kits (Hardware)** - https://developer.amazon.com/alexa-voice-service/dev-kits

There are three different stories going on here for me which I think are relevant to how we think about, and approach our usage of technology. I'm really interested in Amazon Alexa because of:

- **Voice Enablement** - How do you enable voice applications using APIs? What role will voice play in the wider conversational API landscape?
- **Skills Concept** - I am fascinated by the concept of a skill and how it applies to not just voice enablement, and conversational interface, but also representing a unit of compute or a transaction that occurs in API land (serverless, microservices, containers, etc.)
- **API Management** - How do you manage a set of APIs that serve conversational interfaces and voice-enablement? What is different than regular API management, and what can others learn from their approach?

As I said in the opening, I'm not 100% convinced that voice interfaces will be the future for everyone. I depend on the intimacy that exists between my fingers and the keyboard to make the magic happen each day--which might be a little noisy, but it doesn't involve me rambling on, talking to a device. Even though I'm not into voice interfaces, and much of a talker, I am interested in the motivations behind, and the approach that Amazon is taking with their conversational interfaces. It is something i'm comparing with my research into Twitter, Slack, as well as Facebook. These companies are investing a lot into their ecosystems--you can see the signs of it over at Amazon with [the 137 job openings for their Alex team](https://www.amazon.jobs/en/teams/alexa-skills?base_query=&loc_query=&job_count=10&result_limit=10&sort=relevant&team_category%5B%5D=alexa-skills&cache).

Audrey and I are going to talk about Amazon Alexa on our Contrafabulists podcast this week, so you can tune in to get more thoughts of mine regarding Alexa, and voice enablement APIs. I'll probably continue the exploration of my thoughts about this approach to interfaces, and particularly the development of "skills". Which I think has an interesting overlap with APIs, and the modularization we are seeing as a result of compute (ie. containers, microservices, devops), as well as the impact APIs are having on labor (ie. Uber, Mechanical Turk, Task Rabbit). I feel like there is a lot more going on here than just developing fun skills for having conversations with Alexa in your home.
