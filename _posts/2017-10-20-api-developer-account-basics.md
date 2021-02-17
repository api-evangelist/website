---
published: true
layout: post
title: 'API Developer Account Basics'
image: https://s3.amazonaws.com/kinlane-productions2/algo-rotoscope/stories/cargo-ship-on-sea_blue_circuit.jpg
---

<p><img src="https://s3.amazonaws.com/kinlane-productions2/algo-rotoscope/stories/cargo-ship-on-sea_blue_circuit.jpg" align="right" width="45%" style="padding: 15px;" />
<p>I’m helping some clients think through their approach to API management. These projects have different needs, as well as different resources available to them, so I’m looking to distill things down to the essential components needed to get the job done. The first element you need to manage API access is the ability for API consumers to be able to sign up for an account, that will be used to identify, measure usage, and engage with each API consumer.

<p><strong>Starts With An Account</strong>
While each company may have more details associated with each account, each account will have these basics:

<ul>
  <li><strong>account id</strong> - A unique identifier for each API account.</li>
  <li><strong>name</strong> - A first name and last name, or organization name.</li>
  <li><strong>email</strong> - A valid email address to communicate with each user.</li>
</ul>

<p>Depending on how we enable account creation and login, there might also be a password. However, if we use existing OpenID or OAuth implementations, like Github, Twitter, Google, or Facebook, this won’t be needed. We are relying on these authentication formats as the security layer, eliminating the need for yet another password. However, we still may need to store some sort of token identifying the user, adding these two possible elements:

<ul>
  <li><strong>password</strong> - A password or phrase that is unique to each user.</li>
  <li><strong>token</strong> - An OAuth or other token issued by 3rd party provider.</li>
</ul>

<p>That provides us with the basics of each developer API developer account. It really isn’t anything different than a regular account for any online service. Where things start to shift a little specifically for APIs, is that we need some sort of keys for each account that is signing up for API access. The standard approach is to provide some sort of API key, and possibly a secondary secret to compliment it:

<ul>
  <li><strong>api key</strong> - A token that can be passed with each API call.</li>
  <li><strong>api secret</strong> - A second token, that can be passed with each API call.</li>
</ul>

<p>Many API providers just automatically issue these API keys when each account is created, allowing consumers to possibly reset and regenerate at any point. These keys are more about identification than they are about security, as each key is passed along with each API call, and provide identification via API logging, which I’ll cover in a separate post. The only security keys deliver is that API calls are rejected if keys aren’t present.

<p><strong>Allow For Multiple Applications</strong>
Other API providers will go beyond this base level of API account functionality, allowing API consumers to possibly generate multiple sets of keys, sometimes associated with one or many applications. This opens up the question of whether these keys should be associated with the account, or with one or many registered applications:

<ul>
  <li><strong>app id</strong> - A unique id for the application.</li>
  <li><strong>app name</strong> - A name for the application.</li>
  <li><strong>app description</strong> - A description of the application.</li>
  <li><strong>api key</strong> - A token that can be passed with each API call.</li>
  <li><strong>api secret</strong> - A second token, that can be passed with each API call.</li>
</ul>

<p>Allowing for multiple applications isn’t something every API provider will need, but does reduce the need for API consumers to signup for multiple accounts, when they need an additional API key for a separate application down the road. This is something that API providers should be considering early on, reducing the need to make additional changes down the road when needed. If it isn’t a problem, there is no reason to introduce the complexity into the API management process.

<p>This post doesn’t even touch on logging and usage. It is purely about establishing developer accounts, and providing what they’ll need to authenticate and identify themselves when consuming API resources. Next I’ll explore the usage, consumption, and billing side of the equation. I’m trying to keep things decoupled as much as I possibly can, as not every situation will need every element of API management. It helps me articulate all the moving parts of API management for my readers, and customers, and allows me to help them make sensible decisions, that they can afford.

<p>Ideally, developer accounts are not a separate thing from any other website, web or mobile application accounts. If I had my way, API developer accounts would be baked into the account management tools for all applications by default. However, I do think things should be distilled down, standardized, and kept simple and modular for API providers to consider carefully, and think about deeply when pulling together their API strategy, separate from the rest of their operations. I’m taking the thoughts from this post and applying in one project I’m deploying on AWS, with another that will delivered by custom deploying a solution that leverages Github, and basic Apache web server logging. Keeping the approach standardized, but something I can do with a variety of different services, tools, and platforms.


