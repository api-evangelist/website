---
published: true
layout: post
title: >-
  Locking Up Any Open Data Taxonomy Is Short Sighted In Todays Online
  Environment
date: 2017-11-12T13:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Licensing
  - HSDA
  - City Government
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/open-referral/211tax.png'
---
<p><a href="https://211taxonomy.org/"><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/open-referral/211tax.png" align="right" width="40%" style="padding: 15px;" /></a></p>I published a taxonomy API as part of my Human Services Data API (HSDA) work recently, and as part of the work I wanted it to support a handful of the human services taxonomies available currently. The most supported taxonomy available out there is [the AIRS/211 LA County Taxonomy](https://211taxonomy.org/). It is a taxonomy in use by 211 of LA County, as well as owned and licensed by them. From what I gather, it is the most common format in use, and [you can find licensing pages for it from other municipal 211 providers](http://211wny.org/index.php/airs-license). Before you can download a copy of the taxonomy you have to agree to the license I've posted at the bottom of this post, something I was unwilling to do.

Taxonomies shouldn't be locked up this way. Let alone taxonomies for use in open data, helping citizens at the municipal level. I understand that 211 LA will argue that they've put a bunch of work into the schema, and therefore they want to protect what they view their intellectual property, but in 2017 this is wrong. This isn't the way things should be done, sorry. The AIRS taxonomy should be openly available, and reusable in a machine readable format, and evolved by an open governance process. There is no reason for this valuable taxonomy, that has the potential to make our cities better, should be locked up like this--it needs to be widely used, and adopted without any legal friction along the way.

I understand that it takes work, and resources to keep a taxonomy meaningful, and usable, but we should not stand in the way of people finding human services, and restricting 211 providers from using the same vocabulary. There are other was to generate revenue, and evolve forward a taxonomy in an online, collaborative environment, much like we are currently doing with open source software. This kind of stuff drives me nuts, and the licensing around this important technology is something I'll keep an eye on, and contributing whatever I can to help stimulate the discussion in favor of open sourcing. In the absence of AIRS, I have adopted [an open source 211 taxonomy called Open Eligibility](https://github.com/auntbertha/openeligibility), but alas it seems like an effort that has gone dormant. [I have forked the specification](https://github.com/human-services/openeligibility), added more simpler JSON, CSV, and JSON formats which I will be working with it alongside the rest of [my Human Services Data API (HSDA) taxonomy work](http://developer.open.referral.adopta.agency/#HSDA Taxonomy).

Taxonomy licensing is another area of consideration I'll add to [my API licensing research](http://licensing.apievangelist.com/), as well as for guidance around my HSDA work. I wish this type of stuff didn't still happen in 2017. It is a relic of another time, and in a digital age, taxonomies for any aspect of public infrastructure should be openly licensed, and reusable by everyone. I would like to see [Open Referral](http://openreferral.org/) expand its portfolio to push forward one or more taxonomies for not just human services, but also organizations, locations, and potentially other relevant schema we are pushing forward. I see Open Referral as an incubator for schema, OpenAPI definitions, as well as datasets like 211 taxonomy, helping provide a commons where 211 organizations can find what they need. 

<hr />

TAXONOMY SUBSCRIPTION AGREEMENT

CAREFULLY READ THIS TAXONOMY SUBSCRIPTION AGREEMENT BEFORE DOWNLOADING, INSTALLING OR USING THE TAXONOMY (DEFINED BELOW). TAKING ANY STEP TO DOWNLOAD, INSTALL OR USE THE TAXONOMY IN ANY WAY CONSTITUTES YOUR ASSENT TO AND ACCEPTANCE OF THIS AGREEMENT AND IS A REPRESENTATION BY YOU THAT YOU HAVE THE AUTHORITY TO ASSENT TO AND ACCEPT THIS AGREEMENT. IF YOU DO NOT AGREE WITH THE TERMS AND CONDITIONS OF THIS AGREEMENT, YOU MUST NOT DOWNLOAD, INSTALL OR USE THE TAXONOMY AND YOU MUST IMMEDIATELY RETURN THE TAXONOMY (AND NOT KEEP ANY COPIES) TO 211 LA AND SO NOTIFY 211 LA OF SUCH FAILURE TO AGREE.

Taxonomy Subscription Agreement ("Agreement") contains the terms and conditions by which Information and Referral Federation of Los Angeles, Inc., doing business as 211 of LA County ("211 LA") provides a subscription license to use the Taxonomy. This Agreement is a binding legal contract between you (both the individual downloading, installing and/or using the Taxonomy and, if applicable, the legal entity on behalf of which such individual is acting) ("Subscriber") and 211 LA.

1.Definitions

Subscriber Database means a database of health and human services information and resources that is created and maintained by Subscriber.

Subscriber Directory means a printed directory or electronic read-only directory of health and human services that is created and maintained by Subscriber using a Subscriber Database. As used in this definition, "read-only" means an electronic version of a directory in which the information in such directory, including the Taxonomy, cannot be modified or altered in any way.

Subscription Order Form means the form(s) used by 211 LA for allowing subscribers to purchase or renew subscription licenses of the Taxonomy.

Taxonomy means the Taxonomy of Human Services maintained and made generally available by 211 LA for purposes of indexing health and human services information and resources, including its terms, definitions, codes and references and any and all updates, upgrades, enhancements or other modifications that may be made available by 211 LA to Subscriber from time to time.

Taxonomy Website means a website hosted by 211 LA through which subscription licenses for the Taxonomy can be purchased and the Taxonomy can be downloaded.

2.Taxonomy License.

Limited License. Subject to Subscriber's compliance with the terms and conditions of this Agreement (including, without limitation, Sections 2.2, 2.3, 3 and 4), 211 LA hereby grants to Subscriber a limited, non-exclusive, non-transferable, non-sublicensable license to:

access portions of the Taxonomy Website designated by 211 LA for subscribers and download the Taxonomy as made generally available thereon;

use the Taxonomy, including its codes, terms, definitions, and references, as a classification structure for indexing health and human services information and resources in a Subscriber Database;

include Taxonomy terms in a survey instrument prepared by Subscriber as reasonably necessary to collect information from third party organizations regarding health and human services, provided that such survey instrument may only include the Taxonomy terms that Subscriber has used to index health and human services information and resources in the Subscriber Database;

include Taxonomy terms as an index in a Subscriber Directory distributed or otherwise made available to third parties (including over the Internet), provided that (i) the proceeds of any monetary or other consideration provided in connection with such distribution are provided to a non-profit, charitable organization and (ii) any such Subscriber Directory may only include the Taxonomy terms that Subscriber has used to index health and human services information and resources in the Subscriber Database, along with any higher level terms on the same branch that are needed to display the hierarchical structure; and

include the Taxonomy definitions in the Subscriber Directory referenced in Section 2.1(d) above, provided that such Subscriber Directory may include only those definitions for terms that Subscriber has used to index health and human services information and resources in the Subscriber Database.

License Restrictions. Nothing contained in this Agreement will be construed as conferring upon Subscriber, by implication, operation of law or otherwise, any license or other rights except as expressly set forth in Section 2.1. Subscriber shall not, and shall not allow any third party to: (i) copy, display or otherwise use all or any portion of the Taxonomy except as incorporated into a Subscriber Directory as permitted in Section 2.1; (ii)  transmit or otherwise distribute the Taxonomy (or any portion of the Taxonomy) as a separate product, module or material to any end user or other third party, or make the Taxonomy (or any portion of the Taxonomy) available to any end user or other third party as a downloadable file separate from a Subscriber Directory; (iii) transmit or otherwise distribute any portion of the Taxonomy for commercial purposes or otherwise for profit or other monetary gain; (iv) incorporate the Taxonomy (or any portion of the Taxonomy) into any database or software through which the Taxonomy (or any portion of the Taxonomy) can be printed, downloaded or modified; or (v) loan, lease, resell, sell, offer for sale, sublicense, adapt, translate, create derivative works of or otherwise modify or alter all or any part of the Taxonomy. Further, Subscriber acknowledges and agrees that use of the Taxonomy Website is also subject to 211 LA's Terms of Use, as made available thereon and updated from time to time.

Notice.

If the Taxonomy, or any potion of the Taxonomy (including its terms, codes, definitions or references), are utilized in a Subscriber Directory that is published, transmitted, distributed or otherwise made available to third parties, by any means or medium, the Subscriber shall prominently display the following notice in such directory:

Copyright © 1983-2007, Information and Referral Federal of Los Angeles County, Inc. All rights reserved. The index, codes and definitions of the terms contained herein are the intellectual property of Information and Referral Federal of Los Angeles, Inc. and are protected by copyright and other intellectual property laws. No part of this listing of human services terms and definitions may be reproduced, stored in a retrieval system, or transmitted in any form or by any means, electrical, mechanical, photocopying, recording or otherwise without the prior written permission of the Information and Referral Federal of Los Angeles County, Inc.

If the Taxonomy is displayed or otherwise made available in a Subscriber Directory via the Internet, Subscriber shall prominently include a link to a copyright acknowledgement statement that 211 LA maintains online, currently located at: http://www.211la.org/Content.asp?Content=Taxonomy&SubContent=Copyright.

3.Intellectual Property Ownership.

Ownership of the Taxonomy. As between 211 LA and Subscriber, 211 LA retains and shall own all right, title and interest in and to the Taxonomy and any derivative works or other modifications thereof, including, without limitation, all copyright, trademark, trade secret and other intellectual rights, subject only to the limited license set forth herein. Subscriber does not acquire any other rights, express or implied, in the Taxonomy. Subscriber hereby assigns, and agrees to assign, to 211 LA all right, title and interest (including all intellectual property rights) throughout the world that Subscriber has or may have in the Taxonomy (including with respect to any modifications suggested by, or other contributions made by, Subscriber), which assignment shall be deemed effective as to any future modifications or contributions immediately upon the creation thereof. Subscriber further irrevocably waives any "moral rights" or other rights with respect to attribution of authorship or integrity of any modifications suggested by, or other contributions made by, Subscriber under any applicable law under any legal theory.

Access and Security.

Subscriber is solely responsible for providing, installing and maintaining at Subscriber's own expense all equipment, facilities and services necessary to access and use the Taxonomy, including, without limitation, all computer hardware and software, modems, telephone service and Internet access.

Subscriber may be issued or otherwise assigned a user identification and/or password (collectively, "User Identifications ") to access the Taxonomy and/or Taxonomy Website as permitted hereunder. Subscriber is solely responsible for tracking all use of the User Identifications and for ensuring the security and confidentiality of all User Identifications. Subscriber acknowledges that Subscriber is fully responsible for all liabilities incurred through the use of any User Identification and that any download, transmission or transaction under a User Identification will be deemed to have been performed by Subscriber.

Subscriber shall ensure that each of its employees complies with this Agreement, including, without limitation, the license restrictions in Section 2.2 and shall protect the Taxonomy from any use that is not permitted under this Agreement. Subscriber shall promptly notify 211 LA of any unauthorized copying, display, modification, transmission, distribution, or use of the Taxonomy of which it becomes aware.

211 LA reserves the right at any time and without prior notice to Subscriber to change the hours of operation of the Taxonomy Website or to limit Subscriber's access to the Taxonomy (i) in order to perform repairs or to make updates, upgrades, enhancements or other modifications or (ii) in response to unforeseen circumstances or circumstances beyond 211 LA's reasonable control. 211 LA may add or withdraw elements of to or from the Taxonomy and/or Taxonomy Website from time to time in its sole discretion, although Subscriber acknowledges and agrees that 211 LA has no obligation to maintain or provide any updates, upgrades, enhancements, or other modifications to the Taxonomy or Taxonomy Website.

Verification. 211 LA may, during the term of this Agreement and with seven (7) days prior notice, request and gain access to Subscriber's premises for the limited purpose of conducting an inspection to determine and verify that Subscriber is in compliance with the terms and conditions hereof. Subscriber shall promptly grant such access and cooperate with 211 LA in the inspection; provided, however, the inspection shall be conducted in a manner not intended to disrupt unreasonably Subscriber's business and shall be restricted in scope, manner and duration to that reasonably necessary to achieve its purpose.

4.Payment

Payment. In consideration for the subscription license granted under Section 2.1, Subscriber shall pay the applicable fees as set forth in the Subscription Order Form and/or Taxonomy Website. All fees are nonrefundable. Any information that you may provide in connection with obtaining the subscription (including any nonprofit and/or AIRS membership information) may be verified and your subscription license may be placed on hold or terminated in the event of inaccuracies or discrepancies.

Taxes. In addition to all applicable fees, Subscriber shall pay all sales, use, personal property and other taxes resulting from this Agreement or any activities under this Agreement, excluding taxes based on 211 LA's net income, unless Subscriber furnishes proof of exemption from payment of such taxes in a form reasonably acceptable to 211 LA. Further, If Subscriber is required by law to deduct or withhold any taxes, levies, imposts, fees, assessments, deductions or charges from or in respect of any amounts payable hereunder, (a) Subscriber shall pay the relevant taxation authority the minimum amounts necessary to comply with the applicable law, (b) Subscriber shall make such payment prior to the date on which interest or penalty is attached thereto, and (c) the amounts payable hereunder shall be increased as may be necessary so that after Subscriber makes all required deductions or withholdings, 211 LA shall receive amounts equal to the amounts it would have received had no such deductions or withholdings been required.

Discounts. From time to time, and in 211 LA's sole discretion, 211 LA may offer discounts to particular organizations (such as nonprofits, government agencies and members of the Alliance of Information and Referral Systems (AIRS)). If such a discount is offered to Subscriber, Subscriber may be required to submit proof of nonprofit status (such as a federal EIN number), a valid AIRS membership number and/or additional information in order to receive such discounts.

Delivery. The Taxonomy is only made available electronically via download from the Taxonomy Website and, unless otherwise agreed by 211 LA in writing on a case-by-case basis, will not be delivered in any other form or via in any other method.

5.Term and Termination

Term. Subscriber's rights with respect to the Taxonomy will commence on the date full payment of license fees are received and approved by 211 LA and will continue for an initial period of one (1) year, at which point Subscriber's rights and this Agreement shall expire. If available, Subscriber may renew its subscription license via the Taxonomy Website, which renewal will be subject to and governed by 211 LA's then-current fees and then-current terms and conditions (which may include a new or updated Taxonomy Subscription Agreement).

Termination of Agreement. Subscriber may terminate this Agreement at any time by sending an email message addressed to taxonomy@infoline la.org, with the subject "Subscription Cancellation." Further, if Subscriber commits any breach of any provision of this Agreement, 211 LA will have the right to terminate this Agreement (including the rights granted to Subscriber under 2.1) by written notice, unless Subscriber remedies such breach to 211 LA's reasonable satisfaction within thirty (30) calendar days after receiving written notice from 211 LA.

Effect of Termination.

Upon termination or expiration, and except as expressly provided in Section 5.3(b), the rights and license granted to Subscriber hereunder shall immediately cease and Subscriber will immediately cease all use of the Taxonomy, will destroy all copies of the Taxonomy and will promptly certify such action to 211 LA in writing. Without limitation of the foregoing, 211 LA may immediately terminate Subscriber's account and ability to access the Taxonomy via the Taxonomy Website upon any expiration or termination of this Agreement. Expiration or termination of this Agreement will not limit either party from pursuing other remedies available to it, including injunctive relief.

The parties' rights and obligations under Sections 2.2, 3, 4, 5.3, 6, and 7 will survive expiration or termination of this Agreement. Further, unless this Agreement has been terminated by 211 LA for breach, the rights granted to Subscriber under Sections 2.1(b) through (e), as well as the rights and obligations set forth in Section 2.3, shall survive and continue following any expiration or termination of this Agreement, but only with respect to the most recent version of the Taxonomy downloaded by Subscriber from the Taxonomy Website as of the date of expiration or termination and provided that Subscriber's rights shall continue to be subject to termination by 211 LA under Section 5.2.

6.Disclaimer of Warranty and Limitation of Liability.

Disclaimer of Warranty. 211 LA does not represent that the Taxonomy will meet any expectations or specifications of Subscriber. THE TAXONOMY AND ANY OTHER INFORMATION, PRODUCTS OR SERVICES PROVIDED BY 211 LA TO SUBSCRIBER ARE PROVIDED "AS IS," WITHOUT WARRANTY OF ANY KIND. 211 LA HEREBY DISCLAIMS ANY AND ALL WARRANTIES OF ANY KIND, WHETHER EXPRESS, IMPLIED OR STATUTORY, INCLUDING, WITHOUT LIMITATION, THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, SATISFACTORY QUALITY, ACCURACY, TITLE AND NONINFRINGEMENT, AND ALL WARRANTIES THAT MAY ARISE FROM COURSE OF PERFORMANCE, COURSE OF DEALING OR USAGE OF TRADE.

Limitation of Liability. TO THE EXTENT PERMITTED BY APPLICABLE LAW: (I) IN NO EVENT WILL 211 LA BE LIABLE FOR ANY INDIRECT, INCIDENTAL, SPECIAL, CONSEQUENTIAL OR PUNITIVE DAMAGES, OR DAMAGES FOR LOSS OF PROFITS, REVENUE, BUSINESS, SAVINGS, DATA, USE OR COST OF SUBSTITUTE PROCUREMENT, INCURRED BY SUBSCRIBER OR ANY THIRD PARTY, WHETHER IN AN ACTION IN CONTRACT OR TORT, EVEN IF THE SUBSCRIBER OR THE OTHER PARTY HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES OR SUCH DAMAGES ARE FORESEEABLE AND (II) 211 LA'S LIABILITY FOR DAMAGES HEREUNDER WILL IN NO EVENT EXCEED THE FEES RECEIVED BY 211 LA HEREUNDER. SUBSCRIBER ACKNOWLEDGES THAT THE LIMITATIONS OF LIABILITY IN THIS SECTION 6.2 AND IN THE OTHER PROVISIONS OF THIS AGREEMENT, AND THE ALLOCATION OF RISK HEREIN, ARE AN ESSENTIAL ELEMENT OF THE BARGAIN BETWEEN THE PARTIES, WITHOUT WHICH 211 LA WOULD NOT ENTER INTO THIS AGREEMENT.

7.Miscellaneous Provisions

No Assignment. Subscriber may not assign, sell, transfer, delegate or otherwise dispose of, whether voluntarily or involuntarily, by operation of law or otherwise, this Agreement, or any rights or obligations under this Agreement. Any purported assignment, transfer, or delegation by Subscriber will be null and void. Subject to the foregoing, this Agreement will be binding on the parties and their respective successors and assigns.

Relationship Between the Parties. The parties shall at all times be and remain independent contractors. Nothing in this Agreement creates a partnership, joint venture or agency relationship between the parties.

Governing Law. This Agreement is to be construed in accordance with and governed by the internal laws of the State of California (as permitted by Section 1646.5 of the California Civil Code (or any similar successor provision)) without giving effect to any choice of law rule that would cause the application of the laws of any jurisdiction other than the internal laws of the State of California to the rights and duties of the parties. In the event of any controversy, claim or dispute between the parties arising out of or relating to this agreement, such controversy, claim or dispute may be tried solely in a state or federal court located within the County of Los Angeles, California and the parties hereby irrevocably consent to the jurisdiction and venue of such courts.

Severability and Waiver. If any provision of this Agreement is held to be illegal, invalid, or otherwise unenforceable, such provision will be enforced to the extent possible consistent with the stated intention of the parties, or, if incapable of such enforcement, will be deemed to be severed and deleted from this Agreement, while the remainder of this Agreement will continue in full force and effect. The waiver by either party of any default or breach of this Agreement will not constitute a waiver of any other or subsequent default or breach.

Headings. The headings used in this Agreement are for convenience only and shall not be considered in construing or interpreting this Agreement.

No Third Party Beneficiaries. This Agreement is made and entered into for the sole protection and benefit of the parties hereto, and is not intended to convey any rights or benefits to any third Party, nor will this Agreement be interpreted to convey any rights or benefits to any person except the parties hereto.

Entire Agreement. This Agreement, along with the Terms of Use made available on the Taxonomy Website, constitutes the complete agreement between the parties and supersedes any prior or contemporaneous agreements or representations, whether written or oral, concerning the subject matter of this Agreement. This Agreement may be changed by 211LA from time to time immediately upon notice to Subscriber (which may be achieved by posting an updated copy of this Agreement on the Taxonomy Website) or by written agreement of the parties. Continued use of the subscriber portions of the Taxonomy Website following any change constitutes acceptance of the change.
