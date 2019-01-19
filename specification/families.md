### Families
Family records compose relationships (parents, children) that makeup a family.

The `families` record is used to record marriages, unions, adoptions or whatever event that caused two people becoming the parents of a child. There is no limitation of the number of parents that can be in a family. However keep in mind that most software products assume only two. If a person participated in more than one family union, then they should appear in more than one `families` record. No assumptions should be made as to the sex/gender of the parents.

The preferred order of the children pointers within a `families` structure is chronological by birth.


```
"families":{
    "id":"FM001",
    "parents": [
        { "ref": "IN001" },
        { "ref": "IN002" }
    ]
    },
    "children": [
        {
            "ref": "IN003",
            "relType": {
                "type": "adopted",
                "id": "IN001"
            }
        },
        { "ref": "IN003" }
    ],
    "basedOn":{
        "link":[
            {
                "target":"EventRec",
                "ref":"EV001"
            },
            {
                "target":"EventRec",
                "ref":"EV002"
            }
        ],
        "note":"…"
    },
    "externalID":[
        {
            "type":"AFN",
            "id":"4S3469Q"
        },
        {
            "type":"submitter",
            "id":"F8945"
        }
    ],
    "note":"…",
    "evidence":{
        "citation":{

        }
    },
    "enrichment":{
        "citation":{
            "link":{
                "target":"SourceRec",
                "ref":"SR002"
            },
            "caption":"We Attend the Kunzle Family Reunion",
            "whereInSource":"5 min, 15 sec into the video, to 10 min, 30 sec.",
            "note":"Our family is featured about 5 minutes into the video."
        }
    },
    "changed":[
        {
            "date":"23 APR 1976",
            "time":"13:25:12",
            "note":"Record created"
        },
        {
            "date":"…",
            "time":"…",
            "contact":{
                "link":{
                    "target":"ContactRec",
                    "ref":"…"
                }
            },
            "note":"Adopted child added"
        }
    ]
}
 ```