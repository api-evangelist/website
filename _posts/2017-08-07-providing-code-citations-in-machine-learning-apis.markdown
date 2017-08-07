---
published: true
layout: post
title: Providing Code Citations In Machine Learning APIs
date: 2017-08-07T09:00:00.000Z
tags:
  - API Evangelist
  - Machine Learning
  - Definitions
  - Citations
  - Dependencies
image: >-
  https://s3.amazonaws.com/kinlane-productions/algorithmia/machine-learning-citation.png
---
<p><a href="https://algorithmia.com/algorithms/bkyan/StyleThief"><img src="https://s3.amazonaws.com/kinlane-productions/algorithmia/machine-learning-citation.png" align="right" width="40%" style="padding: 15px;" /></a></p>[I was playing around with the Style Thief, an image transfer API from Algorithmia](https://algorithmia.com/algorithms/bkyan/StyleThief), and I noticed the citation for the algorithm behind. The API is an adaptation of [Anish Athalye's Neural Style Transfer](https://github.com/anishathalye/neural-style/), and I thought the algorithmic citation of where the work was derived from was an interesting thing to take note of for my machine learning API research.

I noticed on Algorithmia's page there was [a Bibtex citation](http://www.bibtex.org/), which referenced the author, and project Github repository:

@misc{athalye2015neuralstyle,
  author = {Anish Athalye},
  title = {Neural Style},
  year = {2015},
  howpublished = {\url{https://github.com/anishathalye/neural-style}},
  note = {commit xxxxxxx}
}

This provides an interesting way to address citation in not just machine learning, but with open source driving algorithmic APIs in general. It gives me food for thought when it comes to [what licensing I should be considering when wrapping open source software with an API](http://apievangelist.com/2015/12/02/what-licensing-should-i-be-considering-when-i-take-open-source-software-and-offer-up-as-an-api/). I've been [thinking about dependencies a lot lately when it comes to APIs and their definitions](http://apievangelist.com/2017/08/04/including-api-dependencies-within-api-definition/), and I'd consider citation or attribution to be in a similar category. I guess rather then technical dependency, it is more in the business and legal dependency category.

Similar to how Pivio allows you to reference dependencies for your microservices, I'm thinking that [API Commons](http://apicommons.org), or some other format like Bibtext could provide a machine readable citation, that could be indexed as part of an [APIs.json index](http://apisjson.org). Allowing us API designers, architect, and providers to provide proper citation for where our work is derived. These aren't just technical dependencies, but also business and political dependencies, that we should ensuring are present with each API we deploy, providing an observable provenance of where ideas come from, and a honest look at how we build on the work of each other.
