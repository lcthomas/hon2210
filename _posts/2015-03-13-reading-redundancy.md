---
id: 782
title: Reading Redundancy
date: 2015-03-13T17:53:45+00:00
author: Marshall
layout: post
guid: http://lindsaythomas.net/hon2210/?p=782
permalink: /2015/03/13/reading-redundancy/
categories:
  - Machine Reading
---
Undoubtedly, throughout the novel(s), Sam and Hailey share a lot of the same reading material. The question of how much is what I wanted to portray visually. Admittedly, I almost immediately (I did look into other methods) jumped at the opportunity to exercise my skills in programming (Ruby, if one should care to know) to perform the analysis. This rewarded me with the flexibility to look at the data how I wanted to see it, and also let me fine tune some of the parameters to my liking.

Initially, I composed the script to do a character-by-character analysis of each line. That is, it would first see if the characters at index (position) one matched up, then it would look at position two, and so forth. Of course, the question you may be thinking now is what if the comparison was only off by one character? This strict analysis of each line is also aided by a looser word match analysis. While analyzing Sam&#8217;s line, the script would note the words that he used. When looking at Hailey&#8217;s corresponding line, the script would look into the collection of words Sam used and see if it lay within there. Following the matching process, each line is assigned a &#8216;similarity&#8217; value that ranges from zero to one. I played with the weights for the character and word analysis and even considered dropping the character analysis entirely, but I thought it would be valuable to the visualization if the script increased the similarity value if the lines matched even more than from a basis of used words.

So, what&#8217;s the result?

<div id="attachment_795" style="width: 310px" class="wp-caption aligncenter">
  <a href="http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-5.40.32-PM.png"><img class="wp-image-795 size-medium" src="http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-5.40.32-PM-300x195.png" alt="Screen Shot 2015-03-13 at 5.40.32 PM" width="300" height="195" srcset="http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-5.40.32-PM-300x195.png 300w, http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-5.40.32-PM-100x65.png 100w, http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-5.40.32-PM-150x97.png 150w, http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-5.40.32-PM-200x130.png 200w, http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-5.40.32-PM-450x292.png 450w, http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-5.40.32-PM-600x390.png 600w, http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-5.40.32-PM-900x585.png 900w, http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-5.40.32-PM.png 934w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    Redundancy in the novel(s). It looks better if you click on it.
  </p>
</div>

&nbsp;

On the horizontal axis is, basically, the progression of the novel. I chunked the novel into 36 sections because it was sufficient for these purposes and because the number of lines (6480) is cleanly divided by it. The first section is the very beginning of the novel and section 36 is the very end of the novel. The vertical axis contains the similarity (dubbed &#8216;likeness&#8217; in the label) calculated using the method explained earlier.

The graph has four lines for a reason. The most important line is the thick, blue line that sits below the thinner lines. At first, I only cared about the average similarity amongst all lines present in the young couple&#8217;s story. That value is what the blue line represents. It was not before too long that I was curious about how similar lines were that matched 25% or more (according to my weighted percentages). To put it simply, the red line does not factor in lines that had a similarity value less than .25. It&#8217;s a similar story for the other two lines. What I find most interesting in the comparison of these lines is the discrepancies between them. For example, in the blue line (all text) there is a sharp spike following the dip in section two. This spike is not nearly as noticeable in the other lines.

Line graphs have always been my favorite kind of graph, and the decision to use it for mapping out this data was a natural decision since time is an important element to the book. The thickness of the lines themselves were by my design. Although I could have left them as simple one-point, thin lines, I wanted them to better communicate the amount of data that went into making that line. I decided against using percentages on the y-axis eventually because I feel like using percentages enforces the idea that these are exact numbers while my calculations were not as in-depth as I would have liked them to be (time constraints).

In addition to the line graph shown and explained above, I also produced another graphic.

<div id="attachment_786" style="width: 310px" class="wp-caption aligncenter">
  <a href="http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-12.18.18-PM.png"><img class="size-medium wp-image-786" src="http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-12.18.18-PM-300x68.png" alt="Similarity calculations for EVERY line in the novel(s)." width="300" height="68" srcset="http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-12.18.18-PM-300x68.png 300w, http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-12.18.18-PM-100x23.png 100w, http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-12.18.18-PM-150x34.png 150w, http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-12.18.18-PM-200x45.png 200w, http://lindsaythomas.net/hon2210/wp-content/uploads/sites/7/2015/03/Screen-Shot-2015-03-13-at-12.18.18-PM.png 425w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    Similarity calculations for EVERY line in the novel(s).
  </p>
</div>

Tiny? It is. Hard to read? Yeah. I produced this graphic to supplement my primary visual because I think it is important to show the data that the graph given above is derived from. The axes for this scatterplot are pretty much the same as in the first graphic. The only difference is that the x-axis is divided into the line numbers. There are exactly 6480 lines in each story. One represents the first lines given, and 6480 represents the last lines given. Mondrian was more direct in giving me exactly what I wanted to see in this graphic, so its output is the one you see above. I had to squeeze the graph into such tiny dimensions because simply increasing the size of the plots was not as visually appealing. It makes it very easy to see what I believe is a very nifty trend Danielewski implemented. In the first half of the novel, everything before the obvious gap near the middle, the lines that were different were very different. This is shown as the plots hugging the x-axis. In the last half, this kind of activity is not observed.

There&#8217;s a lot more I&#8217;d like to mention, but I&#8217;ll leave it as an exercise to the reader to find interesting aspects to my visuals, as I am slightly over my word limit&#8230;

Should anyone curious enough care, my script can be found [here](http://mardev.net/downloads/analyze.rb "Only Revolutions Analysis Script").