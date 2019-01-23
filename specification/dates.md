# Dates
It is important to record and preserve dates in the context/culture of the event. For example if a native american was born and lived using the Mayan calendar system, we want to preserve those dates rather than simply convert them to a calendar system broadly used today such as the [Gregorian](https://en.wikipedia.org/wiki/Gregorian_calendar) calendar. Doing such would lose context, information, logic, and meta data that person was originially identified with.

The display of the date is left up to the rendering process each software product chooses to use. In some cases a calendar conversion calculation would need to be implemented.

Multiple dates can be stored for an event ensuring that the origianl will be preserved while also accomodating a more convenient date that is more widely understood today. This gives the software product the option of which date(s) they want to take advantage of, and ease the burden of doing date calculations. The most relavent date should be the fist item in the array, usually the Gregorian.

Gregorian dates are notated as Day/Month/Year (1/12/2000). Time is notated as Hours:Minutes:Seconds:Milliseconds (03:34:21:500)

```
"date": [
	{
		"value": "1/6/1965 03:14:00",
		"date": "1/6/1965",
		"time": "03:14:00",
		"zone": "America MST",
		"calendar": "gregorian"
	},
	{ 
		"value": "2 Manik' 0 Pop",
		"calendar": "mayan"
	},
	{ 
		"value": "甲子",
		"calendar": "rural"
	}
],
```