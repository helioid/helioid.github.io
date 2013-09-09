---
layout: post
title: Simple Fast Text Categorization in Ruby
categories:
- General
tags: []
status: publish
type: post
published: true
meta:
  _edit_last: '1'
---
It's been a while since our last update, indicating a transition for the Helioid team, and we thought it was time for an update on what we've been up to. As we've noted in many past posts, our dedication to Helioid came from our own frustration in exploring new topics of interest and a desire to provide a tool that helped filter out the proverbial needles from the proverbial haystacks by categorizing search results. We remain committed to helping that long tail of exploratory searchers and to working with and supporting the community of innovators in the search space.

So, we're pleased to announce the release of a <a
href="https://github.com/helioid/categorize">categorization library</a>,
installable as a Ruby gem, which developers can use to categorize search
results, or any other document collections they'd like to add a layer of
structure to, in order to support more intuitive navigation.  For example, the
cluster model categorizes the first five summaries for a <a
href="http://www.helioid.com/searches/web/q/helioid">"helioid"</a> search as:

> "search refinement"

> "floor silicon"

> "word difficult"

These could use some work.

The gem includes <a href="https://github.com/helioid/categorize#basic-usage">usage examples</a> and a walkthrough of how to customize the gem to your needs. Developers can apply categorize using <a href="https://github.com/helioid/categorize#use-an-alternative-model">alternative clustering models</a>, and the gem includes a simple bag-of-words clustering algorithm, as well as both hierarchical and non-hierarchical Ward clustering based algorithms. Developers can customize the basic parameters of whichever categorization model they use, such as the maximum number of clusters, and the minimum support threshold for clustering. We're excited to see the range of sites and alternative search tools the developer community applies Helioid's categorization to using this library.
