### Individuals
An array of people that exist in the genealogical data set. The individual record is a compilation of facts, known or discovered, about an individual. Sometimes these facts are from different sources. This form allows documentation of the source where each of the facts were discovered.

The individuals may be linked to from the `families` section. IDs for individuals should be unique to that individual within the file.

```
"individuals":[
    {
        "id":"IN001"
    },
    {
        "id":"IN002",
        "name": {
            "value": "Neta Eskelson Allen",
            "parts": [
                {
                    "FN": [
                        { "value": "Neta" }
                    ],
                    "MN": [
                        { "value": "Eskelson" }
                    ],
                    "LN": [
                        { "value": "Allen" }
                    ],
                    "SUF": [
                        { "value": "Duchess", "type": "title" }
                    ]
                }
            ]
        },
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
