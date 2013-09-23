---
layout: post
title: "Opportunities in API Deployment, PDF APIs"
url: 'http://apievangelist.com/2011/04/04/opportunities-in-api-deployment-pdf-apis/'
image: ''
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/Tag-Cloud-API-PDF.png" alt="" width="350" align="right" />I'm spending time evaluating different types of APIs in various categories.

I want to see how each provider delivers their API in similar categories, and potentially look for opportunities within those categories for new API services.

I'm starting with PDF APIs.

There are quite a few web APIs providing services to generate and work with PDFs.

The first main group of APIs I notice are HTML to PDF conversion APIs:

  * [DocRaptor][1]
  * [Doculicious][2]
  * [htm2pdf][3]
  * [Joliprint][4]
  * [HTML2PDF][5]
  * [Web2PDF][6]
  * [PDF My URL][7]
  * [PDF Crowd][8]
Next there are a couple of other PDF conversion tools:<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/PDF_red.jpg" alt="" width="150" align="right" />
  * [Anything to PDF][9] \- Convert base 64 encoded data to PDF
  * [PDF Alchemy][10] \- Word to PDF
Beyond document conversion I found two APIs for commenting and annotating PDFs:
  * [Crocodoc][11] \- PDF commenting and collaboration
  * [A.nnotate][12] \- PDF annotation
Then there was a single provider of PDF document signatures:
  * [DocuSign][13]
There are two clear leaders that provide more advanced PDF document management services:
  * [Doxument][14] \- HTML to PDF, OCR, Split PDF pages in separate images
  * [Google Docs][15] \- File Conversion to PDF, OCR, translation
With the ubiquitous nature of PDFs, and a wide range of desktop and web based PDF tools, I think there is a huge opportunity for new types of APIs in this area. <img class="c1" src="http://kinlane-productions.s3.amazonaws.com/pdf-ocr.png" alt="" width="150" align="right" /> There are dozens of code libraries in various languages for manipulating PDFs. I would suggest some savvy developer:
  * Identify the most viable business uses for PDF APis
  * Select the strong set of PDF language libraries
  * Wrap in a RESTful wrapper
  * Deploy on Amazon EC2 with PDF storage on Amazon S3
PDF APis is one category of APIs that has huge opportunity for growth in the next couple of years.

   [1]: http://docraptor.com/documentation (DocRaptor)
   [2]: http://docs.doculicious.com/api (Doculicious)
   [3]: http://webservice.htm2pdf.co.uk/htm2pdf.asm (html2PDF)
   [4]: http://joliprint.com/api/ (Joliprint)
   [5]: http://www.html2pdf.biz/api.php (HTM2PDF)
   [6]: http://www.web2pdfconvert.com/pdf-api.aspx (Web2PDF)
   [7]: http://pdfmyurl.com/support/support.jsp (PDF My URL)
   [8]: http://pdfcrowd.com/html-to-pdf-api/ (PDF Crowd)
   [9]: http://api.danielprocter.com/ (Anything to PDF)
   [10]: http://www.pdfalchemy.com/ (PDF Alchemy)
   [11]: http://crocodoc.com/api/ (Crocodoc)
   [12]: http://a.nnotate.com/api-reference.html (Annotate)
   [13]: http://www.docusign.com/developers-center/developers-center-overview (DocuSign)
   [14]: http://doxument.com/en/developer (Doxument)
   [15]: http://code.google.com/apis/documents/ (Google Docs)
