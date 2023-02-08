---
published: true
layout: post
title: 'Using ChatGTP to convert human knowledge into machine actionable formats'
image: /images/posts/2023-02-08-using-chatgpt-to-digitize-knowledge/headline.jpg
author:
  name: pascal
tags:
- data
- metadata
- ddi
- fair
- Featured
---

Human knowledge has naturally for centuries been captured in human friendly formats such as books, intended to be consumed by, you guessed it, humans. But our world has changed dramatically and we now live in a space   where this needs to be shared with computers. Machine driven processing, learning, or intelligence requires access to human knowledge in digital formats. We have more or less completed the transition from paper into formats such a PDF, Word, Excel, HTML, but these are unstructured and not easily consumable or understandable by software. We need to take this one step further and transition into machine friendly JSON, XML, or RDF formats, whose structured can be well described by standard specifications, schemas, and models. This is often perceived as a monumental task, but can AIs such a ChatGTP help?

### The Digitization Challenge
I've been working with metadata and related standards and best practices for over two decades, and one of the biggest barrier we face is precisely this conversion problem. For example, we produce data that we store in files and databases to use by computer applications and software, but do not have the habit to make the documentation or knowledge surrounding the data in machine friendly formats, resulting in data wrangling (humans doing the research work and spoon feeding the machines). 

But beyond this, to create high-quality data, drive research and innovation, enable machine learning, and unleash machine intelligence, it is critical to also have access to more fundamental knowledge and reference metadata. 

For example, for consistency and accuracy, data related to countries should utilize ISO country codes. Or when recording measurements, numeric values should be expressed and associated with SI units. Such standards and best practices are widely available, but inconsistently used by software. These resources should be equally be available to humans and machines, facilitating the seamless exchange of information between the two.

Such information is surprisingly hard to find in machine actionable formats, and even more rarely available over APIs. Sure you may find various resources out there that have been put together by a good soul, an open source project, or in some case robust initiatives. But these are rarely under the custody or control of standard settings organizations that are actually in charge of maintaining this knowledge, resulting in discrepancies, provenance uncertainties, or difficulties in understanding how things may have changed over time.

This situation is unintended and the problem not neglected, however, converting long-standing analog maintenance and publishing processes into digital ones can pose challenges for agencies with limited technology and IT expertise. And a universal challenge for these agencies is the transformation of unstructured publications into machine-readable formats.

### Can ChatGPT Help?
ChatGPT (Chat Generative Pre-trained Transformer) is a chatbot launched by OpenAI late 2022 that has gained tremendous popularity and press coverage. ChatGPT has been trained on a diverse range of internet text, including websites, articles, and social media posts, the goal being to provide the AI with the ability to understand and generate text on a wide variety of topics, with a high level of coherence and consistency. 

Can ChatGPT be used to digitize our unstructured information? The only way to determine is by trying.

### An experiment around the International System of Units (SI)
As a member of the CODATA [Digital Representation of Units of Measurement (DRUM)](https://codata.org/initiatives/task-groups/drum), my aim is to raise awareness, educate, and empower communities in the utilization and implementation of digital unit representation. Our mission involves exploring the challenge of converting information related to units, quantities, and fundamental constants into digital formats.

ChatGPT has recently captured the attention of our group and we aim to evaluate its proficiency in units of measurement and the accuracy of the information it provides.

As I started to dive into this process and ask ChatGPT various questions, I realized that I could not only get the answers formulated into plain English language, but also in formats such as JSON, which essentially is the conversion we are looking for. And this seems to work reasonably well. 

#### Boltzmann constant historical values
Here is an example around the Boltzmann constant, starting with a basic knowledge question:

![](/images/posts/2023-02-08-using-chatgpt-to-digitize-knowledge/chatgpt_bolzmann_01.png)

With the easy one out of the way, I shifted to the more complex issue of determining the changes of its value over time. This is not particularly trivial as the National Institute of Standards and Technology (NIST) website only officially publishes the latest values, with historical data from 2014 and earlier being available in ASCII and PDF files (dating back to 1969). While other public resources are available, this illustrates some of the difficulties in compiling this information:

![](/images/posts/2023-02-08-using-chatgpt-to-digitize-knowledge/chatgpt_bolzmann_02.png)

I was pleasantly surprised to see that ChatGPT was able to provide information dating back to 1906. However, I quickly realized my lack of experience in querying AI, as the response was missing some intermediate values. To obtain a more complete version, I reworded my prompt:

![](/images/posts/2023-02-08-using-chatgpt-to-digitize-knowledge/chatgpt_bolzmann_03.png)


Looking better. And this is the moment I realized that this could be returned in JSON format, which ChatGPT produced as follows, apparently solving the digitization challenge:

![](/images/posts/2023-02-08-using-chatgpt-to-digitize-knowledge/chatgpt_bolzmann_04a.png)

![](/images/posts/2023-02-08-using-chatgpt-to-digitize-knowledge/chatgpt_bolzmann_04b.png)

### Caveats and Current Limitations
Now this may look impressive, but it is important to know that current version of ChatGPT has limits

#### Inconsistent Answers
ChatGPT may not always return the same answer, and may even be wrong (as do people). As an example, the same above question asked the next day to ChatGPT only returned a JSON file with values for 5 different years, and in this case going back to 1884. This kind of issue may be addressable in the future with more accurate promoting on my part or having the ability to tweak the AI.

![](/images/posts/2023-02-08-using-chatgpt-to-digitize-knowledge/chatgpt_bolzmann_04c.png)

And all these values, particularly historical ones, should be reviewed and vetted. And the matter in this specific case is also complicated as it is historically not clear when the constant was actually named after Boltzmann, as for instance illustrated by [this discussion thread](https://hsm.stackexchange.com/questions/6925/when-did-the-name-boltzmann-constant-prevail-and-how).

#### Size Limit

Another current limitation of ChatGPT to be aware of is size. The free version is currently is limited it 4,000 tokens of input and output, which only allows for short questions and answers.

For example when I prompted ChatGPT to provide me with the list of all the SI units and their relationships, the returned information was correct in plain English, but the JSON file was truncated.

I anticipated for this restriction to be addressed once the recently announced [ChatGPT Plus](https://openai.com/blog/chatgpt-plus/) (paid version) becomes available.

![](/images/posts/2023-02-08-using-chatgpt-to-digitize-knowledge/chatgpt_truncated_01a.png)
…
![](/images/posts/2023-02-08-using-chatgpt-to-digitize-knowledge/chatgpt_truncated_01b.png)
…truncated output…


#### No API

ChatGPT can today only be interacted with through its web based user interface, limiting the amount of information that can be exchanged and processed. An API in the works which, once available, should allow us to integrate with tools and automate the processes.

![](/images/posts/2023-02-08-using-chatgpt-to-digitize-knowledge/openai_twitter_01.png)

### Conclusions
This initial experiment is highly promising and inspiring. It opens up new avenues for the digitization of human knowledge to make it more accessible and usable by machines, particularly in the realm of public references and standards based metadata. Relieving the burden of conversion would greatly aid organizations as they shift towards a digital environment. Although it may not be a perfect solution, human-machine collaboration may prove to be the key. I am eager to delve deeper into this exciting development.
