---
layout: post
title: "iCloud Storage APIs"
url: 'http://apievangelist.com/2011/06/08/icloud-storage-apis/'
image: ''
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/apple/iCloud-Steel.jpg" alt="" width="150" align="right" />[iCloud][1] storage APIs allow IOS application developers to store documents and other data to a central location so userscan view or edit from any device without having to sync or transfer files.

There are two ways that applications can take advantage of iCloud storage:

  * Document Storage - Enabling storage and sharing of information in document form.
  * Key-Value Data Storage - Enabling storage and sharing small amounts of data.
Most applications will use iCloud document storage to share documents, which is a feature that users think of when they think of cloud storage. Users care about whether photos, videos, and documents are accessible across devices while the key-value data store is not something a user would never see.

Key-value storage will be used for small amounts of data such as storing application state, settings, and other important information that delivers a better user experience. Although not as apparent to the end-user, key-value storage will be just as important as document storage.

<img class="aligncenter c1" src="http://kinlane-productions.s3.amazonaws.com/apple/iCloud-Storage-APIs.png" alt="" width="550" align="center" />

All iCloud storage is managed centrally by the iCloud service, which handles coordination of documents and key-value stores. The iCloud service handles storage searches, change notifications, version control, conflicts, and security for applications that integrate with a user's iCloud storage account.

Neither document storage or key-value storage in the cloud are anything new. But when it is implemented as part of the IOS platform, it becomes much bigger. Apple is solving everyday problems users face when using their smart phones, by storing data centrally in the cloud.

ICloud APIs will enable developers to build rich applications on the IOS platform, and continue to grow IOS market share.

######  Related articles

  * [Apple iCloud API][2] (apievangelist.com)
  * [iCloud Storage APIs][3] (kinlane.com)
  * [Documents in the Cloud with Apple iCloud][4] (kinlane.com)

   [1]: http://www.apple.com/icloud/ (iCloud)
   [2]: http://blog.apievangelist.com/2011/06/06/apple-icloud-api/
   [3]: http://www.kinlane.com/2011/06/icloud-storage-apis/
   [4]: http://www.kinlane.com/2011/06/documents-in-the-cloud-with-apple-icloud/
