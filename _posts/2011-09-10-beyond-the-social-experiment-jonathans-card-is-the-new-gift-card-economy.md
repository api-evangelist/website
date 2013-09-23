---
layout: post
title: "Beyond the Social Experiment Jonathans Card is the New Gift Card Economy"
url: 'http://apievangelist.com/2011/09/10/beyond-the-social-experiment-jonathans-card-is-the-new-gift-card-economy/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/starbucks-gift-card-300x229.jpg'
---

[<img src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/Jonathans-Card/starbucks-gift-card-300x229.jpg" alt="" width="250" align="right" />][1]I followed the [Jonthan’s Card Socal Experiment][2] closely. The whole time I had an entry on my to do list, to write a story about it. I never successfully found an angle I could get behind, then [Audrey][3] said, “Why don’t you just write about he tech behind it?”.

Great idea! Jonathan’s Card is interesting as a social or marketing experiment, but I am more interested in the technology that was used to make it happen, not just the social experiment.

It all starts with an image of Jonathan’s Starbucks Card. But it took the mobility of the smart phone to be able to display the image of his sard and purchase a coffee at your local Starbucks.

An image and your smart phone are essential technology in this experiment, but none of this would be possible without the [Starbucks Card program][1]. Starbucks allows anyone to purchase and add money to the balance of the card as long as you know the card number, and the site also allows you to see charges made against the card.

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/Jonathans-Card/jonathans-card-image.png" alt="" width="200" align="right" />][4]The Starbucks Card is the central ingredient in this experiment, but Twitter also plays an important role. Jonathan uses Twitter as a central messaging channel, and ultimately an API for the Johnathan’s Card Experiment. He wrote a bot that scrapes the Starbucks site for the card balance and posts it to Twitter, whenever anything is charged to the Starbucks Card.

Twitter is also being used by the community participating in this “social experiment”. Twitter allows them to tweet at @jonathanscard adding to the Twitter data stream. Also, some innovative developer particpated by adding graphing apps on top of the @jonathanscard Twitter stream, that provided visualisations for the experiment.

Additionally, to provide easier access for developers, Jonathan whipped up a simple read only API providing insight into the experiment in the following ways:

  * **Balances** \- Returns the card balance for every minute of the day
  * **Latest Activity** \- Returns the most recent card balance with a timestamp indicating when it was retrieved. Under normal circumstances, the balance will be less than a minute old.
  * **Changes** \- Returns balance changes with delta amounts.
  * **Summary** \- Returns aggregate numbers.

I don’t know about you I see a model for gift card providers to take advantage of when it comes to their gift card programs.  So I took a quick look at the gift card landscape, and immediately you have all the big retail players:

  * [Amazon Gift Cards][5]
  * [Walmart][6]
  * [Target][7]
  * [Best Buy][8]

Since a gift card is just another version of a credit card, the leading credit card companies have gift cards:

  * [Prepaid Visa][9]
  * [American Express][10]

Then there are a couple gift card only sites, providing access to existing gift card programs and private label and custom git cards:

  * [GitCards.com][11]
  * [Gift Card Mall][12]

It is clear when you walk into any grocery store, that gift cards are here to stay, and are a new part of our economy. Jonathans card is more a demonstration of how technology like Twitter, smart phones and APIs can be added to gift cards, and create a more social and mobile gift card economy.

Think how this experiment would work in more trusted and closed situations, like your son or daughter going to college and the entire family, including grandparents, aunts and uncles can contribute to a relatives life using gift cards, Twitter, APIS and their smart phone.

   [1]: https://www.starbucks.com/card
   [2]: http://jonathanstark.com/card/ (Jonathans Card Social Experiment)
   [3]: http://www.hackeducation.com (Audrey Watters)
   [4]: http://jonathanstark.com/card/
   [5]: http://www.amazon.com/gp/gc (Amazon Gift Cards)
   [6]: http://www.walmart.com/cp/Gift-Cards/96894 (Walmart)
   [7]: http://www.target.com/c/GiftCards/-/N-5xsxu (Target)
   [8]: http://www.bestbuy.com/site/Electronics/Gift-Cards/cat09000.c?id=cat09000 (Best Buy)
   [9]: http://usa.visa.com/personal/cards/prepaid/visa_gift_card.html (Prepaid Visa)
   [10]: https://www.americanexpress.com/gift-cards/ (American Express Gift Cards)
   [11]: http://www.giftcards.com/ (GiftCards.com)
   [12]: https://www.giftcardmall.com/ (Gift Card Mall)
