---
layout: post
title: "The Flora and Fauna of the Twitter Ecosystem"
url: 'http://apievangelist.com/2012/05/07/the-flora-and-fauna-of-the-twitter-ecosystem/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/Field-Guide-Tweets.png'
---

<img src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/twitter/Field-Guide-Tweets.png" alt="" width="150" align="right" />

Twitter has an innovative approach to presenting the objects that make up the Twitter Platform. They have built a [field guide to Twitter Platform objects][1], designed like an [Audubon Society][2] field guide, describing the four primaty Twitter objects:

  * **Tweets** - Also known as a Status Update, Tweets are the basic atomic unit of all things Twitter. Users [create Tweets][3]. Tweets can be [embedded][4], [replied to][3], [favorited][5], [unfavorited][6], [retweeted][7], [unretweeted][8] and [deleted][8].
  * **Users** - Users can be anyone or anything. They [tweet][3], [follow][9], [create lists][10], have a [home_timeline][11], can be [mentioned][12], and can be[looked up][13] in bulk.
  * **Entities** - Entities provide metadata and additional contextual information about content posted on Twitter. Entities are never divorced from the content they describe. After May 14th, 2012 [Tweet Entities][14] will be returned wherever [Tweets][15] are found in the API. Entities are instrumental in [resolving URLs][16].
  * **Places** - Places are specific, named locations with corresponding geo coordinates. They can be attached to [Tweets][15] by specifying a `place_id` when [tweeting][3]. Tweets associated with places are not necessarily issued from that location but could also potentially be _about_ that location. [Places][17] can be [created][18] and [searched for][19]. Tweets can also be [found][20] by place_id.

It is a creative way to educate users about the Twitter API, making it more visually appealing. Beyond that, I'm not sure it helps developers get up and running using the API, but who knows...it might make it more accessible to some users.

Have you seen any other creative wasy of displaying API documentaton?




   [1]: https://dev.twitter.com/docs/platform-objects (field guide to Twitter Platform objects)
   [2]: http://www.audubon.org/ (Audubon Society)
   [3]: https://dev.twitter.com/docs/api/1/post/statuses/update
   [4]: https://dev.twitter.com/docs/embedded-tweets
   [5]: https://dev.twitter.com/docs/api/1/post/favorites/create/:id
   [6]: https://dev.twitter.com/docs/api/1/post/favorites/destroy/:id
   [7]: https://dev.twitter.com/docs/api/1/post/statuses/retweet/:id
   [8]: https://dev.twitter.com/docs/api/1/post/statuses/destroy/:id
   [9]: https://dev.twitter.com/docs/api/1/post/friendships/create
   [10]: https://dev.twitter.com/docs/api/1/post/lists/create
   [11]: https://dev.twitter.com/docs/api/1/get/statuses/home_timeline
   [12]: https://dev.twitter.com/docs/api/1/get/statuses/mentions
   [13]: https://dev.twitter.com/docs/api/1/get/users/lookup
   [14]: https://dev.twitter.com/docs/tweet-entities
   [15]: https://dev.twitter.com/docs/platform-objects/tweets
   [16]: https://dev.twitter.com/docs/tco-url-wrapper
   [17]: https://dev.twitter.com/docs/api/1/get/geo/id/:place_id
   [18]: https://dev.twitter.com/docs/api/1/post/geo/place
   [19]: https://dev.twitter.com/docs/api/1/get/geo/search
   [20]: https://dev.twitter.com/docs/places/finding-tweets-about-places
