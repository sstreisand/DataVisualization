This is my Data Visualization Final Project
#Summary - in no more than 4 sentences, briefly introduce your data visualization and add any context that can help readers understand it
My data is statistics for degree-granting 4-year or above post-secondary schools in the United States. My data visualization shows the number of these in different states of the United states.  It also shows the number of institutions per population amount.  There are some states that have a lot of schools, but they don't necessarily have a high number of schools per population size.
The file index8.html has my final project in it.

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

I tried both bar and scatter plots and liked the way the bar plot worked with the transition.  The blue color was used by others and it seemed to be pleasing.
The red mouseover contrasts nicely to help the selected state stand out.  I am not an artist and stuck with colors that seemed to work from the examples I found online.  
I changed some of the spacing and formatting to look better.  I added the story stages to guide the viewer in the story keeping the control form hidden (opacity 0)
until the viewer was able to guide the story, but kept it there so the form elements were available for control.
I kept the data unsorted first, because it was hard for me to find states I was looking at if they were not in alphabetical order in the chart.  I then sorted them so I could see trends.
For example, if you are looking to see how your state compares, looking alphabetically helps to find it.  Then you can follow it in the sorting to see where it
goes in sorted order.  I decided to do it by state, not region, because that gave more granularity - I would not have found the uniqueness of Vermont if I did it by region.
There were a lot more things I wanted to do but I don't have time to do them all.

Here is my initial gist (it was slightly renovated from the initial design because I added the sort checkbox but forgot to save the original): [https://gist.github.org/sstreisand/85ab9c34324ea92fb185](Data Visualization Final Project Take 2)

Here is an updated gist where I added the other data values - population, and number of Institutions per 100,000 of population.  You can sort by value (when checked) or else states are sorted alphabetically.
http://gist.github.org/sstreisand/968d2752a1c0b1ce6dde/

In my later iterations I added the choropleth based on feedback that said to try it even if I didn't use it. I thought it was good for exploratory
analysis to see if there were any patterns in locations/regions and kept it so the viewer could see for him/herself.  I added a checkbox to show the map and in final iteration either the map shows or the chart shows.
I added a story so that it starts off by guiding the viewer through charts (sorted and unsorted) and maps and then allows the viewer to select their own.

After my first evaluation, I added a scatterplot of population vs. per capita # of schools by state (index9.html) but I'm not sure it adds
anything to the story.
#Feedback 
Include all feedback you received from others on your visualization from the first sketch to the final visualization
- I also included a word document with all feedback copied in case the reviewer could not read the links below

###First Feedback (from Google+):
Here is a link to the feedback thread on Google+:  https://plus.google.com/117771238554345892990/posts/ifm6kk1GcbE

First feedback:
```
Francis ...
Jul 7, 2015
Nice start! I love the basic steel blue d3 bar chart. It's simple and beautiful. Maybe it's because I'm on mobile, but I can't see the x labels (states)... I need to tap each bar to see the data. I would include the labels. Also, I would sort the data by state in descending order so instantly I can tell which states are highest, which are lowest, and which are in the middle. 

Second observation is that I would be more interested in per capita data.... Perhaps something like 4 year degrees per square foot. Since CA and TX are huge states (by land mass) I would expect them to have more universities. However, if you did it by universities per square foot i would expect Massachusetts to be close to the top. Or maybe... Universities per capita would show something really cool? Either way, I think it adds a dimension to your graph.

Lastly, I saw your comment about making a map. Do it! Even if you don't use it, I found that I've learned a lot about d3 and JavaScript in general by grinding through the process of creating a map. Good luck and please share your visualization when it is complete!﻿
```

<The x labels don't show on bl.ocks.org unless you display in its own window, something about the frame size I suppose.  I added a checkbox to allow sorting data by highest to lowest.  I also added per capita data - per x of the population (I set x in my code), not per size.  I also added a map at the bottom.>


- I received feedback that I should sort it by number of schools per state so I added the sort checkbox and it sorts by number of schools per state.  
- I also received feedback to have a ratio of schools per population, so I added a pure population and a ration of schools per population as choices on the chart.

Other feedback included:
- include some more interesting info. For example, in your data there are religion/category divisions -- you can show this data by making staked bar-chart and/or include some (or most) of this information in popup.
-  Nice visualization! Maybe you could add a bottom such that you could switch from absolute to per capita, so that people that are interested in having the absolute value could also have it. Also, the title of the y axis should be horizontal. Visually is much more simple because that way you don't have to turn your head. A last thing I would recommend is to remove the ticks from the horizontal axis. Keep up the good work!﻿
-  This is really nice looking graph, but after scrolling the mouse, I found myself thinking "so what".  You could use this graph to tell a story about access to 4-year college.  Group the states by region and superimpose a line of population by state.   The x-axis labels are cluttered and can't be seen without opening it in a separate window.  Try using the 2 letter state abbreviations and see if that cleans things up.﻿

I also have a scatterplot that shows individual statistics for the schools mapped by state, but I didn't think that really showed anything interesting.

I finally was able to re-enter the forums and received this feedback: (thread at https://discussions.udacity.com/t/requesting-help-and-feedback-on-my-project/27306 )

```
Hi Susan,

I am no d3 expert :), still learning....but my 2 cents regarding the tooltips are as follows:

I suggest keep the tooltip size constant, making the width as long as the longest state name i.e.'District of Columbia' and adjusting height that could include 4 rows (state, Institutes, Pop. and Pop. density).

Add Keys before values for ease of understanding (image attached as a suggestion).
```
-----
```
I like it! Other than the issues you mentioned, my only comment is that the vertical label on the y-axis that's just inside the plot area will overlap with the first bar. Perhaps you could move the label outside the plot area?

If you figure out how to dynamically size the popup boxes to fit text, please let me know! smile

And I completely sympathize with you on "It seems everytime I try to fix something I wind up breaking the whole thing." I know the frustration!
Good Luck!

Other than that, your project looks good to me and I like the way transition takes place when sorting is checked.
```
I added the tooltip idea to make it as large as the largest location and added keys before values and put the vertical label outside the plot area.

###Feedback from first review
https://review.udacity.com/#!/reviews/38811 was the feedback from my first review.  I tried to incorporate a variation of the scattterplot that was suggested.
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
+ http://stackoverflow.com/questions/3674265/is-there-an-easy-way-to-clear-an-svg-elements-contents
+ http://stackoverflow.com/questions/21838013/d3-choropleth-map-with-legend
+ http://stackoverflow.com/questions/29325040/get-value-of-checked-radio-button-using-d3-js
+ http://stackoverflow.com/questions/9522019/how-to-check-a-particular-radio-box-in-a-group-using-javascript
+ Bar chart help: http://bost.ocks.org/mike/bar/3/
+ Loading multiple files: http://www.jeromecukier.net/blog/2013/11/20/getting-beyond-hello-world-with-d3/
+ Updating bar chart: http://stackoverflow.com/questions/22052694/how-to-update-d3-js-bar-chart-with-new-data
+ Help on scatterplot from Nikolay's example: http://bl.ocks.org/nikolay-shenkov/raw/3c05dd0ec4b86cdbb968/2