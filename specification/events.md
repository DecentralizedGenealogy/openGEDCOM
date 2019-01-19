
### Events
An array of events surrounding the people in your database such as birth, death, marriage etc.

```
"events":[
    {
        "id":"EV001",
        "type":"marriage",
        "vitalType":"marriage",
        "participant":[
            {
                "link":{
                    "target":"IndividualRec",
                    "ref":"IN001"
                },
                "role":"husband",
                "age":"26"
            },
            {
                "link":{
                    "target":"IndividualRec",
                    "ref":"IN002"
                },
                "role":"wife",
                "age":"21"
            }
        ],
        "date":{
            "calendar":"Julian",
            "text":"ABT 7 NOV 1834"
        },
        "place":{
            "placeName":{
                "placePart":[
                    {
                        "type":"town",
                        "level":"4",
                        "text":"Cove"
                    },
                    {
                        "type":"county",
                        "level":"3",
                        "text":"Cache"
                    },
                    {
                        "type":"state",
                        "level":"2",
                        "text":"Utah"
                    },
                    {
                        "type":"country",
                        "level":"1",
                        "text":"USA"
                    }
                ]
            },
            "coordinates": {
            	"latitude": "18.153 N",
            	"longitude": "178.150 E"
            },
            "placeNameVar":[
                {
                    "method":"kana"
                },
                {
                    "method":"romanji"
                }
            ]
        },
        "religion":"Reformed Christian",
        "externalID":{
            "type":"…",
            "id":"…"
        },
        "submitter":"…",
        "note":"…",
        "evidence":{
            "citation":{
                "link":{
                    "target":"SourceRec",
                    "ref":"SR001"
                },
                "whereInSource":"File No. 7895-09, p. 23",
                "whenRecorded":"10 June 1903",
                "extract":"Text extracted from the source.",
                "note":"Certified copy in possession of Larry T. Smith, Sandy, Utah."
            }
        },
        "enrichment":"….",
        "changed":"…"
    },
    {
        "id":"EV002",
        "type":"christening",
        "vitalType":"birth",
        "participant":[
            {
                "link":{
                    "target":"IndividualRec",
                    "ref":"IN001"
                },
                "role":"parent"
            },
            {
                "link":{
                    "target":"IndividualRec",
                    "ref":"IN002"
                },
                "role":"parent"
            },
            {
                "link":{
                    "target":"IndividualRec",
                    "ref":"IN003"
                },
                "role":"child"
            }
        ]
    }
]
```