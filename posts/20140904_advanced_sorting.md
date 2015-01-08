# Advanced sorting

> September 09, 2014 - by Alexandre

By default, in OpenSearchServer, search results are sorted by relevance.

Another field can be used for sorting results, such as a "price" or "date"field, by simply adding JSON sorting terms to the query:

```json
"sorts": [ 
   { 
     "field": "price", 
     "direction": "DESC"   }
]
```

Default sorting on relevance will work most of the time, but sometimes **results will appear to be randomly sorted** when repeatedly submitting the same search. This is because, for these particular search keywords, **several results have the same relevance "score"** as computed by OSS.

<!--more-->

To avoid this apparent randomness, you can easily **decide to sort documents having the same relevance score on a second field**. For example, to use the "date" field as a second level of sorting simply write:


```json
 "sorts": [ 
  {
     "field": "score", 
     "direction": "DESC"   },
   {
     "field": "date", 
     "direction": "DESC"   }
]
```

Of course this little trick can be used the other way round too. When sorting documents using a particular field, documents having the same value for this field will be displayed in a random order. To avoid this, add a sorting using the "score" pseudo-field:


```json
"sorts": [ 
   { 
     "field": "price", 
     "direction": "DESC"   },
   { 
     "field": "score", 
     "direction": "DESC"   }
]
```

Three (or more) levels can be used:


```json
"sorts": [ 
   { 
     "field": "price", 
     "direction": "DESC"   },
   { 
     "field": "score", 
     "direction": "DESC"   },
   { 
     "field": "product_id", 
     "direction": "DESC"   }
]
```