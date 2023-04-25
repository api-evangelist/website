---
published: true
layout: post
title: 'AI has a metadata problem…'
image: /images/posts/2023-04-24-ai-has-mtedata-problem/standards_emerge.png
author:
  name: pascal
tags:
- ai
- metadata
- Featured
---

Artificial intelligence (AI) has become a captivating and transformative field, capturing the imagination of individuals and industries alike. As I immerse myself in the world of AI, I feel, as many, awed by its potential to revolutionize the way we live and work. 

However, amidst the excitement, there lies a critical challenge that demands attention: the lack of transparency and the scarcity of metadata.

Consider, for instance, conversational AIs like ChatGPT. When users receive responses from such models, they may be curious about the sources of information that informed the AI's answers. Unfortunately, inquiries into the underlying sources often yield limited or ambiguous information, with occasional dead links or unrelated citations. While some metadata may exist beneath the surface, it is difficult to access, unreliable, and lacks clarity.

While AI experts are cognizant of these limitations, everyday users less so. Charmed by the AI's articulate responses, users may overlook the need to critically evaluate the validity of the information provided. 
It is essential to remember that, like humans, AI models are fallible and should be approached with healthy skepticism.

As AI continues to permeate our lives, questions of trustworthiness, bias, and privacy take center stage. Understanding how an AI model has been trained and the origin of its underlying data is paramount to addressing these concerns. 
After all, would we accept statements from anonymous speakers, press releases from unknown sources, or scientific papers without authors or peer review? Such analogies illustrates the current state of AI, where the absence of metadata poses a significant challenge.

So, how do we navigate this to create an AI ecosystem that deliver high-quality, trustworthy information? The journey begins with acknowledging the importance of transparency and metadata in AI and taking proactive steps to address these issues.

### The metadata challenge

The challenge of metadata is not a novel one; rather, it is actually a longstanding data problem. For over two decades, various stakeholders, including national data producers, data librarians, academic researchers, and international organizations, have collaborated to establish standards and best practices for data documentation.

The private sector and technology industry appear to be sparsely aware of these efforts, but mature models for documenting data in digital formats, such as JSON, XML, and RDF, already exist. These models can provide a foundation for addressing metadata challenges in AI and other domains.

One notable initiative that has brought together players in this area is the [FAIR initiative](https://www.go-fair.org/), which advocates for data to be Findable, Accessible, Interoperable, and Reusable. The FAIR principles have emerged as an overarching framework that guides the development of data management practices and standards.

In the context of AI, the urgency lies in documenting provenance, proper citation, and the use of unique identifiers and citations for data sources. To achieve this, the AI community could leverage or learn from existing specifications and initiatives that have been developed for data documentation. 

For instance:
- The [Data Catalog Vocabulary (DCAT)](https://www.w3.org/TR/vocab-dcat-3/) provides a standard for describing datasets in data catalogs. 
- The [PROV Ontology (PROV-O)](https://www.w3.org/TR/prov-o/) offers a model for representing provenance information. 
- The [Data Documentation Initiative (DDI)](https://ddialliance.org/) is an international standard for describing science data
- [DataCite](https://datacite.org/value.html) is an organization that provides persistent identifiers (DOIs) for research data.

By building on these established models and initiatives, the AI community can take meaningful steps toward enhancing metadata transparency and fostering trust in AI systems, while concurrently aligning on existing practices.

### A way forward?

Transparency in AI is not a new topic of discussion, and I am certainly not the first to highlight its importance. And it is important to acknowledge that not all AI models lack documentation; however, accessing and understanding such information can be challenging.

This [recent article](https://www.washingtonpost.com/technology/interactive/2023/ai-chatbot-learning/) published in The Washington Post for example illustrates this issue by examining the Google C4, a large-scale dataset used in language model training. This underscores the complexities associated with tracing the provenance of data used in AI models.

Recognizing the need for improved transparency, the [Hugging Face](https://huggingface.co/) community has taken steps to address this issue through the use of [Model Cards](https://huggingface.co/docs/hub/model-cards) and [Dataset Cards](https://huggingface.co/docs/hub/datasets-cards). 

These Cards are standardized markdown/YAML documents that provide essential information about AI models, including their intended use, performance, and limitations. This initiative can serve as a valuable starting point and reflects the needs of the AI community.

To strengthen this approach, it would be beneficial to integrate and align Model and Dataset Cards with established standards and best practices, such as those mentioned in the previous section. 

The goal here being to develop a formal specification or standard for AI documentation that is backed by a robust data model. 

Additionally, the creation of tools are essential to foster the adoption and use of such specifications and the involvement of AI and data communities and  other stakeholders, are necessary for effective governance.

By elevating metadata management and transparency to a priority and adopting a collaborative approach towards the establishment of documentation standards and best practices, we can work towards a future where AI models are not only powerful but also transparent, accountable, and trustworthy.

### Conclusions

For more than two decades, I have been a vocal advocate for the adoption of metadata standards and best practices in data management. As I reflect on the challenges faced by the AI community, I see the issue of metadata transparency as a natural extension of this broader effort.

Fortunately, we do not need to start from scratch. There is immense value in leveraging and extending the metadata standards that have been thoughtfully developed over the past two decades. By building upon these existing practices, we can address the metadata aspects specific to the AI domain.

A common challenge in the world of standards is the proliferation of too many competing options:

[![](/images/posts/2023-04-24-ai-has-mtedata-problem/standards_multiply.png)](https://xkcd.com/927/)

[https://xkcd.com/927/](https://xkcd.com/927/)


However, the good news is that the AI space  is not yet in this predicament. Instead, we find ourselves at a pivotal moment where we have the opportunity to shape the future of AI metadata standards in a cohesive and unified manner.

![](/images/posts/2023-04-24-ai-has-mtedata-problem/standards_emerge.png)

I am enthusiastic about contributing to this effort, and I believe that success lies in bringing together diverse stakeholders from the data, technology, and AI communities. By convening around the same table, sharing expertise, and building upon existing best practices, we can collaboratively develop standards that enhance the transparency and trustworthiness of AI systems. Together, we can work towards a future where AI is not only intelligent but also accountable and reliable.

--- 

*Acknowledgements: Thanks to Kin Lane, my teammates at Postman, and my colleagues across the (meta)data communities for inspiring this story.*

*Disclaimer: In the interest of providing readers with a more polished and articulate experience, this article has been enhanced with the assistance of ChatGPT-4.*