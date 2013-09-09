---
layout: post
title: Are our Preferences in a Sub-Space?
categories:
- General
tags:
- categorized search
- personalization
- topic models
status: publish
type: post
published: true
meta:
  _edit_last: '1'
---
The web is really big, but when one searches for information the topics they are looking for exist within a much smaller portion of the web.  A system that knows our individual preferences can optimize its document search, by starting this search from documents that we likely prefer.  Additionally, by learning and knowing our preferences, the system can improve its presentation of results by biasing document rankings towards documents which are similar in theme to documents we preferred in the past, or disambiguating our queries based on the interpretations we used in the past.

As an example of handling multiple meanings (polysemy), if we've searched for <em>leopard</em> and <em>tiger</em> we're showing an interest in something like the <em>large cats</em> topic, and when we search for <em>jaguar</em> we probably want the cat.  However, if we've recently searched for <em>lexus</em> and <em>bmw</em> our interest is likely in the <em>luxury cars</em> topic and when searching for <em>jaguar</em> we probably want the car.  Searching for <em><a id="oc:2" title="jaguar" href="http://www.google.com/search?q=jaguar">jaguar</a></em> using Google, on January 30th 2011, puts the car at the top &ndash; probably accurate in general but certainly not always.

This method can also be used to help with words whose meaning changes over  time (dynamic referents).  For example, if we search for <em>Rahm Emmanuel</em>, <em>Obamacare</em>, and then <em>US president</em> we're likely looking for <em>Barack Obama</em>.  But if we had searched for <em>Saddam Hussein</em>, <em>Dick Cheney</em>, and then <em>US president</em> the chances we are looking for <em>George Bush</em> are much higher than in the previous sequence of searches, and it would be worthwhile to highly rank some <em>George Bush</em> related results.

Performing these disambiguation tasks and other personalization techniques relies on coming to an understanding of the searcher's topics of interest.  To quantify the preferences of web users we'll begin by introducing a method to describe preferences that is understandable and useful.  We can consider user preferences as being broken down into a finite set of  "topics", each of which the user has a preference for.  For easy visualization, we'll take three topics: <em>Business</em>, <em>Sports</em>, and <em>Health</em> (inspired by <a id="y71b" title="Google News" href="http://news.google.com/">Google News</a>).  Let's consider a user who is moderately interested in <em>Business</em>, uninterested in <em>Sports</em>, and quite interested in <em>Health</em>.  We can represent each these interests on a separate line graph for each topic with something like the following:

<img class="aligncenter" title="Parallel Topics" src="http://d.helioid.com/images/fig1_parallel_topics.png" alt="" width="249" height="119" />

The large black dot indicates interest in a topic and the farther the dot is towards the right end of the arrow the more interested the user is in that topic.  We can then consider each topic as a dimension in 3-dimensional space and plot the user's topic preferences in this space with each axis as a topic:

<img class="aligncenter" title="Topic Space" src="http://d.helioid.com/images/fig2_space_topics.png" alt="" width="350" height="195" />

We now have a single black dot to indicate the user's topic preferences.  Tracing the distance from the dot horizontally left, to the green line,  we can determine the user's preference in the <em>Health</em>-dimension, tracing to the blue line vertically down, to the blue line, we can determine the user's preference in the <em>Business</em>-dimension.  The <em>Sports</em>-dimension is represented by the axis going into the page, the arrow helps us see the dot's distance in this dimension by tracing down and then diagonally along the orange line.

Now, back to web  search.  A convenient feature of breaking down user preferences by topics is that we can also break down a document's content by topics,  perhaps the dot above also represent the topics making up a document about health in the business setting, which mentions that sports can  contribute to health.  Given the divisions of a document into topics we can visualize our preferences by placing the documents we like in a  topic-space just as above.  (With an appropriate "distaste"  weighting we can also incorporate disliked documents into the same method.)

Before we become too excited about this new way to map our preferences, a fair question to ask is: do we even have significant and meaningful preferences in topic space?  That is, if we place the documents we like into topic space will they be clustered around some specific preferences or will they be more or less evenly distributed, and therefore not give us much useful information.  We can empirically answer this question by examining user clicks in a search engine log.

To test the topical distribution of preferences we took the documents clicked on by an anonymous user, broke these documents into 3 topics (for easy visualization), and plotted the documents in 3 dimensional space:
<div id="utf:"><img class="aligncenter" title="Personalized Topics" src="http://d.helioid.com/images/ls_personalized.png" alt="" width="400" height="372" />In this plot each dot represents a document and the color of the dot is to help us distinguish the location on the z-axis (into the page) &ndash; redder dots are closer and darker dots are farther.  We see that this user's clicked documents are located in a well defined sub-space of the  entire topic space, and within this sub-space form some additional clumps, i.e. they are not evenly distributed.  The dotted lines shown form a plane (a 2-dimensional surface or manifold) that is the best fit plane  (using regression) to the 3-dimensional points.</div>
This can be very useful information if we are helping the user look for documents.  Going back to <em>jaguars</em> for an example, suppose when we place documents about the cars <em>Lexus</em>, <em>BMW</em>, etc. in the topic space they end up in the far-top-right, and when we place documents about <em>leopards</em>, <em>tigers</em>,  etc. they end up in the close-bottom-left.  Given our model, this shows us that the user's preferences are near the big cats and we can surmise the user is more interested in big cats than luxury cars.  Then if this user searches for <em>jaguar</em> we will highly rank documents about jaguar the animal (apparently <em>panthera onca</em>).

The benefits of this sort of document reordering were tested in sketchily  formulated experiments and produced encourage, but inconclusive, results.  We stress that the benefit of this approach is not that we are simply providing documents similar to documents the user liked in the past.  The benefit is that we are providing documents similar to the topics associated with previously liked documents.  This is the nuanced, but essential, benefit of searching with an integrated topic models.

<strong>References</strong>
<ul>
	<li> A very accessible introduction to meaning in text is <a id="cwih" title="Geometry and Meaning" href="http://csli-publications.stanford.edu/site/1575864487.shtml">Geometry and Meaning</a> by Dominic Widdows.</li>
	<li>Research and figures taken from the draft paper <a id="r13_" title="Applying Diversity and Novelty to Personalized Search" href="http://peet.ldee.org/projects/graduate/personalized-search-topics/">Applying Diversity and Novelty to Personalized Search</a>, academic references are within.</li>
</ul>
