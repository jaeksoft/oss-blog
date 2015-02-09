# Web crawling: get rid of useless URL parameters

> August 01, 2014 - By Séverine

When using OSS’s Web Crawler, the crawling operation might last too long. **The more URLs the web crawler has to parse, the longer the crawl gets**. This is why it is important to **limit the number of URLs** as much as possible.

The `Pattern list` can be your first response. Limiting the allowed patterns for a website's URLs is a good starting point. But sometimes it is not enough, especially in these two scenarios:

1. when a website does not define any `Canonical URL` (to help search engines avoid duplication) and appends a `jsessionid` parameter to all its URLs. In such a situation, the web crawler may encounter multiple links to the same page, which only differ by their `jessionid` parameter. This is terrible for search engine discoverability and content duplication.
2. when a website contains faceted listings: this could lead to a innumerable combinations of parameters and thus innumerable URLs to be crawled. A typical example of such URLs would end in ways such as `...?color=blue&dir=ASC`, `...?color=red&dir=DESC`, `...?color=purple&brand=LOREM&size=M`, ...). In this case it is usually unnecessary for the crawler to crawl all these combinations. It only needs to see the content once to index it.

In these two circumstances **it becomes vital to delete the unnecessary parameters** to keep the URL Browser data as clean as possible.

Learn how to properly [configure the powerful URL Filter feature in our documentation center!](http://www.opensearchserver.com/documentation/faq/crawling/how_to_use_URL_filter_feature.md)
