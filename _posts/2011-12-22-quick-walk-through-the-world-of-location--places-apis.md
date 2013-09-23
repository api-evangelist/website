---
layout: post
title: "Quick Walk Through the World of Location & Places APIs"
url: 'http://apievangelist.com/2011/12/22/quick-walk-through-the-world-of-location-&-places-apis/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/local-search-map-pin.png'
---

[<img src="http://kinlane-productions.s3.amazonaws.com/hyp3rl0cal/local-search-map-pin.png" alt="" width="150" align="right" />][1]

**[Photo Credits**][1]

I took a walk through what I am calling the locations and places API landscape today. Most of these APIs I’m familiar with, but as the [CityGrid API Evangelist][2], I’m getting an opportunity to immerse myself into this new local, social mobile world.

As I immerse myself in this semi-new world I want to share my findings with everyone else.  If you have any suggestions make sure and let me know in comments below.

First I started with **[CityGrid APIs][3]**, which provide several key location and places APIs:
[<img src="http://kinlane-productions.s3.amazonaws.com/citygrid/citygrid_logo_200.png" alt="" width="150" align="right" />][4]

  * **The Places API** - Provides functionality for information on local businesses, including search, detail, user content submission, and predictive text
  * **The Offers API** - Provides coupons and special offers from businesses based on geography and category
  * **The Reviews API** - Provides access to customer reviews for businesses selected by id or by geography or category

Then I wanted to see what Google was doing, and of course started with the **[Google Maps APIs][5]:**
[<img src="http://kinlane-productions.s3.amazonaws.com/google/Google-Maps-Logo.jpg" alt="" width="100" align="right" />][6]

  * **Maps JavaScript API** - The Google Maps Javascript API lets you embed Google Maps in your own web pages
  * **Maps Image API** - The Google Maps Image APIs make it easy to embed a static Google Maps image or Street View panorama into your web page, with no need for JavaScript

Along with Google Maps they offer a set of **[Geo Web Services][7]** that contain several location and places based APIs:

  * **Directions API** - The Google Directions API is a service that calculates directions between locations
  * **Distance Matrix API** - The Google Distance Matrix API is a service that provides travel distance and time for a matrix of origins and destinations.
  * **Elevation API** - The Google Elevation API provides you an interface to query locations on the earth for elevation data.
  * **Geocoding API** - Geocoding is the process of converting addresses into geographic coordinates
  * **Places API** - The Google Places API is a service that returns information about places, defined as establishments, geographic locations, or prominent points of interest

Already with **[CityGrid][8]** and Google I’m seeing that the type of location and places services, really start to get complicated and diverse. With **[Google Latitude][9]** I start separating the location from the place, with what are two location specific APIs:[<img src="http://kinlane-productions.s3.amazonaws.com/google/google_latitude_icon.jpeg" alt="" width="100" align="right" />][9]

  * **Curent locations** - Represents the user's most recent known location
  * **Location history** - Represents the list of all recorded user locations

After Google I have to look at another big player, ****

   [1]: http://www.designdelux.com/
   [2]: http://www.citygridmedia.com/developer/blog/citygrid-api-evangelist/ (CityGrid API Evangelist)
   [3]: http://developer.citygridmedia.com/ (CityGrid APIs)
   [4]: http://developer.citygridmedia.com/
   [5]: http://code.google.com/apis/maps/index.html (Google Maps API)
   [6]: http://code.google.com/apis/maps/
   [7]: http://code.google.com/apis/maps/documentation/geocoding/ (Geo Web Services)
   [8]: http://www.citygrid.com/ (CityGrid)
   [9]: http://code.google.com/apis/latitude/
