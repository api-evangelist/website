---
layout: post
title: "Module Exposes Drupal Resources as RESTful API"
url: 'http://apievangelist.com/2011/01/29/360/'
image: ''
---

A [new Drupal module][1] makes use of the [Drupal Entity API][2] and then takes information about the entity and delivers it as a [Restful][3] [Web Service][4].

Features are:<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/drupal-logo.jpg" alt="" width="200" align="right" />

  * RESTful compliant
  * Support for all Drupal entity types
  * Provides create, read, update and delete (CRUD) operations
  * Service endpoints are automatically generated for each entity
  * JSON response format
You can [download the module on Github][5], but it is also synchronized to the [Drupal.org CVS][6].

This module allows Drupal owners to immediately deliver a RESTful API from their existing Drupal site and can also be used by developers looking to quickly deliver an API can build it using the Drupal platform.

   [1]: http://drupal.org/project/restws
   [2]: http://drupal.org/project/entity
   [3]: http://www.kinlane.com/
   [4]: http://www.apievangelist.com/
   [5]: http://github.com/klausi/restws
   [6]: http://drupal.org/node/36662
