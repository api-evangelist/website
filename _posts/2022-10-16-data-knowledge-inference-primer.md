---
published: true
layout: post
title: 'Data Knowledge Inference:  A primer'
image: /images/posts/2022-10-16-data-knowledge-inference-primer.jpg
author:
  name: pascal
tags:
- Data
- Metadata
- FAIR
- Knowledge Inference
- Machine Learning
- AI
- Featured
---

<p>
Data in its current state is insufficient to meet the needs of users and intelligent applications. It needs to be elevated to digital knowledge by supplementing it with machine-actionable metadata. This is necessary to align on <a href="https://www.go-fair.org/fair-principles/" target="_blank">FAIR principles</a>, reduce data wrangling, support the establishment of Open Data APIs, and unleash computer intelligence.
</p>

<h3>Automating metadata inference to turn data into digital knowledge</h3>
<p>
Data typically resides in files or databases that lack the capacity to, alongside, capture documentation. As a result, the information necessary to find, access, or do anything useful with the data is lacking. Furthermore, even when found, such documentation is rarely available in formats that applications can understand. This translates into data wrangling, and severely limits our ability for machine driven processing or the establishment of rich APIs.
</p>
<p>
Compiling metadata—machine-actionable documentation in standards formats like JSON, RDF, or XML is often perceived as a significant hurdle as it is commonly seen as a manual burden and a monumental task that requires going back through decades of data. We all want metadata, but nobody wants to do it. This does not need to be the case. 
</p>
<p>
First, while the backlog aspect may be real, it only applies to past data, and there is no reason not to start doing this for newly-produced data. But besides this, we can call upon the assistance of computer tools to help alleviate a significant portion of this burden. Even with no documentation available at all, it is entirely possible to infer metadata from scratch from a data file. 
</p>
<p>
How would such a process work and how far could this be pushed? What would <i>metadata inference</i> look like? Below are some high-level ideas, concepts, and approaches I'm exploring under the Postman Open Technologies Open Data and Research Intelligence program.
</p>

<h3>Basic Profiling: Understanding the data structure and content statistics</h3>
<p>
The first step we need to take when documenting data is to understand the basic structure and content of each data field. The most challenging use case when it comes to inferring such metadata is a standalone text file (e.g., CSV), as it holds no information about the data, besides an optional header line with the variable (column) names. Other formats such as SQL databases or statistical packages like SAS, Stata, and SPSS do carry a fair amount of information (schema, names, value label) that provide a starting point and reduce initial efforts.
</p>
<p>
Acquiring such knowledge is actually relatively easy as there are numerous <a href="https://en.wikipedia.org/wiki/Data_profiling" target="_blank">data profiling</a> tools and techniques readily available to us. This includes <a href="https://hevodata.com/learn/data-profiling-tools" target="_blank">free</a> and commercial packages such as <a href="https://pandas-profiling.ydata.ai/docs/master/" target="_blank">Python Pandas Profiling</a>, <a href="https://datacleaner.github.io/" target="_blank">Data Cleaner</a>, Talend’s <a href="https://www.talend.com/products/talend-open-studio/" target="_blank">Open Studio</a>, <a href="https://openrefine.org/" target="_blank">OpenRefine</a>, <a href="https://www.visidata.org/" target="_blank">VisiData</a>, and the likes. The key is to use these tools and other custom utilities to produce outputs in open formats such as JSON or XML based on domain standards endorsed by the community.
</p>
<p>
Our first step towards achieving metadata inference is therefore to put together a toolkit leveraging available tools in our arsenal that produces outputs documenting data type, summary and descriptive statistics, string patterns, and other insightful attributes that can be used to infer useful facts about the data. 
</p>
<p>
While this is readily a significant step forward, it is, as you suspect, only the beginning.
</p>


<h3>Advanced Profiling: Higher level documentation</h3>
<p>
With some basic knowledge in place, we can now start answering more interesting questions going beyond traditional profiling. 
</p>
<p>
One example would be to classify the variables in terms of being categorical, nominal, ordinal, or continuous. Categorical variables have a set of discrete values that are typically strings (or integers) and are commonly used for dimensional analysis or as classifiers. Continuous variables, on the other hand, are typically floating point or decimals that can take any numeric values and are used with statistical aggregations and models. When you think of this, determining such characteristics can relatively easily be achieved with good confidence by leveraging the output of profilers (frequencies, value distribution), adding new facts to our knowledge.
</p>
<p>
Another example would be to determine a dataset primary key. This could be as trivial as finding a variable having all values with a frequency of 1 and no null or missing entries. Compound primary keys may be more challenging to detect, but can be determined by running various permutations. Note that it is not uncommon for datasets not to have a primary key. In such a case, documenting this and generating one may be desirable if such an option is acceptable.
</p>
<p>
Many similar simple ideas can be explored: missing value analysis or documenting the statistical distributions can provide valuable insights on variables, correlation and other multi-variate analysis could be precomputed, hash/fingerprinting techniques can be applied to facilitate comparison and identification.
</p>
<p>
By extending basic profiling, we can start designing various methods to infer higher-level knowledge around data.
</p>

<h3>Concept Inference: What is the data about?</h3>
<p>
Diving into more complex and enriching methods, let’s think about inferring conceptual components present in the data: what is it about? What are the topics/subjects, time, or geography? 
</p>
<p>
One simple way would be to examine the actual variable names if present (e.g., the first line in CSV or database fields). While names can be cryptic in some cases, some fairly clearly identify the nature of the column content (e.g., gender, DOB, ID, name, country, state, etc.), or offer a good hint. Many of these commonly used abbreviations or acronyms can be associated with concepts. The degree of confidence can be strengthened by basic metadata such as descriptive statistics. A biological sex variable for example typically has 2-3 categories (male, female, no response), while a gender variable will be more in the 5-10 counts, enabling us to differentiate between both concepts.
</p>
<p>
We could also recognize that a categorical variable set of values matches commonly used national, international, or domain classifications such as country, state, or province codes, industry, or occupation, revealing many of the underlying variable and dataset concepts.
</p>
<p>
A date/time data type or string pattern would indicate that a variable is temporal in nature, which is not only an important fact, but can also offer insights about the time period covered by the data.
</p>
<p>
Finding variables that are associated with geospatial concepts is also of high interest. This could be done by recognizing longitude and latitude patterns, examining categorical variable codes to match geospatial classifications, or parsing keywords from string variables (e.g., country, state, or province names). A phone number pattern can be used not only to indicate what the variable is about, but also as a proxy for geography. For example, all numbers may match the US, and digging deeper, all area codes may point to a specific state like California. 
</p>
<p>
And naturally, performing analysis on text variables would reveal more concepts.
</p>
<p>
Similarly to profiling, many algorithms can be elaborated to infer concepts from the data. This is where intelligence really begins to emerge, as concepts are typically how users and applications discover and use datasets and variables of interest.
</p>

<h3>From Profiling to Machine Intelligence</h3>
<p>
The endgame and ultimate objective of this exercise is to unleash machine intelligence.  As you can envision by now, the above ideas may just be scratching the surface of what can be achieved through machine-driven knowledge inference. Many generic or specialized algorithms can be designed to infer knowledge from the data. 
</p>
<p>
The latter however can only be achieved with the core knowledge in place, which means we first need profiling and concept inference layers in place, before we can hand this over to machine learning and AI. But ultimately, applications should be able to self-discover data and document with minimal intervention from human counterparts.While this may be somewhat down the road, it is never too early to start experimenting.
</p>

<h3>Organizing An Army of Expert Agents</h3>
<p>
To implement a metadata inference framework, we envision designing an environment where software agents with various levels of expertise would work together in a well-orchestrated manner. Agents can then rely on each other's outputs to collaboratively and iteratively infer knowledge around data, from basic facts to high-level conceptual components and beyond. Each little piece of information can be modeled and stored as facts in a database leveraging semantic technology..
</p>
<p>
It is also important for machine-based agents to get support when needed from their human counterparts, as not all information can be inferred with 100% certainty. Facts should therefore always be accompanied with a degree of confidence that can be used to seek human guidance below a certain threshold. So this will naturally not completely alleviate the burden, but machines can significantly contribute to creating metadata around data.
</p>


<h3>An API Powered Framework</h3>
<p>
As  back-end tools and libraries are put together, APIs will naturally play a fundamental role in connecting the dots and delivering knowledge inference solutions to users and applications, offering end points where files or data streams can be submitted for analysis and providing access to reference metadata and inferred knowledge.
</p>

<h3>Where to go from here?</h3>
<p>
Hope this article helps you get a feel of what I'm are up to at Postman Open Technologies.
I'm naturally looking to collaborate with others on this, so reach out if you have any feedback or suggestions, and visit our <a href="https://github.com/postman-open-technologies/opendata-knowledge-inference" target="_blank">GitHub repository</a> if interested in participating in this innovative research. Be on the lookout for more articles in the near future.
</p>



