---
published: true
title: Algorithmic Observability In Predictive Policing
image: >-
  https://s3.amazonaws.com/kinlane-productions/algorotoscope/stories/crypto-machine-bletchley_copper_circuit.png
date: 2017-06-28T16:00:00.000Z
tags:
  - API Evangelist
  - Algorithms
  - Policing
  - Transparency
  - Observability
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algorotoscope/stories/crypto-machine-bletchley_copper_circuit.png" align="right" width="40%" style="padding: 15px;" /></p>As I study the world of APIs I am always on the lookout for good examples of APIs in action so that I can tell stories about them, and help influence the way folks do APIs. This is what I do each day. As part of this work, I am investing as much time as I can into better understanding how APIs can be used to help with algorithmic transparency, and helping us see into the black boxes that often are algorithms.

Algorithms are increasingly driving vital aspects of our world from what we see in our Facebook timelines, to whether or not we would commit a crime in the eyes of the legal system. [I am reading about algorithms being used in policing in the Washington Monthly](http://washingtonmonthly.com/magazine/junejulyaugust-2017/code-of-silence/), and I learned about an important example of algorithmic transparency that I would like to highlight and learn more about. A classic argument regarding why algorithms should remain closed is centered around intellectual property and protecting the work that gives you your competitive advantage--if you share your secret algorithm, your competitors will just steal it. While discussing the predictive policing algorithm, Rebecca Wexler explores the competitive landscape:

> But Perlin’s more transparent competitors appear to be doing just fine. [TrueAllele’s](https://www.cybgen.com/products/casework.shtml) main rival, a program called STRmix, which claims a 54 percent U.S. market share, has an official policy of providing defendants access to its source code, subject to a protective order. Its developer, John Buckleton, said that the key to his business success is not the code, but rather the training and support services the company provides for customers. “I’m committed to meaningful defense access,” he told me. He acknowledged the risk of leaks. “But we’re not going to reverse that policy because of it,” he said. “We’re just going to live with the consequences.”

> And remember [PredPol](http://www.predpol.com/), the secretive developer of predictive policing software? [HunchLab](https://www.hunchlab.com/), one of PredPol’s key competitors, uses only open-source algorithms and code, reveals all of its input variables, and has shared models and training data with independent researchers. Jeremy Heffner, a HunchLab product manager, and data scientist explained why this makes business sense: only a tiny amount of the company’s time goes into its predictive model. The real value, he said, lies in gathering data and creating a secure, user-friendly interface.

In my experience, the folks who want to keep their algorithms closed are simply wanting to hide incompetence and shady things going on behind the scenes. If you listen to individual companies like Predpol, it is critical that algorithms stay closed, but if you look at the wider landscape you quickly realize this is not a requirement to stay competitive. There is no reason that all your algorithms can't be wrapped with APIs, providing access to the inputs and outputs of all the active parts. Then using modern API management approaches these APIs can be opened up to researchers, law enforcement, government, journalists, and even end-users who are being impacted by algorithmic results, in a secure way.

I will be continuing to profile the algorithms being applied as part of predictive policing, and the digital legal system that surrounds it. As with other sectors where algorithms are being applied, and APIs are being put to work, I will work to find positive examples of [algorithmic transparency](http://apievangelist.com/2016/08/04/pushing-for-more-algorithmic-transparency-using-apis/) like we are seeing from STRmix and HunchLab. I'd like to learn more about their approach to ensuring observability around these algorithms, and help showcase the benefits of transparency and observability of these types of algorithms that are impacting our worlds--helping make sure everyone knows that black box algorithms are a thing of the past, and the preferred approach of snake oil salesman.
