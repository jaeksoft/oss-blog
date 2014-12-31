# Using synonyms to ensure user satisfaction

Using synonyms is a great way to ensure user satisfaction - as they mean fewer searches that return zero results. OpenSearchServer's synonym feature meets this goal by providing:

*   synonyms for single words
*   **synonyms for expressions** made of several words
*   **multiple synonyms** for one word
Furthermore** synonyms are only processed at query time**. This allows for flexible management, since there is **no need to reindex all of your data** when synonyms change!

<!--more-->

Last but not least, you can create **multiple lists of synonyms**! One example is creating not just list of synonyms, but also lists of [hypernyms](http://en.wiktionary.org/wiki/hypernym) (_fruit_ is an hypernym of _apple_) and [hyponyms](http://en.wiktionary.org/wiki/hyponym) (_horse_ is, fittingly, an hyponym of _animal_).

Different fields can be created in the schema to store those values, and different weights can then be used for those in queries. For instance one can assign a weight of 20 to a title, a weight of 10 to its synonyms, a weight of 5 to its hyponyms and a weight of 2 to its hypernyms.

Another use of this feature is **replacing abbreviations**, **slang terms**, etc.

Don't worry, starting to use synonyms is not complex at all! Learn how to do it in our [How to use synonyms](http://www.opensearchserver.com/documentation/faq/querying/how_to_use_synonyms.md) documentation's page.