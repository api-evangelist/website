---
layout: post
title: "More Government Data with the Federal Register API"
url: 'http://apievangelist.com/2011/08/03/more-government-data-with-federal-register-api/'
image: ''
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/government/presidential-seal.png" alt="" width="175" align="right" />][1]Each day Federal agencies publish documents in the Federal Register. These documents include proposed rules, final rules, public notices, and Presidential actions. The print-based version of the Federal Register can be difficult to read, process and access, so the [Office of the Federal Register][1] (OFR) of the [National Archives and Records Administration][2] (NARA), and the [U.S. Government Printing Office][3] (GPO), who all joined forces to launch the [FederalRegister.gov][4] website, also deployed an API.

The goal of the initiative was to make it even easier for developers to build new ways of interacting with Federal Register data, making it easier for citizens and communities to understand the regulatory process and to participate in the Government decision-making process.

The [Federal Register API][5] is RESTful, with no keys required for authentication and responses in a JSON format. They even provide a simple JSON interface for callbacks. All data in the Federal Register is updated daily by 6 a.m., and is published Monday through Friday, except Federal holidays, and consists of four types of entries:

  * **Presidential Documents** \- Executive orders and proclamations
  * **Rules and Regulations** \- Policy statements and interpretations of rules
  * **Proposed Rules** \- Petitions for rulemaking and other advance proposals
  * **Notices** \- Scheduled hearings and meetings open to the public, grant applications, administrative orders, and other announcements of government actions
The Federal Register API is meant to deliver print-based material in machine-readable formats, to make the Federal Register more searchable, accessible, easier to digest, and easier to share withother systems.

The Federal Registers, encourages every citizen to become more involved in the workings of their government and to make their voices heard on the things that matter to them, from the smallest to the largest issues.

I'm reporting on multiple government APIs lately with, [Political Influence in U.S. an API Call Away][6]" and "[More Government Data with U.S. Department of Labor API][7]". With all the bullshit and theatrics in politics and the media, this kind of news really gets me excited about getting more involved in the Government decision-making process.

   [1]: http://www.archives.gov/federal-register/ (Office of the Federal Register)
   [2]: http://www.archives.gov/ (National Archives and Records Administration)
   [3]: http://www.gpo.gov/ (U.S. Government Printing Office)
   [4]: http://www.federalregister.gov/ (federalregister.gov)
   [5]: http://www.federalregister.gov/blog/learn/developers (Federal Register API)
   [6]: Political%20Influence%20in%20U.S.%20an%20API%20Call%20Away (http://blog.programmableweb.com/2011/08/01/sunlight-labs-releases-influence-explorer-text-api/)
   [7]: http://blog.programmableweb.com/2011/07/28/more-government-data-with-u-s-department-of-labor-api/ (More Government Data with U.S. Department of Labor API)
