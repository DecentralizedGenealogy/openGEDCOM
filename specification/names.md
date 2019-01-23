# Names
Representing a person's name in a data structure seems like a simple task. When you introduce the need to represent the name taking into consideration the context of language, culture, and time it becomes more difficult.

In addition it's imperative that each name be represented with uniqueness, having no ambiguity with similar yet different names. It is done by breaking down each name to its atomic level, and building a fully qualified name by putting its atomic parts together in an elegant and simple fashion. This naming strategy was derrived from the **Composite Clinical Data Dictionary** (C<sup>2</sup>D<sup>2</sup>) developed by [Richard Dick, Ph.D.](http://www.cavanaughconsulting.org/richard-dick-ph-d/).

This specification currently allows all current names to be uniquely defined, and allows the specification to infinitely grow as new situations are encountered.

<sup>[TODO: Provide links to more C2D2 documentation]</sup>

[Atomic Name Part Definitions](#Atomic-Name-Part-Definitions)

### Simple Name Example
An overly simplified (not recommended) way of representing a person's name

`"name": [ { "NAM": "Sarah Jane Williams" } ]`

### Complex Name Example 1
A more complicated example of an hispanic name with the complexities of the multiple surnames along with an academic title.

```
"name": [
	{
		"NAM": "Rosa María Muñoz Gómez",
		"parts": [
			{
				"FN": [
					{ "value": "Rosa" },
					{ "value": "Maria" }
				],
				"LN": [
					{
						"value": "Muñoz"
					}
				],
				"SUF": [
					{ "value": "Ph.D.", "type": "Academic" }
				],
				"CP-MN": [
					{
						"value": "Gómez",
						"modifier": {
							"desc": "marriage",
							"ref": "marriage_event_id"
						}
					 }
				],
				"MLN": [
					{ "value": "Izquierdo" }
				],
				"PLN": [
					{ "value": "Muñoz" }
				]
			}
		]
	},
	{ "NAM": "Rosa" }
]
```

### Complex Name Example 2
In this example we uniquly represent [Muhammad Ali](https://en.wikipedia.org/wiki/Muhammad_Ali). Since Ali had two names, we'll represent his identity with two name elements. Ordering is important, and is chronological. The first name entry in the array is considered the default or current name, with the last name being the first name the person held. The `modifier` element references an `event` in the openGEDCOM file that describes the event that took place that caused the name to change.
```
"name": [
	{
		"NAM": "Muhammad Ali",
		parts: [
			{ "FN": "Muhammad" },
			{ "LN": "Ali" }
		],
		"modifier": {
			"ref": "name_change_event_id",
			"desc": "Name change in 1964"
		}
	},
	{
		"NAM": "Cassius Marcellus Clay, Jr.",
		"parts": [
			{
				"FN": [
					{ "value": "Cassius" }
				],
				"MN": [
					{ "value": "Marcellus" }
				"LN": [
					{ "value": "Clay" }
				],
				"SUF": [
					{ "value": "Jr." }
				],
				"MLN": [
					{ "value": "Johnson" }
				],
				"PLN": [
					{ "value": "Clay" }
				],
				"ALIAS" : [
					{
						"value": "The Greatest",
						"type": "nickname"
					}
				]
			}
		]
		"modifier": {
			"ref": "birth_event_id",
			"desc": "birth"
		}
	}
]
```


## Atomic Name Part Definitions
The following is a list of the atomic name parts that combined will make up a person's full name.

Atomic Code | Description | Example
--- | --- | ---
NAM | Name String, such as it exists | "Davis, Lance, Steven John
LN | Last Name or Family Name String | "Schlovinski"
H-LN | Hyphenated Last Name String | "Bjon-Schlovinski"
FN | First Name or Given Name String | "James"
LN-PX | Last Name Prefix String | "Von as in Von Neuman"
MN | Middle Name String (Ind and Mod) | "Lewis"
SUF | Last Name Suffix String | "Jr., Esq.", "Ph.D., M.D., J.D.", "PE, RHIA, RHIT"
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
MI | Middle Initials | For middle initials where the initials did not represent another name
NMI | My Initials that I use for my Name | "A.", "W.E.B."
AV | Audible sound(s), or visual elements that make up a name | A "ref" (reference) to a digital media file. For example a WAV file of the person saying their name, or an image showing their signature.
TRIB | Tribal data associate with name String | "Navajo"
\_[new_atomic_code_name] | An new proposed atomic code is prefixed with an underscore "\_" until it has officially been adopted | For example the atomic code "_AVATAR" could be created to represent a person's online profile identity name