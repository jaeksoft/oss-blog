# Improving relevancy with “Mirror AND filter”

> August 27, 2014 - by Séverine

When using multiple keywords in a single search query, one usually wants to apply an AND operator to these keywords. That is, **all keywords must be found** in at least one field of a document for this document to be included in results.

This is a common scenario, which suits most users. If an OR operator (meaning "at least one of the keyword") were to be used, it would produce** irrelevant results**.

However sometimes one **wants to give some documents more weight for a having one of the keywords in a specific field**, as long as they also contain the other keywords of the query in this or other fields.

Let's assume two documents, each with three fields:

1. _Title_: Science of comets  
_Subtitle_: How to make a good landing  
_Summary_: The science of comets is a vast subject, we will cover it in a particular way.
2. _Title_: Science or fiction  
_Subtitle_: A review of the science of science-fiction  
_Summary_: Much has been imagined by science-fiction writers, from walking on the Moon to comet landing: find out what is not fiction anymore!

If a user searches for "**comet landing**" and we use the traditional way of running this search, the second document will most likely come first in the results since the words "comet landing" are **directly found** in its summary. Even if the "title" and "subtitle" fields were given more weight, the first document would not come first for this search.

Hence the need to give more weight to some documents **if they have some of the keywords in important fields**. OpenSearchServer's Mirror And Filter feature can achieve this.

Here is how it gets the job done: an **OR** operator is used (instead of an AND) to run the search and **to score the documents**, but then a filter is applied on these results to only **keep those documents that would have been found if the operator had been an AND**.

Clever, heh? Keep on reading [our documentation page](http://www.opensearchserver.com/documentation/faq/querying/improving_relevancy_with_mirrorandfilter.md) to know more and to improve the relevance of your search results!