---
layout: post
title: 'Beyond the Social Experiment Jonathans Card is the New Gift Card Economy'
url: 'http://apievangelist.com2011/09/10/beyond-the-social-experiment,-jonathans-card-is-the-new-gift-card-economy/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/starbucks-gift-card-300x229.jpg'
---
{% include JB/setup %}
<p>
     <a href="https://www.starbucks.com/card" target="_blank"><img src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/Jonathans-Card/starbucks-gift-card-300x229.jpg"  width="250" align="right" /></a>I followed the <a title="Jonathans Card Social Experiment" href="http://jonathanstark.com/card/">Jonthan’s Card Socal Experiment</a> closely. The whole time I had an entry on my to do list, to write a story about it. I never successfully found an angle I could get behind, then <a title="Audrey Watters" href="http://www.hackeducation.com">Audrey</a> said, “Why don’t you just write about he tech behind it?”.
</p>
<p>
     Great idea! Jonathan’s Card is interesting as a social or marketing experiment, but I am more interested in the technology that was used to make it happen, not just the social experiment.
</p>
<p>
     It all starts with an image of Jonathan’s Starbucks Card. But it took the mobility of the smart phone to be able to display the image of his sard and purchase a coffee at your local Starbucks.
</p>
<p>
     An image and your smart phone are essential technology in this experiment, but none of this would be possible without the <a href="https://www.starbucks.com/card" target="_blank">Starbucks Card program</a>. Starbucks allows anyone to purchase and add money to the balance of the card as long as you know the card number, and the site also allows you to see charges made against the card.
</p>
<p>
     <a href="http://jonathanstark.com/card/" target="_blank"><img src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/Jonathans-Card/jonathans-card-image.png"  width="200" align="right" /></a>The Starbucks Card is the central ingredient in this experiment, but Twitter also plays an important role. Jonathan uses Twitter as a central messaging channel, and ultimately an API for the Johnathan’s Card Experiment. He wrote a bot that scrapes the Starbucks site for the card balance and posts it to Twitter, whenever anything is charged to the Starbucks Card.
</p>
<p>
     Twitter is also being used by the community participating in this “social experiment”. Twitter allows them to tweet at @jonathanscard adding to the Twitter data stream. Also, some innovative developer particpated by adding graphing apps on top of the @jonathanscard Twitter stream, that provided visualisations for the experiment.
</p>
<p>
     Additionally, to provide easier access for developers, Jonathan whipped up a simple read only API providing insight into the experiment in the following ways:
</p>

