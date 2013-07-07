---
layout: post
title: Pinboard API Tax Proposal
url: http://apievangelist.com2013/03/15/pinboard-api-tax-proposal/
source: http://apievangelist.com2013/03/15/pinboard-api-tax-proposal/
domain: apievangelist.com2013
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/pinboard-icon.png
---
{% include JB/setup %}<p>
     <a href="https://pinboard.in" target="_blank"><img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/pinboard/pinboard_in_blue.png"  width="200" align="right" /></a>
</p>
<p>
     Maciej Ceglowskiis, the founder of popular social bookmarking platform <a href="https://pinboard.in">Pinboard</a>,made an <a href="https://groups.google.com/d/msg/pinboard-dev/PidYOmyBaxI/mLDKIzC6olgJ" target="_blank">interesting proposal over on the Pinboard Google Group</a>:
</p>
<p>
     <em>I've been thinking about imposing an API tax, the proceeds of which would go into improving API infrastructure and offsetting operating costs, structured along these lines:</em>
</p>
<ul>
     <li>
          <em>API free to use for your own Pinboard account</em>
     </li>
     <li>
          <em>Every API client making requests on behalf of someone else must register an app identifier</em>
     </li>
     <li>
          <em>$20/year tax if your app makes requests for over 100 Pinboard accounts</em>
     </li>
     <li>
          <em>$100/year tax if your app makes requests for over 1000 Pinboard accounts</em>
     </li>
     <li>
          <em>Possibly additional price levels to waive certain rate limits</em>
     </li>
</ul>
<p>
     <em>Think of it as a road tax that then pays for further construction, repair, and people in orange vests.</em>
</p>
<p>
     I’m guessing that Maciej has a lot of experience to back his proposal, watching how developers use Pinboard for their own purposes, or on behalf of a user via a client. I heavily depend on Pinboard for my curation at API Evangelist, so API access would remain free for me. I’m not sure how I would feel if I was building a client.
</p>
<p>
     On the forum, there is very interesting feedback from Matt Schmidt, developer of <a href="https://play.google.com/store/apps/details?id=com.pindroid">PinDroid</a>, the leading Pinboard client for Android:
</p>
<p>
     <em>I'm very much against this. Why would you tax the makers of the apps that help drive use of your product, rather than the users themselves? To extend your road use tax analogy, this is like taxing the car companies for their customer's use of the roads.</em>
</p>
<p>
     <em>I offer PinDroid as a free, open source app and have no interest in making money off it, but I also have no interest in losing money on it. Why not offer api access as a premium account feature (like archiving) for an extra buck instead?</em>
</p>
<p>
     <em>To be clear, if such a "tax" were to be implemented, I will have to stop developing and supporting PinDroid and take it off the market.</em>
</p>
<p>
     Matt provides some real life feedback, that I can’t. PindDroid is a vital player in the PinBoard ecosystem, that could be hurt by such a tax. Free and open source code and clients are a vital aspect of any API ecosystem, you definitely want to understand how this layer will be affected by such a tax.
</p>
<p>
     <a href="https://play.google.com/store/apps/details?id=com.pindroid"><img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/pinboard/pindroid.png"  width="500" /></a>
</p>
<p>
     Maciej just made this proposal today, so the conversation is fresh. Head over to the <a href="https://groups.google.com/d/msg/pinboard-dev/PidYOmyBaxI/mLDKIzC6olgJ" target="_parent">Pinboard Google Group</a> to weigh in. I’ll post another story after the conversation dies down, providing more thoughts about API taxes.
</p>
<p>
     Thanks Marsh (<a href="https://twitter.com/earth2marsh" target="_blank">@earth2marsh</a>) for alerting me to the conversation!
</p>
