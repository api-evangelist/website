---
published: true
layout: post
title: 'Positive API Behavioral Reinforcement'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/bf-skinner-old-chair-hopsital.jpg
author:
    name: kinlane
tags:
- Governance
- Spectral
- Policies
- Rules
---
I started API Evangelist because people were telling me I was doing the REST API thing wrong, and being pretty shitty about it along the way. I don’t mind being corrected, but when the RESTafarians in 2010 were telling me I was doing APIs wrong and none of them were helping me learn the “right way”—-I wanted a way to push back in my own way. It is what made me spend the next decade helping guide people in a positive direction when it comes to doing APIs. While I am fully aware that I can also be mean from time to time, and I struggle to always be super helpful, I work hard to try and center my work in reinforcing positive behaviors and outcomes when it comes to doing APIs in this often chaotic digital world we all operate in.

One way I have been centering myself when it comes to guiding people in a positive direction involves API governance using Spectral rules. I have run hundreds of Spectral rules against many different OpenAPI definitions, and other types of schema, and while I don’t mind being hit with tens or hundreds of things I’ve done wrong in my API design—-it know that most people just see this as an overwhelming negative on their recurring journey to satisfying their Jira ticket at the end of their sprint. When you don’t have a strong grasp and interest in API design, and you do not have a healthy awareness of OpenAPI and why it matters to have a complete and accurate contract, you will ultimately see the 100+ errors you just received as huge negative standing in between you and what you are trying to accomplish.

It doesn’t work for every rule, but for the majority of the Spectral rules I create, I produce both a negative and a positive version. For everything I critique on being missing from your API design I also reward you for it being present. I am looking to reward you for all the hard work you’ve done and make sure that any additional work you do is known and available for you to learn from, even after you have fixed it. The absence of education, enablement, and positive reinforcement across the API lifecycle is why we are in the state of finding ourselves when it comes to technical debt and the perpetually growing API sprawl. The enterprise doesn’t invest in education and shining a light on the incremental hard work that teams are doing when it comes to designing and delivering APIs. When it comes to API governance we often dive into the negative end of the swimming pool rather than providing positive behavioral reinforcement. It is something that ultimately slows us down. 

When I design any Spectral rule, I give it a meaningful name, description, and message, and then as I am crafting the JSON Path and supporting rule, I think about both sides of the equation. I think about what I am looking for in the design of each API, but I am also looking to showcase when it is present-—not just when it is missing. With this approach I have gotten more thoughtful during policy and rule design-time, which is paying dividends when it comes to influencing things across the API lifecycle. Each rule isn’t simply a JSON path that is truthy or falsy, and beyond the impact on an API, there is an impact on everyone involved with designing, developing, and delivering an API, as well as those involved in consuming APIs downstream. In this shared environment a little positive API behavioral reinforcement will go along ways, and when you think about the hundreds of details that should be present, it all adds up pretty quickly.