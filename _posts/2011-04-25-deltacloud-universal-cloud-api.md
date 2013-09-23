---
layout: post
title: "Deltacloud Universal Cloud API"
url: 'http://apievangelist.com/2011/04/25/deltacloud-universal-cloud-api/'
image: ''
---

<img class="alignnone c1" title="DeltaCloud" src="http://kinlane-productions.s3.amazonaws.com/cloud-computing/DeltaCloud.PNG" alt="" width="172" height="54" align="right" />I'm spending time going through [RedHat's][1] [Deltacloud set of cloud APIs][2]. They recently recently moved the project to the [Apache Incubator][3] and submitted it to the [Distributed Management Task Force][4] (DMTF) .

With the [Deltacloud API][2] you can start an instance on an internal cloud, then with the same code start another on [Amazon EC2][5] or [Rackspace][6]. This seems like the closest thing we have at the moment, to a true [cloud API standard][7].

Deltacloud Core provides:

  * REST API
  * Backward compatibility across versions
Deltacloud Aggregator provides a web UI in front of the Deltacloud API. With Deltacloud Aggregator, you can:
  * View image status and stats across clouds, all in one place
  * Migrate instances from one cloud to another
  * Manage images locally and provision them on any cloud
[Deltacloud API][8] and Aggregator are free and open source and support the following providers:

  * [Amazon EC2][5]
  * [GoGrid][9]
  * [OpenNebula][10]
  * [Rackspace][6]
  * [RHEV-M][11]
  * [RimuHosting][12]
They will also soon be supporting:
  * [Terremark][13]
  * [vCloud][14]
They offer up a [Ruby Gem for download][15]. I will have to get a new environment up and running so I can play with. The ability to manage resources across multiple cloud providers and allowing for instance portability is very important to me. Hopefully I can get time to play with more.

   [1]: http://www.redhat.com/
   [2]: http://deltacloud.org/
   [3]: http://incubator.apache.org/deltacloud/index.html
   [4]: http://www.dmtf.org/
   [5]: http://aws.amazon.com/ec2/
   [6]: http://www.rackspace.com/
   [7]: http://www.kinlane.com/2010/06/cloud-storage-api-standard/
   [8]: http://deltacloud.org/index.html
   [9]: http://www.gogrid.com/
   [10]: http://www.opennebula.org/
   [11]: http://www.redhat.com/virtualization/rhev/desktop/rhevm/
   [12]: http://rimuhosting.com
   [13]: http://www.terremark.com/
   [14]: http://www.vmware.com/solutions/cloud-computing/
   [15]: http://deltacloud.org/download.html
