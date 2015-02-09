# Using variables with the Database Crawler

> August 05, 2014 - By Alexandre

Sometimes, when crawling databases, one needs to change some parameters just before running the standard query. For example, one might want to execute a database crawl for but a subset of data, or even a specific product.

The sloppy approach is to create multiple database crawlers by duplicating one, changing some values and saving them - and hopefully giving them an explicit name. But this **will quickly become complicated to maintain**.

Fortunately, OpenSearchServer's database crawler **can take some parameters as inputs**.

There are two different paths to do that: via a task in the Scheduler (manually or through the dedicated API), or by directly using the Database Crawler API.

Learn more about this [awesome feature in our documentation center](http://www.opensearchserver.com/documentation/faq/crawling/how_to_use_variables_with_database_crawler.md).
