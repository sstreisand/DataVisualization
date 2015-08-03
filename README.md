This is my Data Visualization Final Project
#Summary - in no more than 4 sentences, briefly introduce your data visualization and add any context that can help readers understand it
My data is statistics for degree-granting 4-year or above post-secondary schools in the United States. My data visualization shows the number of these in different states of the United states.  It also shows the number of institutions per population amount.  There are some states that have a lot of schools, but they don't necessarily have a high number of schools per population size.


My data is statistics for degree-granting 4-year or above post-secondary schools in the United States.  It is labelled by 

#Design - explain any design choices you made including changes to the visualization after collecting feedback

I downloaded data from the National Center for Education Statistics at http://nces.ed.gov/ipeds/datacenter/DataFiles.aspx from 2013.  I selected a subset of the data fields available, which includes state, region, Institutional Category (public/private non-profit/private for-profit), Carnegie Classification and Undergraduate Profile.
It contains statistics on admissions test scores, tuition, percent accepted, etc.

There was a lot of data and I needed to find a way to narrow down what I presented to show a story.  Instead of using the statistics, I did a summary count of institutions per state.
I found a bar chart example online and tried to fit that to my data.  It highlighted the moused-over bar and I added a tooltip.  That's what I started out with.
I had several sketches or ideas of how to improve:
* Use a map of the US, mouseover each state with summary data for different statistics
* Use a scatterplot with state on x axis and plot statistics on the y axis
* Plot average state statistics in a bar chart (similar to the count (length) I now have
* Color code bars by region of the country
* Use stacked bar chart breaking down different characteristics for each state (count of public/private/for-profit for example)

Here is my initial gist (it was slightly renovated from the initial design because I added the sort checkbox): [https://gist.github.org/sstreisand/85ab9c34324ea92fb185|Data Visualization Final Project Take 2]
#Feedback 
- include all feedback you received from others on your visualization from the first sketch to the final visualization
###First Feedback (from Google+):
Francis CorriganJul 7, 2015


 1
Reply
 
Nice start! I love the basic steel blue d3 bar chart. It's simple and beautiful. Maybe it's because I'm on mobile, but I can't see the x labels (states)... I need to tap each bar to see the data. I would include the labels. Also, I would sort the data by state in descending order so instantly I can tell which states are highest, which are lowest, and which are in the middle. 

Second observation is that I would be more interested in per capita data.... Perhaps something like 4 year degrees per square foot. Since CA and TX are huge states (by land mass) I would expect them to have more universities. However, if you did it by universities per square foot i would expect Massachusetts to be close to the top. Or maybe... Universities per capita would show something really cool? Either way, I think it adds a dimension to your graph.

Lastly, I saw your comment about making a map. Do it! Even if you don't use it, I found that I've learned a lot about d3 and JavaScript in general by grinding through the process of creating a map. Good luck and please share your visualization when it is complete!﻿

<The x labels don't show on bl.ocks.org unless you display in its own window, something about the frame size I suppose.  I added a checkbox to allow sorting data by highest to lowest.  I also added per capita data - per x of the population (I set x in my code), not per size.  I also added a map at the bottom.>

- I received feedback that I should sort it by number of schools per state so I added the sort checkbox and it sorts by number of schools per state.  
- I also received feedback to have a ratio of schools per population, so I added a pure population and a ration of schools per population as choices on the chart.

Other feedback included:
- include some more interesting info. For example, in your data there are religion/category divisions -- you can show this data by making staked bar-chart and/or include some (or most) of this information in popup.
-  Nice visualization! Maybe you could add a bottom such that you could switch from absolute to per capita, so that people that are interested in having the absolute value could also have it. Also, the title of the y axis should be horizontal. Visually is much more simple because that way you don't have to turn your head. A last thing I would recommend is to remove the ticks from the horizontal axis. Keep up the good work!﻿
-  This is really nice looking graph, but after scrolling the mouse, I found myself thinking "so what".  You could use this graph to tell a story about access to 4-year college.  Group the states by region and superimpose a line of population by state.   The x-axis labels are cluttered and can't be seen without opening it in a separate window.  Try using the 2 letter state abbreviations and see if that cleans things up.﻿

I also have a scatterplot that shows individual statistics for the schools mapped by state, but I didn't think that really showed anything interesting.

#Resources 
- list any sources you consulted to create your visualization
+ data from http://nces.ed.gov/ipeds/datacenter/DataFiles.aspx 
+ http://javascriptissexy.com/understand-javascript-callback-functions-and-use-them/
+ Map of US GeoJSON http://eric.clst.org/Stuff/USGeoJSON
+ https://leanpub.com/D3-Tips-and-Tricks
+ Alphabetic Sort: http://stackoverflow.com/questions/8900732/javascript-sort-objects-in-an-array-alphabetically-on-one-property-of-the-arra
+ http://stackoverflow.com/questions/15125920/how-to-get-distinct-values-from-an-array-of-objects-in-javascript
+ http://www.remkohde.com/2013/03/25/d3-binding-multi-dimensional-arrays-and-deep-nested-data/  
+ More sorting help from http://bl.ocks.org/mbostock/3885705
+ Positioning a Tooltip:  http://codepen.io/recursiev/pen/zpJxs
+ http://geoexamples.com/geoexamples/d3js/d3js_electoral_map/tooltipCode.html
+ From http://bl.ocks.org/mbostock/4573883 how to put in a scale
+ http://www.java2s.com/Code/JavaScript/Form-Control/Gettheradiobuttonselection.htm
+ Us-states.json comes from https://github.com/alignedleft/d3-book/blob/master/chapter_12/us-states.json
+ http://eyeseast.github.io/visible-data/2013/08/27/responsive-legends-with-d3/
