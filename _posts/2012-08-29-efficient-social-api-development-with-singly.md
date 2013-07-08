---
layout: default
title: 'Efficient Social API Development with Singly'
url: 'http://apievangelist.com2012/08/29/efficient-social-api-development-with-singly/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/singly-logo-horizontal.png'
---


<p>
     <a title="Singly" href="https://singly.com" target="_blank"><img src="https://s3.amazonaws.com/kinlane-productions/singly/Singly-Personal-Data-Explorer.png"  width="200" align="right" /></a>
</p>
<p>
     Last week I announced that <a title="API Evangelist and Singly Were Partnering" href="/2012/08/20/api-evangelist-partners-up-with-singly-to-evolve-the-social-and-personal-api-space/">API Evangelist and Singly were partnering</a>, and while I’m helping Singly with their API Evangelism strategy and they are providing me with some vital data on some of the most important APIs in the industry and how developers are using them--I’m fascinated by the Singly unified API model and how it can simplify developing apps that use social and personal data.
</p>
<p>
     As I do with any API, I sign up for an account, come up with an idea for a prototype, start hacking, then get to work telling the story of the process. To get started using Singly, I wanted to build a simply social data explorer that would help me understand how the platform works, but also give me a simple example for explaining to other developers.
</p>
<p>
     Before diving in, let me start with the basics. What is <a title="Singly" href="https://singly.com" target="_blank">Singly</a>?
</p>
<blockquote>
     Singly is a <a title="unified API interface for accessing social and personal data" href="https://singly.com">unified API interface for accessing social and personal data</a> from the top API platforms. Singly has built an API on Twitter, Facebook, LinkedIn and other API platforms. Simplified the authentication, objects and API endpoints into a unified API, allowing you to access multiple APIs through a single, simpler API interface, drastically improving the time you have to spend developing social features in your web and mobile apps.
</blockquote>
<p>
     For this project I focused on the top social network APIs: <a title="Facebook" href="https://www.singly.com/docs/facebook" target="_blank">Facebook</a>, <a title="Foursquare" href="https://www.singly.com/docs/foursquare">Foursquare</a>, <a title="Github" href="https://www.singly.com/docs/github">Github</a>, <a title="Instagram" href="https://www.singly.com/docs/instagram">Instagram</a>, <a title="LinkedIn" href="https://www.singly.com/docs/linkedin">LinkedIn</a> and <a title="Twitter" href="https://www.singly.com/docs/twitter">Twitter</a>. Ok, for many Github isn’t a social network. It’s something just geeks use, but to us, it is a social network. Anyways, let’s start building my social data exploration prototype.
</p>
<p>
     <img src="https://s3.amazonaws.com/kinlane-productions/github/github-logo.png"  width="120" align="right" />
</p>
<p>
     First, I <a title="signed up for Singly which was instant using my Github login" href="/2012/07/18/let-developers-register-for-your-api-with-their-github-profile/">signed up for Singly using my Github login</a>. Once signed up, I added my first Singly application, which allows me to generate application specific Singly keys, which features I will use, and provides a single interface to store and manage that access for each social network that I will be using. When adding a new app, it takes some time to setup, and create an app definition in all 6 social networks and add keys to my Singly app, but once you are all done, all you have to worry about is a single Singly key--Singly takes care of the rest.
</p>
<p>
     <img src="https://s3.amazonaws.com/kinlane-productions/singly/Singly-App-Management.jpg"  width="500" />
</p>
<p>
     Now I have a single API for accessing all six social APIs. Singly provides consistent endpoints across these services:
</p>
<ul >
     <li>https://api.singly.com/v0/services/facebook
     </li>
     <li>https://api.singly.com/v0/services/foursquare
     </li>
     <li>https://api.singly.com/v0/services/github
     </li>
     <li>https://api.singly.com/v0/services/instagram
     </li>
     <li>https://api.singly.com/v0/services/linkedin
     </li>
     <li>https://api.singly.com/v0/services/twitter
     </li>
</ul>
<p>
     Of course the objects you can work with across all of them aren’t the same, as they can be very different services, but the patterns are consistent and Singly standardizes the authentication and objects as much as possible across all APIs.
</p>
<p>
     The first authentication and code library for Facebook took me about 10 minutes. Then after that I was able to reuse my code and had all five other services up and running in another 10 minutes.
</p>
<p>
     How you use social data in your web and mobile applications will vary, but the unified API approach offered by Singly is taking API development to a new level. Using Singly I don’t think of terms of single APIs and how I have to approach each integration--I can now think of building social features into my applications across multiple APIs in a very seamless and efficient way.
</p>
<p>
     I will be exploring this same approach, using the other blogging, productivity and quantified self services Singly offers. I just wanted to get started with the social APIs, and begin wrapping my head around more efficient API development using a unified API like Singly.
</p>
