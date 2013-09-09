---
layout: post
title: If Microsoft's Thumbtack was Intelligent
categories:
- General
tags:
- microsoft
- personalization
- visualization
status: publish
type: post
published: true
meta:
  _edit_last: '1'
---
In early December Microsoft Live Labs released "Thumbtack":http://livelabs.com/blog/introducing-thumbtack/, which is said to: "[use] machine learning and natural language techniques to understand the information you give it."  Looking through the interface one notices some interesting tools.  Such as a gadget that creates plots based on attributes of the items you collect and a "Layout Gadget" that I assume creates layouts but currently appears to only work with "IE7":http://thumbtack.livelabs.com/FAQ.aspx.  Intelligent parsing of information, on demand analysis, visualization, there are great ideas here.  The unaccomplished obstacle is how to allow users access to these in an intuitive and simple fashion.

The improvements that could make Thumbtack a more useful tool include:

*1. Automatically parse attributes in content added to Thumbtack.*

bq. In a "FAQ video":http://video.msn.com/?mkt=en-US&playlist=videoByUuids:uuids:fa6082f9-a8e0-4067-9c32-53ef1ae4ab42&showPlaylist=true&from=msnvideo it says that Thumbtack can automatically create properties from the attributes.  How to make this happen is unintuitive and the video later goes on to say that the attributes for the automobile feature plots it creates have been added manually as name (key) value pairs.  Having a properties gadget that actually presents an interface asking users to add properties as "name" and "value" pairs is fine in a debugger (or, in this context, as an advanced option) but this invites confusion and estrangement in a user interface.

bq. When a user adds content, Thumbtack should automatically parse that content into keys and values, as sets, or into another most useful representation (maybe a graph).  If the parse gets things wrong the user should be able to change the values or labels, and the parsing engine will learn and hopefully know better next time.  If the parsing engine's at a complete loss it can prompt the user for interactive guidance.

bq. With this capability built in the information would be much more useful to the user.  Because newly added information would be quickly integrated into existing information through the parsed metadata, the user would explicitly see the value of adding and correctly categorizing new information.  Additionally, the boundaries and definitions of user created categories would likely become more clearly defined.

*2. Integrate Thumbtack into web search.*

bq. The Thumbtack interface appears to be completely divorced from web search.  The interface has a text field labeled "search" in the upper right that does not search the web but instead searches over items already present in Thumbtack.  One of the primary times that users need to categorize and keep track of web information is when they are conducting searches, whether goal directed or exploratory.

bq. Thumbtack could be integrated into Microsoft's Live Search "API":http://msdn.microsoft.com/en-us/library/bb251794.aspx so that search results are displayed in the Thumbtack canvas and incrementally parsed for properties as the users looks through the results.  Search results brought into the interface could be compared, arranged, and saved all while learning algorithms run in the background to determine what new information and what types of organization would be most helpful to the user.

*3.  Give the Thumbtack "bookmarklet" more features.*

bq. Another "video":http://video.msn.com/?mkt=en-US&playlist=videoByUuids:uuids:6a905d98-0332-4c3f-8b25-75737cd9b675&showPlaylist=true&from=msnvideo demonstrates the "bookmarklet" that pops up over web pages so that while browsing you can add information into thumbtack.  Unfortunately, this tool can only be used to add copied content, a title, and tags to a specific collection (items in Thumbtack are grouped into collections).  Some things a user may want to do is add their content to more than one collection, assign some special properties to their content, maybe even share their content on the spot, or find things similar to this piece of content.

bq. In addition to giving the user more options in terms of how they treat the content they are adding, the tool would be very useful as an "inspector" palette for the current page.  It could display information about the current page and show how it relates to items already in your Thumbtack collections.  Microsoft Live Search data about the current content could be pulled up and the user could use this to explore similar content or narrow in on the current content.

bq. Users should also be able to use the Thumbtack's gadgets from within this popup.  Maybe they want to see a quick plot of this content integrated into their existing collections, or maybe they want to see how adding this content would change the layout of already existing content.  Forcing the user to switch between to environments is unnecessarily burdensome.

Microsoft Thumbtack is an impressive tool with a lot of potential.  If it was given a more intuitive interface and a clear direction it could be very useful.  Sadly, it seems that after its release it's slowly drifting into obscurity.
