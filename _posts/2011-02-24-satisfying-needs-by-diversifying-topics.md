---
layout: post
title: Satisfying Needs by Diversifying Topics
categories:
- General
tags:
- categorized search
- diversity
- personalization
- topic models
status: publish
type: post
published: true
meta:
  _edit_last: '1'
---
When retrieving documents for a search query, a simplistic approach that ranks the most relevant documents highest will leave users completely unsatisfied if it incorrectly interprets the query.  Incorrect interpretation is an inevitable possibility when dealing with ambiguous queries, which in some experiments were shown to represent over 16% of all queries [1].  Significant ambiguity can result from query terms that have many synonyms.  We can hypothesize the the amount of ambiguity will increase as the internet (and search indexes) grow simply because the probability of the same term being used in different contexts increases as the number of terms increases.

As an example, consider the query "ajax" which could refer to web development methods of Asynchronous JavaScript and XML, to the Amsterdam soccer team, to the household cleaning product, to the Greek warrior, etc.  Ranking solely by relevance score will likely lead to a first page of results that only satisfy the web development meaning, due to the number of highly interconnected online documents about this topic.  In fact, when searching on <a id="qqxd" title="Yahoo!" href="http://search.yahoo.com/search;_ylt=?p=ajax">Yahoo!</a> these are the only results one receives (all searches performed February 14th 2011).  If we happened to be searching for one of the other meanings we'd need to adjust our query.  When searching on <a id="pldd" title="Google" href="https://encrypted.google.com/search?hl=nl&amp;q=ajax">Google Netherlands</a> we end up with the opposite problem and all the results relate to the Amsterdam soccer team.  However, when searching on <a id="i20o" title="Google" href="https://encrypted.google.com/search?hl=en&amp;q=ajax">Google English</a> we see a result about the Amsterdam soccer team and a town in Calgary mixed into the top 10.

When addressed in a more general Artificial Intelligence setting, as opposed to the Information Retrieval setting we're focusing on here, this problem is occasionally referred to as the "Paris Hilton problem."  Is a searcher who enters this query interested in the woman or the Parisian hotel? Although the results are dominated by web sites about the Hilton heiress, <a href="https://encrypted.google.com/search?q=paris+hilton">Google</a> does provide one site, at rank 9, satisfying those of us seeking to book a stay at the Hilton Arc de Triomphe Paris.

Recently information retrieval research has started to put more focus on addressing the problem of ambiguous queries.  The primary solution has been to alter the search result list so that our top results not only reflect highly relevant results, but results that cover the multiple meanings a query could represent -- to <em>diversify</em> the search results.  This is analogous to the reinforcement learning strategy of "exploit and explore" in which we make what appears as a sub-optimal decision so that we can gain information and make better decisions in the future.  There is also a relationship to risk management in portfolio theory: by cautiously covering multiple meanings we can reduce the worst case outcome when we incorrectly predicted the user's intended meaning.  The results of Google English appear to have incorporated something of a diversification strategy.

A key challenge in result diversification is to determine what the underlying topics of the returned search results are.  Knowing our results' topics will teach us how to diversify our results.  We recently presented work on precisely this topic, the image below shows a summary of the system we built [2].
<p style="text-align: center;"><img class="aligncenter" style="padding-top: 10px; padding-bottom: 10px;" src="http://d.helioid.com/images/diversify.png" alt="Diversification System Diagram" width="529" height="163" /></p>
The basic strategy is to apply a topic modeling algorithm to the fetched results and then use a reordering algorithm to ensure we highly rank both relevant documents and topics with a high probability of being in different topics.  The specific implementation we design used Probabilistic Latent Semantic Analysis to generate topics but any other algorithm (e.g. Latent Dirichlet Allocation, Correlated Topic Model, etc.) could be substituted.

The inquisitive reader might be wondering, well, if I know the topics I like and the search engine knows the topics representing documents, why bother diversifying search results, why not simply provide me with documents related to my preferences?  Relating this back to the previous post about search users' <a id="y8.x" title="topic preferences" href="http://blog.helioid.com/2011/01/are-our-preferences-in-a-sub-space/">topic preferences</a>, there is clearly a viable path of research here.  We look forward to presenting details about our work integrating these techniques.

References

[1] M. Sanderson. <a id="ggfk" title="Ambiguous queries: test collections need more sense" href="http://www.seg.rmit.edu.au/mark/publications/my_papers/fp596.pdf">Ambiguous queries: test collections need more sense</a>. SIGIR '08, pp. 499-506, 2008.

[2] P. Lubell-Doughtie and K. Hofmann. <a href="http://peet.ldee.org/projects/graduate/result-diversification/">Improving Result Diversity using Probabilistic Latent Semantic Analysis</a>. DIR '2011, pp. 24-27, 2011.
