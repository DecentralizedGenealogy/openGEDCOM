# openGEDCOM
The openGEDCOM file specification is a set of standards that allow the community to interchange genealogical information without loss of meta data. This standard is owned and maintained by the community.

## Table of Contents
* [Version](#version)
* [Header](#header)
* [Names](names.md)
* [Individuals](#indivicuals)
* [Families](#families)
* [Sources](#sources)
* [Events](#events)

## Examples
The following are examples of a full openGEDCOM. The Full example is more comprehensive, while the simplified one contains less meta data to provide a higher level view of the structure of the document.
* [Full Example](specification/example_full.json)
* [Simpified Example](specification/example_simple.json)

### Version
The version number of the openGEDCOM spec used to generate the file.

### Header
Contains information about the software product that generated the file along with information about the user who owns the genealogical data.
```
"header": {
    "fileCreation": {
        "Date":"2 OCT 2000",
        "Time":"15:20:2.3"
    },
    "Product": {
            "ProductId":"DAS",
            "Version":"6.3",
            "Name":"Deluxe Ancestral System",
            "Company":"XYX Inc.",
            "url": "xyx.example.com"
    },
    "submitter": {
    	"name": "John Doe",
    	"address": {
    		"street": ["123 N. Canyon Rd.", "Apartment 13"],
    		"town": "Salt Lake City",
    		"county": "Salt Lake",
    		"state": "Utah",
    		"country": "USA",
    		"zip": "84001"
    	},
    	"url": "https://johndoe.example.com"
    	"phone": "+1 801-555-1212"
    	"email": "johndoe@example.com"
    },
    "notes":"…"
}
```

### Individuals
An array of people that exist in the genealogical data set.
```
"individuals":[
    {
        "Id":"IN001"
    },
    {
        "Id":"IN002",
        "IndivName":[
            {
                "Name":"Neta Eskelson Allen",
                "NamePart":[
                    {
                        "Type":"title",
                        "text":"Duchess"
                    },
                    {
                        "Type":"given name",
                        "Level":"3",
                        "text":"Neta"
                    },
                    {
                        "Type":"maiden name",
                        "Level":"2",
                        "text":"Eskelson"
                    },
                    {
                        "Type":"surname",
                        "Level":"1",
                        "text":"Allen"
                    }
                ],
                "IndNameVariation":{
                    "Method":"romanji",
                }
            },
            {
                "Type":"alias",
                "text":"…"
            },
            {
                "Type":"nickname",
                "text":"…"
            }
        ],
        "Sex":"Female",
        "living":"false",
        "PersInfo":[
            {
                "Type":"occupation",
                "Information":"seamstress",
                "Date":"FROM 1835 TO 1875"
            },
            {
                "Type":"residence",
                "Date":"FROM 10 JUL 1845 TO 25 MAY 1880",
                "Place":"…"
            },
            {
                "Type":"attribute",
                "Information":"5 ft. 4 in. tall, blond hair, blue eyes, well mannered"
            }
        ],
        "AssocIndiv":{
            "Link":{
                "Target":"IndividualRec",
                "Ref":"…"
            },
            "Association":"first ancestor",
            "Note":"…",
            "Citation":"…"
        },
        "DupIndiv":{
            "Link":{
                "Target":"IndividualRec",
                "Ref":"…"
            },
            "Note":"…",
            "Citation":"…"
        },
        "ExternalID":{
            "Type":"…",
            "Id":"…"
        },
        "Submitter":"…",
        "Note":"…",
        "Evidence":"…",
        "Enrichment":"…",
        "Changed":"…"
    },
    {
        "Id":"IN003"
    }
],
```

### Families
Family records compose relationships of the parents and children that makeup a family.
```
"families":{
    "Id":"FM001",
    "Parent":{
        "Link":{
            "Target":"IndividualRec",
            "Ref":"IN001"
        }
    },
    "Parent":{
        "Link":{
            "Target":"IndividualRec",
            "Ref":"IN002"
        },
        "FamilyNbr":"2"
    },
    "Child":[
        {
            "Link":{
                "Target":"IndividualRec",
                "Ref":"IN003"
            },
            "ChildNbr":"1"
        },
        {
            "Link":{
                "Target":"IndividualRec",
                "Ref":"…"
            },
            "ChildNbr":"2",
            "RelToFath":"adopted"
        }
    ],
    "BasedOn":{
        "Link":[
            {
                "Target":"EventRec",
                "Ref":"EV001"
            },
            {
                "Target":"EventRec",
                "Ref":"EV002"
            }
        ],
        "Note":"…"
    },
    "ExternalID":[
        {
            "Type":"AFN",
            "Id":"4S3469Q"
        },
        {
            "Type":"submitter",
            "Id":"F8945"
        }
    ],
    "Submitter":"…",
    "Note":"…",
    "Evidence":{
        "Citation":{

        }
    },
    "Enrichment":{
        "Citation":{
            "Link":{
                "Target":"SourceRec",
                "Ref":"SR002"
            },
            "Caption":"We Attend the Kunzle Family Reunion",
            "WhereInSource":"5 min, 15 sec into the video, to 10 min, 30 sec.",
            "Note":"Our family is featured about 5 minutes into the video."
        }
    },
    "Changed":[
        {
            "Date":"23 APR 1976",
            "Time":"13:25:12",
            "Note":"Record created"
        },
        {
            "Date":"…",
            "Time":"…",
            "Contact":{
                "Link":{
                    "Target":"ContactRec",
                    "Ref":"…"
                }
            },
            "Note":"Adopted child added"
        }
    ]
}
 ```
### Sources
Sources contain an array of source information that provides evidence of the genealogical conclusions you make about the people in your openGEDCOM file.
```
"sources":[
    {
        "Id":"SR001",
        "Type":"vital records",
        "Repository":{
            "Link":{
                "Target":"RepositoryRec",
                "Ref":"RP001"
            },
            "CallNbr":"4568-09"
        },
        "Title":"Marriage Registry",
        "Article":"…",
        "Author":"California State Board of Health",
        "URI":"…",
        "Publishing":"…",
        "Note":"…",
        "Changed":"…"
    },
    {
        "Id":"SR002",
        "Type":"video tape",
        "xml:lang":"de",
        "Title":"Kunzle Family Reunion",
        "Author":"…",
        "URI":"http://www.kunzlefam.org/famreun.mov",
        "Publishing":"…",
        "Note":"…",
        "Changed":"…"
    },
    {
        "Id":"SR003",
        "Type":"book",
        "Title":"Prominent Families of Early Boston",
        "Publishing":"Lynn, Mass.: The Stuart Little Co., 1936"
    },
	"repository": {
	    "Id":"RP001",
	    "Type":"government",
	    "Name":"California Department of Vital Records",
	    "MailAddress":{
			"AddrLine":"P. O. Box 2406"
	    },
	    "Phone":"…",
	    "Email":"…",
	    "URI":"…",
	    "Note":"…",
	    "Changed":"…"
	}
]
 ```

### Events
An array of events surrounding the people in your database such as birth, death, marriage etc.
```
"events":[
    {
        "Id":"EV001",
        "Type":"marriage",
        "VitalType":"marriage",
        "Participant":[
            {
                "Link":{
                    "Target":"IndividualRec",
                    "Ref":"IN001"
                },
                "Role":"husband",
                "Age":"26"
            },
            {
                "Link":{
                    "Target":"IndividualRec",
                    "Ref":"IN002"
                },
                "Role":"wife",
                "Age":"21"
            }
        ],
        "Date":{
            "Calendar":"Julian",
            "text":"ABT 7 NOV 1834"
        },
        "Place":{
            "PlaceName":{
                "PlacePart":[
                    {
                        "Type":"town",
                        "Level":"4",
                        "text":"Cove"
                    },
                    {
                        "Type":"county",
                        "Level":"3",
                        "text":"Cache"
                    },
                    {
                        "Type":"state",
                        "Level":"2",
                        "text":"Utah"
                    },
                    {
                        "Type":"country",
                        "Level":"1",
                        "text":"USA"
                    }
                ]
            },
            "Coordinates": {
            	"Latitude": "18.153 N",
            	"Longitude": "178.150 E"
            },
            "PlaceNameVar":[
                {
                    "Method":"kana"
                },
                {
                    "Method":"romanji"
                }
            ]
        },
        "Religion":"Reformed Christian",
        "ExternalID":{
            "Type":"…",
            "Id":"…"
        },
        "Submitter":"…",
        "Note":"…",
        "Evidence":{
            "Citation":{
                "Link":{
                    "Target":"SourceRec",
                    "Ref":"SR001"
                },
                "WhereInSource":"File No. 7895-09, p. 23",
                "WhenRecorded":"10 June 1903",
                "Extract":"Text extracted from the source.",
                "Note":"Certified copy in possession of Larry T. Smith, Sandy, Utah."
            }
        },
        "Enrichment":"….",
        "Changed":"…"
    },
    {
        "Id":"EV002",
        "Type":"christening",
        "VitalType":"birth",
        "Participant":[
            {
                "Link":{
                    "Target":"IndividualRec",
                    "Ref":"IN001"
                },
                "Role":"parent"
            },
            {
                "Link":{
                    "Target":"IndividualRec",
                    "Ref":"IN002"
                },
                "Role":"parent"
            },
            {
                "Link":{
                    "Target":"IndividualRec",
                    "Ref":"IN003"
                },
                "Role":"child"
            }
        ]
    }
]
```