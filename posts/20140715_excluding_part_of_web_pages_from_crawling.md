# Excluding part of Web pages from crawling

> July 15, 2014 - by Alexandre

When crawling web pages, we usually **don’t want to index areas of pages like header, navigation menu, footer, sidebar**, ads, etc. Indeed, these parts lead most of the time to **irrelevant results** when querying the index. For example, the same article may be displayed in a sidebar on every pages: when searching for this article, all the pages would be returned!

OpenSearchServer offers several convenient and powerful ways to solve this problem, like **using some XPATH requests to target unwanted areas**:

![Xpath exclude](../images/xpath_exclude.png)

Learn more about [excluding part of web pages when crawling in our documentation center.](http://www.opensearchserver.com/documentation/faq/crawling/how_to_exclude_some_part_of_webpage_from_crawling.md)