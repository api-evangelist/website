---
published: true
layout: post
title: 'Providing Code Citations In Machine Learning APIs'
image: https://s3.amazonaws.com/kinlane-productions2/algorithmia/machine-learning-citation.png
---

<p><a href="https://algorithmia.com/algorithms/bkyan/StyleThief"><img src="https://s3.amazonaws.com/kinlane-productions2/algorithmia/machine-learning-citation.png" align="right" width="40%" style="padding: 15px;" /></a>
<p><a href="https://algorithmia.com/algorithms/bkyan/StyleThief">I was playing around with the Style Thief, an image transfer API from Algorithmia</a>, and I noticed the citation for the algorithm behind. The API is an adaptation of <a href="https://github.com/anishathalye/neural-style/">Anish Athalye’s Neural Style Transfer</a>, and I thought the algorithmic citation of where the work was derived from was an interesting thing to take note of for my machine learning API research.

<p>I noticed on Algorithmia’s page there was <a href="http://www.bibtex.org/">a Bibtex citation</a>, which referenced the author, and project Github repository:

<p>@misc{athalye2015neuralstyle,<br />
   author = {Anish Athalye},<br />
   title = {Neural Style},<br />
   year = {2015},<br />
   howpublished = {\url{https://github.com/anishathalye/neural-style}},<br />
   note = {commit xxxxxxx}<br />
}<br />

<p>This provides an interesting way to address citation in not just machine learning, but with open source driving algorithmic APIs in general. It gives me food for thought when it comes to <a href="http://apievangelist.com/2015/12/02/what-licensing-should-i-be-considering-when-i-take-open-source-software-and-offer-up-as-an-api/">what licensing I should be considering when wrapping open source software with an API</a>. I’ve been <a href="http://apievangelist.com/2017/08/04/including-api-dependencies-within-api-definition/">thinking about dependencies a lot lately when it comes to APIs and their definitions</a>, and I’d consider citation or attribution to be in a similar category. I guess rather then technical dependency, it is more in the business and legal dependency category.

<p>Similar to how Pivio allows you to reference dependencies for your microservices, I’m thinking that <a href="http://apicommons.org">API Commons</a>, or some other format like Bibtext could provide a machine readable citation, that could be indexed as part of an <a href="http://apisjson.org">APIs.json index</a>. Allowing us API designers, architect, and providers to provide proper citation for where our work is derived. These aren’t just technical dependencies, but also business and political dependencies, that we should ensuring are present with each API we deploy, providing an observable provenance of where ideas come from, and a honest look at how we build on the work of each other.


