---
title: Apicurio Is The Open Source Visual API Design Editor I Was Looking For
date: 2017-05-30 08:30:00 Z
tags:
- Design
- Editor
- Open Source
- API Evangelist
---

<p><a href="http://www.apicur.io/"><img style="padding: 15px;" src="https://s3.amazonaws.com/kinlane-productions/apicurio/apicurios-studio-methods.png" align="right" width="40%" /></a></p>
[I've been wanting someone to create an open source API editor for some time](http://apievangelist.com/2015/08/13/a-common-open-source-api-design-editor-is-needed-for-api-service-providers/), and now the folks over at Red Hat / 3Scale have delivered one [called Apicurio](http://www.apicur.io/). It is a web-based Angular2 app, for visually designing your APIs using OpenAPI, with a Github focus.

[Apicurio is that blend of visual designer, and code view that I was hoping for, letting you manage all your paths, and definitions using OpenAPI via Github](http://www.apicur.io/). It doesn't have all [the bells and whistles I'd love to see in my perfect API design editor](http://apievangelist.com/2014/06/25/if-i-could-design-my-perfect-api-design-editor/), but they are just getting going, and I think it is an excellent start.

Using Apicurio you can start a new API, or begin with an existing API by importing an OpenAPI (as it should be). When you are editing each path, it breaks up your verbs and has grayed out placeholders for adding any verbs you are missing--great inline API design literacy, helping folks quickly expand the design of their API. It is a slick, intuitive, API design interface which takes seconds to grasp what's going on and begin expanding the surface area of an API.

After making changes you can save it to Github, helping center the API design and definition process around Github, which can then be applied to the center of any API lifecycle. I really like how the design tool is a visual interface but you can always get at the machine readable definition behind, and edit it directly if you prefer. I feel like it is an interface that both developers and non-developers can put to work while still keeping OpenAPI at the center.

<p><img style="padding: 15px;" src="https://s3.amazonaws.com/kinlane-productions/apicurio/apicurios-studio-definitions.png" align="right" width="40%" /></p>

You can see where they are headed with APIcurio [by checking out the roadmap](http://www.apicur.io/roadmap/), as well as hints in the interface--like grayed out buttons for testing and documentation. I can see the tool turning into a full blown lifecycle management solutions, allowing you to design, deploy, manage, document, test, and many other useful areas along the API lifecycle. The OpenAPI definition and a Github repo core will all help set the stage for Apicurio delivering across the API lifecycle for developers.

I am adding Apicurio to [my API design research](http://design.apievangelist.com), and will be playing with, and keeping an eye on where it is going. It feels like the core API design editor the API space needs right now. We need a lot of standardizing at the API design layer at the moment and having a consistent visual editor for API service providers, and individual API designers to employ will go a long way in onboarding new users, and help existing users deploy APIs more consistently.

When it comes to API documentation, there isn't an excuse for most API providers and service providers to be hand-rolling their own API documentation--there is a good selection of open source solutions out there. Now there is movement in the same way when it comes to visual API designers that keep OpenAPI at the core. It will take a couple years to play out, but having an open source API design editor will have a significant impact on the community, similar to what open source interactive API documentation, and API management solutions have done over the last 5+ years.

Nice work Red Hat / 3Scale!
