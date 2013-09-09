---
layout: post
title: Google's SearchWiki as a step towards more user control
categories:
- General
tags:
- google
- personalization
status: publish
type: post
published: true
meta:
  _edit_last: '1'
---
Google recently released their new SearchWiki feature which allows users, who are logged into a Google account, to rearrange search results (by clicking on arrows that move them up or down one slot), remove results from the returned list, and comment on results (all comments are made public).  More information is in this Google "blog article":http://googleblog.blogspot.com/2008/11/searchwiki-make-search-your-own.html.

It's encouraging to see Google taking user responses into account.  It has always been our opinion that this is something sadly missing from the mainstream search world.  Google also states that the results' movements, removals, and comments will not be used as input to their search algorithms.  Well, at least not yet.

Google knows that customization specific to the searchers individual information is important to delivering relevant results.  In this "blog article":http://googleblog.blogspot.com/2008/07/more-transparency-in-customized-search.html about customized search transparency they detail the introduction of messages that inform users when a search has been customized based on location, recent searches, or web history (for those with Google accounts).  Using the links from these messages you can also re-search removing the specified customization that was used as input to the results they provided.

Whether meant this way or not, the option to remove customization is an important step towards users controlling the way Google's algorithms function.  For a relatively unlikely example, suppose you're in New York using "Tor":http://tor.eff.org/ to proxy your connection and the exit node is in San Francisco, so Google thinks you're in San Francisco.  Your search for "new york bagel" might bring up the "New York Bagel" café in Mill Valley, which is entirely irrelevant.  You can then tell Google to strip out their local search and re-searching will bring you the relevant results you want.

The sort of customization offered by SearchWiki is in a different vein.  You're not meant to interact with or influence the search algorithm.  If you perform a search and then start removing results you can continue until there are none left.  This also means that if you perform a search for "new brunswick":http://www.google.com/search?q=new+brunswick, remove all the results mentioning Canada, and then go on to the second page of results, you'll still get a whole bunch of results mentioning Canada.  Given your actions, it is unlikely you're looking for information about Canada's New Brunswick province, but after having removed all those irrelevant results Google will still present more of them.

One way Google could improve this problem is to bias their returned results after you begin removing and reordering your results.  If they end up getting things wrong the user should be able to tell them so explicitly through customization options.  The user should also have an option to turn this functionality off – or compare results with it on and with it off – if they wish.  Helioid's algorithms can tell when they are getting things wrong _implicitly_ by looking through the results the user removes and the way the user navigates through the returned results.

It's great to see Google innovating.  There's a lot more that can be done.
