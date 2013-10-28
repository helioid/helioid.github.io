---
layout: post
title: Programmatic Categorized Search Results via the Helioid API
categories:
- General
tags: []
status: publish
type: post
published: true
meta:
  _edit_last: '1'
---
We have put online an alpha version of a JSON API for Helioid's search results.
Test it out, see what works and what could be better, then let us know.  We are
going to iterate on it to find the best structure.

For example, the search results for [Data
Analytics](http://www.helioid.com/searches/q/Data+Analytics) can be returned as
JSON using this query:
[http://www.helioid.com/searches/q/Data+Analytics?format=json](http://www.helioid.com/searches/q/Data+Analytics?format=json).

The returned results are stuctured as follows:

```json
{
  "query": "Data Analytics",
  "date": "2013-10-27T03:15:53Z",
  "categories": [{
    "name": "data mining",
    "items": [{
      "date": "2013-10-27T03:15:54Z",
      "rank": 1,
      "summary": "Gain fresh new insights into emerging trends and
                  behaviors that can increase your revenue and reduce
                  cost with Teradata <b>data</b> mining technology.",
      "title": "Teradata - Data Mining and Analytics Solutions",
      "url": "http://www.teradata.com/business-needs/..."
    },
    ...
    ]
  ...
  }]
}
```

The results first include details about the query and then a map from each
category name to the set of search results ("items") within that category.

