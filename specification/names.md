# Names
Representing a person's name in a data structure seems like a simple task. When you introduce the need to represent the name taking into consideration language, cutlure, and context it becomes more difficult.

In addition it's emparative that each name be represented with uniqness, having no ambiguitty with similar yet different names. This is what the Composite Clinical Data Dictionary (C2D2) naming standard allows us to do. It is done by breaking down each name to its atomic level, and building a fully qualified name by putting it's atomic parts together in an elegant and simple fashion.

This specification currently allows all current names to be uniqely defined, and allows the specification to infinatly grow as new situations are encountered.

The C2D2 specificaiton was created by [Richard Dick, Ph.D.](http://www.cavanaughconsulting.org/richard-dick-ph-d/)

[Atomic Name Part Defintions](#Atomic-Name-Part-Defintions)

### Simple Name Example
An overly simplified (but not recommended) way of representing a person's name

`"name": { "value": "Sarah Jane Williams" }`

### Complex Name Example
A more complicated example of representing a Hispanic name with the complexities of the multiple surnames along with an academic title.
```
"name": {
	"value": "Rosa María Muñoz Gómez",
	"D-NAM": [
		{
			"sequence": "FN[0],FN[1],LN[0],CP-MN[0]",
			"value": "Rosa María Muñoz Gómez"
		},
		{
			"sequence": "FN[0],FN[1],LN[0],CP-MN[0]",
			"value": "Rosa María Muñoz de Gómez"
		},
		{
			"sequence": "FN[0],FN[1],LN[0],MLN[0],CP-MN[0],SUF[0]",
			"value": "Rosa María Muñoz Izquierdo de Gómez, Ph.D.",
		}
	],
	"parts": [
		{
			"FN": [
				{ "value": "Rosa" },
				{ "value": "Maria" }
			],
			"LN": [
				{
					"value": "Muñoz",
					"modifier": { "date": "6/17/1962", "event": "birth"	}
				}
			],
			"SUF": [
				{ "value": "Ph.D.",	"type": "Academic" }
			],
			"CP-MN": [
				{ "value": "Gómez" }
			],
			"MLN": [
				{ "value": "Izquierdo" }
			],
			"PLN": [
				{ "value": "Muñoz" }
			]
		}
	]
}
```

## Atomic Name Part Defintions
The following is a list of the atomic name parts that combined will make up a person's full name.

Atomic Code | Description | Example
--- | --- | ---
NAM | Name String, such as it exists | "Davis, Lance, Steven John
LN | Last Name or Family Name String | "Schlovinski"
H-LN | Hyphenated Last Name String | "Bjon-Schlovinski"
FN | First Name or Given Name String | "James"
LN-PX | Last Name Prefix String | "Von as in Von Neuman"
MN | Middle Name String (Ind and Mod) | "Lewis"
SUF1 | Last Name Suffix String | "Jr., Esq."
SUF2 | Last Name Academic Suffixes String | "Ph.D., M.D., J.D."
SUF3 | Last Name Professional Organization Suffixes String | "PE, RHIA, RHIT"
NUM | Numeration String | "IV, XIV"
TITLE | Titles String | "Lord"
PREF | Prefix/Salutation String | "My Lord, Honorable, Dr, Ms."
P-PRF | Preferred Prefix String | "Lord, Dr"
ALIAS | Any aliases used by the person | "Mailman, Duke"
P-AL | Preferred Alias Name String | "Boss"
MADN | Maiden Name String | "Pitt"
P-MN | Previous Maiden Name String | "Bates"
CP-MN | Current-Previous Married Name
MLN | Maternal Last Name String | "Bjon"
PLN | Paternal Last Name String | "Schlovinski"
GEO | Geographic Attribute String | "Tarsus (as in Saul of Tarsus)"
AVO | Avocation Attribute String | "Tent-maker (S. Tent Maker)"
TRIB | Tribal data associate with name String | "Navajo"
D-NAM | Display/Print Name String | "John Davidson or Orm, Dan"