---
id: 851
title: Data Visualization (Don Baracskay)
date: 2015-03-13T22:03:14+00:00
author: donbaracskay
layout: post
guid: http://lindsaythomas.net/hon2210/?p=851
permalink: /2015/03/13/data-visualization-don-baracskay/
categories:
  - Machine Reading
---
My data visualization can be found at ManyEyes.

<http://www-969.ibm.com/software/analytics/manyeyes/#/>

It is currently at the top of the category latest in Visualizations, but this will likely change, so it will most likely be found farther down the list.  If not, ManyEyes has a search engine, and the visualization is entitled “Only Revolutions (Keywords).”

&nbsp;

It is an attempt to quantize and demonstrate the connections between key words in the novel, based on the frequency of said words in proximity to one another and throughout the text as a whole.  I used AntConc’s collocate function to obtain the aforementioned frequencies, and then used Voyant to get the relative frequency of each original word.  I combined these word per word (one excel file for each so I now have 20+) and used a function that took the frequencies and generated a relative score for each word.  I then created a master data set for each of the words in the visualization and standardized and imported the data to the master set.  This was then uploaded to ManyEyes.

This long and rather drawn out process, however, did not create the visualization that I intended.  I had originally hoped to use Gephi or Cytoscape to show how much each word relates to other words, which is what my visualization does, but does so in an unclear way.  To begin, only a certain amount of data can be held within the ManyEyes chart (hereafter: chord diagram), because the diagram can only be a certain size and some words are obscured unless one checks the legend.  Also ManyEyes does not allow one to change colors, a factor that is extremely irritating, as I wanted to use colors that “go” with the words (ie yellow for Hailey, gold for gold).

It does, however, do a good job of quantifying the data.  The thickness of each curve represents how much each word correlates to another.  A lack of curve shows little to no correlation, whereas a thick curve shows great correlation.

The visualization is an attempt to show the metaphors of the book in context with one another.  Using the correlation between two words allows one to see further into each word than simply reading the text.  Unfortunately, it would be best described as a proof of concept.  With better tools, the visualization could show trends that reading the book might not yield.

An example of this deals with the word hope.  We all know that throughout the book there are multiple entities that have “hope” in their names, and in the analysis the word new showed the greatest correlation to hope.  The second greatest correlation was the word “no.”  As in “No Hope.”  After reading the text, one realizes that Sam and Hailey were doomed to die so that each cycle would begin again, and thus they idea that they have no real hope fits in.

In spite of this, the visualization could not contain hope simply due to size constraints (hope was not the only word to reveal interesting connections), and it now serves to show major trends in the book’s words.  An improvement would seek to use the existing data and a plethora of other words in something more like a network style.