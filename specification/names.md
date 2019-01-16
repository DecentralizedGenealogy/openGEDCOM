# Names
Representing a person's name in a data structure seems like a simple task. When you introduce the need to represent the name taking into consideration language, cutlure, and context it becomes more difficult.

In addition it's emparative that each name be represented with uniqness, having no ambiguitty with similar yet different names. This is what the Composite Clinical Data Dictionary (C2D2) naming standard allows us to do. It is done by breaking down each name to its atomic level, and building a fully qualified name by putting it's atomic parts together in an elegant and simple fashion.

This specification currently allows all current names to be uniqely defined, and allows the specification to infinatly grow as new situations are encountered.

The C2D2 specificaiton was created by [http://www.cavanaughconsulting.org/richard-dick-ph-d/](Richard Dick, Ph.D.)

Complex Name Example
Atomic Name Part Defintions

## Complex Name Example
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

## Atomic Name Part Defintions
NAM - Name String, such as it exists. Example:"Davis, Lance, Steven John
LN - Last Name or Family Name String. Example:"Schlovinski"
H-LN - Hyphenated Last Name String. Example:"Bjon-Schlovinski"
FN - First Name or Given Name String. Example:"James"
LN-PX - Last Name Prefix String. Example:"Von as in Von Neuman"
MN - Middle Name String (Ind and Mod). Example:"Lewis"
SUF1 - Last Name Suffix String. Example:"Jr., Esq."
SUF2 - Last Name Academic Suffixes String. Example:"Ph.D., M.D., J.D."
SUF3 - Last Name Professional Organization Suffixes String. Example:"PE, RHIA, RHIT"
NUM - Numeration String. Example:"IV, XIV"
TITLE - Titles String. Example:"Lord"
PREF - Prefix/Salutation String. Example:"My Lord, Honorable, Dr, Ms."
P-PRF - Preferred Prefix String. Example:"Lord, Dr"
ALIAS - Any aliases used by the person. Example:"Mailman, Duke"
P-AL - Preferred Alias Name String. Example:"Boss"
MADN - Maiden Name String. Example:"Pitt"
P-MN - Previous Maiden Name String. Example:"Bates"
CP-MN - Current-Previous Married Name
MLN - Maternal Last Name String. Example:"Bjon"
PLN - Paternal Last Name String. Example:"Schlovinski"
GEO - Geographic Attribute String. Example:"Tarsus (as in Saul of Tarsus)"
AVO - Avocation Attribute String. Example:"Tent-maker (S. Tent Maker)"
TRIB - Tribal data associate with name String. Example:"Navajo"
D-NAM - Display/Print Name String. Example:"John Davidson or Orm, Dan"