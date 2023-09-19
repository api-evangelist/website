---
published: true
layout: post
title: 'Data good practices: If it ain''t computable, it''s a string...'
image: /images/posts/2022-10-29-numeric-vs-string-data-types.jpg
author:
  name: pascal
tags:
- Data
- Metadata
---

Choosing the right data type for a dataset variable, database fields, data model element, or API property can make a huge difference in terms of usability and quality. A mistake that I have commonly seen made over the many years of working with data is the use of numeric variables for things that are not computable. The most typical case is with categorical variables codes, but other examples includes identifiers, accounts numbers, postal codes, and the likes. If something looks like a number, we have a human tendency to assume it should be stored as a number. This is often not necessary and unfortunately can have significant side effects or loss of information. 

A variable only needs to be numeric is if we expect to perform some kind of computation on it like add, subtract, multiply, divide, or statistical function such as average, mean, average, min, max, and the likes. If not, there is no reason to use an integer, decimal, or floating point type. 

The most harmful and negative consequence of mistyping a variable as numeric is the loss of leading zeroes. For example:

- Codes like 01,02,03 turn into 1,2,3, or 012.34 into floating point value 12.34, turning it into an invalid code and loosing its meaning
- An identifier like 012345 becomes 12345, breaking referential integrity
- A U.S. ZIP code 04743 will send your letters and packages to an unknown 4743 location
- A date encoded as DDMMYYYY or MMDDYYYY like 01012022 changes to an invalid 1012023

You get the idea. And this is obviously not something that is desirable. 

But even if your data values never start with a zero, it is conceptually wrong and dangerous to assign a numeric type to something we do not expect to use for computational purposes. A numeric type 'hints' that this is a possibility, and this is unnecessary.

Now there are intersting hybrid use cases, like 'age', that can be used both used as a number or category (dimensional analysis). For example you may want to compute an average age, so in this case the data type should be an integer. At the same time, you may find that values like 99 really mean '99 or older'. This is where metadata comes into play and the variable documentation should describe this top coded value properly. But that is a different topic.  And I will likewise leave date/time data types for another out of the discussion for now, though keep in mind that ISO 8601 date/time as a string is never ambiguous.

So to summarize, string/text should be the default data type for most data values, not numeric. Unless you intend to perform some mathematical or statistical operation, do not assign a numeric data type, even if your instinct tells you to do so.
