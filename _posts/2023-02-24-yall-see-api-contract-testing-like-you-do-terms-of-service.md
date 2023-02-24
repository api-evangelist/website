---
published: true
layout: post
title: "Y’all See API Contract Testing Like You Do Terms of Service"
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/aws-s3-stories-crypto-machine-bletchley-copper-circuit.png
author:
name: kinlane
tags:
- Testing
- Contracts
- Terms of Service
- Business
- Politics
---
I keep working through my API contract testing discussions with folks. I wrote about [getting pedantic when it comes to API contract testing last night](https://apievangelist.com/2023/02/23/getting-pedantic-about-api-contract-testing/) to help me get a grasp on things, and I am working on a piece about change to augment this post, but as I was laying there last night thinking about all of this, I am realizing that folks see API contracts in the same way they see terms of service.

Then majority of people I see wielding the phrase API contract testing around believe that and OpenAPI + JSON Schema driven design-first approach to providing a doc, mock, and set of contract test to be too burdensome, slow, and unnecessary. Like most things in the tech sector, you just push to production and that is the contract. Whatever is in product is the agreed upon contract between producer and consumer. The only problem here, is nothing was actually agreed upon. There was no negotiation. It becomes just like terms of service—-here is this lengthy “coded” “contract” from the producers view of the world, and as soon as you use the API—-you have agreed to the contract. The only thing I need to worry about now, is breaking said contract. But honestly, I really am not going to care about that either. In this house we move fast and break things.

Ultimately, I see a lot of lip service paid to the consumer. I see very little sitting down and working with consumers to actually hammer out a contract. This isn’t “design-first” vs. “code-first. Well, I guess it is. But I am not getting pedantic about design. I am getting pedantic about the consumers having a voice before things hit production. I am not advocating for OpenAPI and JSON Schema here. I am advocating that we agree upon the shape of the digital objects we pass back and forth, access to these objects, and that we can validate in a programmatic way that we are on the same page. I get it. We don’t have time in these fast-paced environments to do all of this. This is true if you ignore the downstream costs, and that you are probably spending more time and money to fix all the broken shit down the road. But hey, that is cool, as long as you don’t make me sit down and have to talk with you ahead of time.

Ultimately, I believe that there is no auto-generation of contracts or contract tests. You may be able to generate the boilerplate language for a contract and generate the code to validate these auto-generated contracts, but to actually have a true contract there needs to be discussion, understanding, and agreement between producer and consumer. This is a very human thing, and like the terms of service which I think will continue to be an area of friction for everyone, and something that heavily favors the producer, and us consumers must just agree and move on without ever really having a voice. Ok, now on to the “change” portion of this discussion, which I think is separate from the contracts, auto-generation, and other parts of the discussion.
