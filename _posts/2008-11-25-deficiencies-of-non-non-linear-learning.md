---
layout: post
title: Deficiencies of non-Non-linear Learning
categories:
- General
tags:
- learning
- models
status: publish
type: post
published: true
meta:
  _edit_last: '1'
---
Non-linear learning is at the heart of the algorithms that underlie what makes Helioid's search effective.  To examine non-linear learning let us first define the term in contrast with linear learning.  (I would like to briefly note that these definitions, though culled from machine learning and logic literature, are primarily my own and I expect some to disagree with them).

Linear learning occurs when each step in a procedure depends solely on deductions made from the previous steps.  Furthermore, the deductions must be valid according to some set of rules.  To take the example of modus ponens from formal logic, suppose we know '"it is daytime"' and that 'if "it is daytime" then "we can see the sun"'.  Given a standard model theory we may deduce, "we can see the sun" by detachment.
In search, the reasonable assumption is made that 'if "Item A appears above Item B in search results" then "Item A is more relevant than Item B"' and Item A should be displayed with more prominence to the user, normally closer to the top of the list of search results.  This line of reasoning is perfectly acceptable but there are times when it quickly runs into trouble for the searcher.

Suppose I am writing music visualization software and I need information about the Processing graphics libraries' particle system.  My first query might be, "processing graphics library particle system".  Try it on "Google":http://www.google.com/search?q=processing+graphics+library+particle+system.  The results I get aren't bad for what I was looking for.  The 6th entry links to a "page on processing.org":http://processing.org/reference/libraries/ from which I can find another link to Jeffrey Traer Bernstein's "page":http://www.cs.princeton.edu/~traer/physics/, which has a particle system library for Processing.

But, going back to Google's results, a look through the top 500 finds no direct link to Traer's page!   Looking through the results the problem may be phrase based.  There are lots of results for "graphics" and "library" and "particle" and "system".  Being a well trained Google user I'd wrap "particle system" in quotes and "re-search":http://www.google.com/search?q=processing+graphics+library+%22particle+system%22.  I also might switch "library" to "language" and try to find a phrase I could combine "processing" with.

But still I'd have no luck getting Traer's page within the top 500 results and most of the results would be irrelevant to my query (the two above linked queries were tested on November 24 2008).  One problem is that I can't interactively say, "this type of result is irrelevant, get rid of it."  I could add some exclusionary keywords or phrases to my query but that would require a good amount of guess work on my part.  I would need to find the right keywords or key-phrases to exclude and there is no guarantee I will be able to do this effectively or even helpfully.

Another problem is that I can't say, "this type is on the right track, give me more of these,"  without making adjustments to my query. The problem here is that when I make these adjustments to my query the initial work I've done in sorting through the results will be lost when my new results are shown.

Google's failure to present the user with relevant results stems from an inability to capture user feedback and implement a method for users to provide feedback.  The failure in part stems from the assumption that a user wants to go through their search results in a linear fashion.
Here are a couple ways in which Helioid's non-linear approach to searching helps solve this problem.

*1. Let the user tell the search engine what they want.*

The user knows when a result is irrelevant, and they should be able to get rid of it.  The user also knows when a result is relevant and they should be able to bias the algorithm towards results of this type.  Some users may know when an entire class of results is irrelevant (or relevant).  They should be able to bias their search results against (or for) showing results that are members of this class.  In the example given above I know I don't care about physics papers so, using Helioid, I can tell the search engine my opinion and it will bias the results is returns against them.

This is a non-linear method because the search results (the deductions) are being modified in a way that is inconsistent with the rules by which they were generated (the theory).

*2. Have the search engine learn from what the user does.*

In many cases it may be unnecessary for the user to explicitly tell the search engine what they want.  Going back to our "Processing library" example, after the user is seen ignoring all the pages related to all the academic papers it may be appropriate to assume the user is uninterested in them.  Maybe even ask the user if they'd like them to be removed.

For the same reasons as above this is another example of non-linear learning.

Assuming that the algorithm knows the answer tout court is a dreadful mistake.  The most important input to the algorithm should be the desires of the user as they are expressed in keywords and through actions.  If a user is found scrolling through multiple pages this is an _input_ and the search results should be adjusted to take this new knowledge into account.  Ignoring user input is the same as not adjusting your reefing after the wind shifts, you'll go off-course.
