A timeline chart for d3
-----------------------

This chart shows events, that have a defined start and/or end
in the time continuum in form of a timeline or timechart.
Events can be instants (one date only) or intervals (start date
and end date).

The timeline consists of two bands.

The upper band shows the timeline items with data within the selected timeline interval.
The lower band is the navigation band; it just shows the distribution of the items.
The numbers in the lower band show the start, the length, and the end of the selected interval, respectively.
Click on the lower band and drag to create a brush and select an interval.

Click on the brush and drag to move the interval.
Click on the left or right border of the brush and drag to resize the interval.
Click on the lower band outside the brush to restore the original view.
Mouseover an item to show a tooltip.


Acknowledgements
----------------

This work was inspired by

'Simile Timeline' by 'David François Huynh'
(http://www.simile-widgets.org/timeline/).
'Swimlane Chart using d3.js' by Bill Bunkat
(http://bl.ocks.org/bunkat/1962173) and


The file structure
------------------

Any csv data file with the following line structure will do:

start,end,label
...,...,...

The first line contains the field names.
The field names 'start', 'end', and 'label' in the first line are required.
The following lines contain the data.

Intervals have a 'start', an 'end', and a label.
The following example describes the lifespan of the philosopher Kant:
1724,1804,Kant

Instants have a 'start', an EMPTY 'end', and a label.
The second comma is required to mark the 'end' field
and to designate this event as a point. The following example
gives the publication date of the 'Critique of Pure Reason' by Kant:
1781,,Critique of Pure Reason

Optional additional fields (i.e., 'description', 'image', 'link', etc.)
are not used in this version, but will be in future versions.

'start' and 'end' either conform to the ISO data format YYYY-MM-DD
or contain full years (that is: with century).
BC dates and dates between 0..99 AD are handled correctly.
For more information on 'start' and 'end' see the
comment of the function 'parseDate'.
'label' ist a plain string. Example:

start,end,label
800 BC,701 BC,Homer
4 BC,65,Seneca
55,135,Epictetus
1469,1527,Machiavelli
1781,,Critique of Pure Reason
...


Limitations
-----------

I have developed this version as an exercise to learn a little bit of d3
and as a proof-of-concept for doing timelines.

This timeline doesn't look especially 'pretty'. I have chosen theses items
(some poets and philosophers, some philosophical works) to show how a relatively
long time span is displayed and how BC dates are handled.
The dates are from the English Wikipedia
Shorter intervals make for 'nicer' timelines, as you can see for yourself,
if you use the brush.


Create your own timelines
-------------------------

To create your own timeline, you need

1.  A data file (see 'The file structure' above).

2.  The file 'timeline.js'; download and put into your working directory
    or on your path.

3.  The file 'timeline.css'; download and put into your working directory
    or on your path; change settings according to your preferences.

4.  Use 'index.html' (without comments) as a template
    and put in your filenames and paths.
     

Feedback
--------

I'm still a d3 newbie. So feedback on doing things more the 'd3 way' is very welcome.
Comments, suggestions, and bug reports are welcome, too.
