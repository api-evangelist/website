---
layout: post
title: "Why Every Education Company Needs an API (& Why Educators Should Care When One Doesn't)"
url: 'http://apievangelist.com/2012/04/13/why-every-education-company-needs-an-api/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/darcy_modified.jpg'
---

When I was a tech blogger for [ReadWriteWeb][1] and API-related news broke, we writers would often shudder. “Well, you can’t use API in the headline,” the argument in the newsroom went. It’s the page-view-kiss-of-death. That’s not because APIs aren’t super-important or super-ubiquitous on the Web (they are both). It’s because most “[normals][2]” don’t know what they are or why they matter. They’d rather click on a story that says “101 Ways to Use Pinterest to Plan Your Wedding.”

The decision to cover APIs regularly on ReadWriteWeb and eschew stories that fall into the “[Number] Ways to Use [Hot New Social Media Tool] to [Conduct a Seasonally-Relevant Activity]” goes a long way to explain the popularity of RWW versus that of Mashable, incidentally.

Also incidentally: Pinterest [has an API][3].

This all presents a bit of a challenge, of course, if I want to make an argument for my readers here about why APIs really matter in education. Do I frame the argument for “normals”? (Wait! HA! “Normals” don’t read Hack Education!) Do I frame it for educators? Entrepreneurs? Technologists? The answer: hopefully all of the above.

##  What is an API?

API stands for “Application Programming Interface.” At its most basic level, an API allows one app to talk to another app. It’s the way in which Web and mobile technologies can open up their data and their software’s functionality to others. It’s how Zynga integrates its games with your Facebook profile. It’s how websites handle accepting payments via Paypal and play YouTube videos. It’s how Instagram can share your photos to Facebook, Twitter, Flickr, and Tumblr.

Rather than having to export a file from one system, then import it into another, APIs allow programs to “make calls,” sending and receiving just the information they need just when they need it. Web APIs (also known as REST APIs) do this – well obviously – via the Web using the protocols of the Web (HTTP). But instead of returning HTML like a website does when you “call” it, Web APIs return XML or JSON – that is, machine-readable data that other apps and websites can make us of.

But enough with the tech…

##  Why does this matter in education?

Educational data is [stuck in silos][4], something fostered by educational software – administrative and instructional – that makes it cumbersome at best and impossible at worst to move data in and out of systems. As a result, there’s lots of extra clerical work that educators and administrators have to do – recreating rosters, copying grades, downloading CSVs, copying-and-pasting, and so on. All because educational apps and software do not, as a rule, talk to one another.

Student Information Systems don’t know which level of Angry Birds students are on. (Um hello, don’t laugh: [Angry Birds is science][5]!) A better example, perhaps: a school’s SIS might not talk to the district’s database or the state’s records system. Parents probably don’t get an automatic SMS when there’s an attendance issue or library book due. Learning management systems don’t automatically capture what or how far students have read in their e-readers or what they’ve annotated.

These functionalities (and lots more) are possible when there are APIs, opening the door to all sorts of _real-time_ connections between products, services, and systems that are currently impossible due to time constraints, burdensome download and data entry processes, and vendors who’d prefer to maintain data lock-in.

<img class="c1" src="https://s3.amazonaws.com/hackedu/darcy_modified.jpg" alt="" />

##  Where are the EDU APIs?

The absence of APIs from a lot of education applications, I’d argue, is a good indication that we’re still dealing in many cases with pre-Web era technologies (or at least a pre-Web era mindframe). Student information systems. Learning management systems. Educational software for your desktop computer. All pre-Web. And even newer versions of these older systems often carry forward this legacy of a world without Web (or hell, even Internet) connectivity.

APIs played a crucial part in the explosion of Web technologies. E-commerce. Social networking. Cloud computing. Now mobile computing. All facilitated by APIs. APIs have enabled companies like Facebook, Google, Amazon, and Twitter to become _platforms_, allowing other developers to build on top of them.

“Platforms” aren’t necessarily something we talk about in education, although they do exist and are being developed [with increasing frequency][6]. Google Apps for Education is certainly an example of one. [Edmodo][7] is attempting to carve a similar path, and with the release its API last month, I described the startup as making the move “[from social network to education platform][8].” Edmodo’s and Google’s APIs allows other companies – [Mathalicious][9], [Desmos][10], [Aviary][11], for example – to connect their apps to these platforms, tapping into rosters, roles, feeds, assignments, calendars, documents and so on.

The LMS could be a platform too, I suppose – [and with APIs, that’s the direction it could go][12]. But what’s interesting to me is that, with their origins in a pre Web 2.0 world, LMSes have devised a separate standard to offer connections to external modules – “[LTI][13],” not API. Is there widespread interest among third-party developers to integrate with LMSes via LTI? (To make the process simpler, [Instructure co-founder Brian Whitmer has created a site][14] with examples and code samples.) Or will the pervasiveness of Web APIs mean that developers' interest goes elsewhere?

I’m veering dangerously back into the technical realm here – the type of discussions that, as I started this post, tend to make “normals” not read and not care about APIs.

But here’s why they’re incredibly important, why we should pay attention to them in education, and why I recommend having an API is something you should look for in the tools you adopt: APIs make data accessible. APIs foster interoperability. APIs extend functionality. And APIs create an ecosystem -- of technology, of developers, of users.  

We want that for ed-tech, don't we?

<img class="c1" src="https://s3.amazonaws.com/hackedu/API_evangelist.jpg" alt="" />

_Disclosure: My boyfriend [Kin Lane][15] is the “[API Evangelist][16],” helping companies think through their API strategies, build their APIs, and support their developers – both internally and externally. So when I talk about the importance of APIs, I should note not just what they afford education but what they afford me. (As in, being an API evangelist than being an ed-tech writer). Thanks APIs!_

_Image credits: via [Darcy Norman's post on "the role of the LMS in higher ed][17]." I added the arrows, I admit, to demonstrate that all these systems need to talk to each other by means other than their Venn Diagram positionality._

   [1]: http://readwriteweb.com
   [2]: http://cdixon.org/2010/01/22/techies-and-normals/
   [3]: http://tijn.bo.lt/pinterest-api
   [4]: /2012/04/11/download-all-your-education-data-with-the-click-of-one-button/
   [5]: http://www.wired.com/wiredscience/2012/04/another-gravitational-experiment-in-angry-birds-space/
   [6]: http://www.elearnspace.org/blog/2011/10/13/the-race-to-platform-education/
   [7]: http://edmodo.com
   [8]: /2012/03/06/edmodo-makes-the-move-from-social-network-to-education-platform/
   [9]: http://mathalicious.com
   [10]: http://desmos.com
   [11]: http://aviary.com
   [12]: https://canvas.instructure.com/doc/api/
   [13]: http://www.imsglobal.org/lti/
   [14]: https://lti-examples.heroku.com/index.html
   [15]: http://kinlane.com
   [16]: http://apievangelist.com
   [17]: http://www.darcynorman.net/2012/04/02/on-the-role-of-the-lms-in-higher-education/
