---
layout: post
title: Virtualized Document Printing APIs
url: http://apievangelist.com2011/09/05/virtualized-document-printing-apis/
source: http://apievangelist.com2011/09/05/virtualized-document-printing-apis/
domain: apievangelist.com2011
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/mimeo-logo-400.png
---
{% include JB/setup %}<p>
     <a href="http://www.mimeo.com/"><img src="http://kinlane-productions.s3.amazonaws.com/mimeo-logo.jpg"  width="200" align="right" /></a>Even though I cover the entire industry around APIs here on <a title="API Evangelist" href="http://www.apievangelist.com">API Evangelist</a>, I also am the API Evangelist for <a title="Mimeo Connect" href="http://developer.mimeo.com">Mimeo Connect</a>.   Mimeo is a printing API that allows you to print a wide variety of business documents, using your Mimeo.com account.  Its pretty powerful stuff, if you think about it, an API that is connected to 3 print facilities.  
</p>
<p>
     The API seems pretty straightforward at first glance, but developers seem to be encountering three major obstacles:
</p>
<ul>
     <li>
          <strong>Mimeo.com Accounts</strong> - Users don’t like having to get a developer account as well as sandbox and live Mimeo.com accounts to work with the API
     </li>
     <li>
          <strong>Mimeo Documents</strong> - Developers don’t really have time to build and define the documents before integration, they just want to print a specific document, and pass some settings to change it up.
     </li>
     <li>
          <strong>Sandbox and Live Environments</strong> - It is great that Mimeo has sandbox and live environments, but developers were expected to maintain two separate environments, just to use the system.
     </li>
</ul>
<p>
     <a href="http://mimeoconnect.3scale.net/wiki/poster-printing-api"><img src="http://kinlane-productions.s3.amazonaws.com/mimeo/posters-sample.png"  width="150" align="right" /></a> These three areas proved to be the difference between some users adopting, and others walking away.  There was too much work in navigating the world of Mimeo accounts and documents.  This isn’t hard if your already a Mimeo web to print user, but if your a developer you just want to print.  <br />
     <br />
     So I created four virtualized print APIs.   I took a REST framework and deployed four separate “<a title="Document Printing APIs" href="http://mimeoconnect.3scale.net/">document printing APIs</a>”:
</p>
<ul>
     <li>
          <a title="Poster Printing API" href="../../2011/09/05/api-stack-large-format-printing-with-the-mimeo-connect-poster-printing-api/">Poster Printing API</a>
     </li>
     <li>
          <a title="Flyer &amp; Brochure Printing API" href="../../2011/09/05/api-stack-single-sheet-printing-with-the-mimeo-connect-flyer-&amp;-brochure-printing-api/">Flyer &amp; Brochure Printing API</a>
     </li>
     <li>
          <a title="Card Printing API" href="../../2011/09/05/api-stack-card-printing-with-the-mimeo-connect-card-printing-api/">Card Printing API</a>
     </li>
     <li>
          <a title="Spiral Notebook API" href="../../2011/09/05/api-stack-bound-document-printing-with-the-mimeo-connect-spiral-notebook-printing-api/">Spiral Notebook API</a>
     </li>
</ul>
<p>
     Then using <a title="3Scale API Management Solution" href="../../serviceproviders/3scale.php">3Scale self-service API management solution</a> I deployed an API area to handle documentation, forum and developer registration and API key management.  Each API has seven methods for ordering print documents:
</p>
<ul>
     <li>Proof (POST)
     </li>
     <li>Proof (GET)
     </li>
     <li>Quote (GET)
     </li>
     <li>Shipping Options (GET)
     </li>
     <li>Order Quote (GET)
     </li>
     <li>Place Order (POST)
     </li>
     <li>Order Status (GET)
     </li>
</ul>
<p>
     <a href="http://mimeoconnect.3scale.net/wiki/spiral-notebook-printing-api"><img src="http://kinlane-productions.s3.amazonaws.com/mimeo/Spiral-Notebook-Example-Image.png"  width="150" align="right" /></a> All a developer has to do is <a title="register for a set of keys" href="http://mimeoconnect.3scale.net/plans">register for a set of keys</a>, grab a code sample and get to work.  They don’t have to setup a Mimeo account or build the documents they want to use.  If they want a poster, they use the <a title="Poster Printing API" href="http://mimeoconnect.3scale.net/wiki/poster-printing-api">Poster Printing API</a> and pass the size, paper, mounting and lamination settings, along with the URL of the PDF they want to print.<br />
     <br />
     These four APIs represent a process I will use to virtualize other API instances on top of the Mimeo Connect REST API, and possibly other APIs too.  It is pretty quick for me to bundle the data, settings, and code for a new virtualized API and deliver an entirely new type of document printing API.   
</p>
<p>
     This will give me an agile way to play around with new configurations of APIs, measure their response using the <a title="3Scale" href="http://www.3scale.net/">3Scale API</a> analytics, and decide whether or not I put more resources into an specific type of API.
</p>
