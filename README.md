# Timeline
A utility for creating SVG timelines from JSON.  

### Example

You will be able to create timelines that look like this:

![simple timeline example](http://jasonreisman.github.io/timeline/simple_timeline.png)

from JSON that looks like this:

```JSON
{
	"width" : 750,
	"start" : "Oct 8 2015",
	"end" : "Oct 15 2015",	
	"num_ticks" : 14,
	"tick_format" : "%b %d, %Y - %I:%M%p",
	"callouts" : [
		["ABC easy as 123", "Oct 14, 2015 3pm"],		
		["Midnight Event A", "12am Oct 10, 2015", "#DD0000"],
		["Noon Event A", "12pm Oct 10, 2015"],		
		["5pm Event A", "5pm Oct 10, 2015"],				
		["Something amazing happening", "Oct 11, 2015"],
		["Awesome Event B", "Oct 12, 2015", "#DD0000"],
		["C", "Oct 13, 2015"],
		["Event E", "Oct 14, 2015"]
	],
	"eras" : [
		["Era 1", "12pm Oct 8, 2015", "3am Oct 12, 2015", "#CD3F85"],
		["Era 2", "8am Oct 12, 2015", "12am Oct 15, 2015", "#C0C0FF"]
	]
}
```

### Prerequisites
You must have a python 2.7 installation and install the Python packages `parsedatetime` and `svgwrite`.

### Usage
```./make_timeline.py <input json filename> > <output svg filename>```
