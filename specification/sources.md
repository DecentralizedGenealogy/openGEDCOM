### Sources
Sources contain an array of source information that provides evidence of the genealogical conclusions you make about the people in your openGEDCOM file. Source records are used to provide a bibliographic description of the source cited.

#### Photo
Photos and other digital media can contain relative filesystem links or web URIs.

```
"sources":[
    {
        "id": "SR001",
        "type": "photo",
        "title": "Robert Kunzle Graduation Photo",
        "author": "…",
        "date": "",
        "URI": "http://flikr.com/photo1.jpg",
        "note": "…"
    }
]
 ```

#### DNA
```
"sources":[
    {
        "id": "SR005",
        "type": "dna",
        "dnaType": "autosomal",
        "haplo": "B5a1a",
        "testingCompany": "23andme",
        "date": "",
        "URI": "http://23andme.com/dna.csv",
        "note": "…"
    }
]
 ```

#### Vital Record
```
"sources":[
    {
        "id": "SR002",
        "type": "vital records",
        "repository": {
            "link": {
                "target": "RepositoryRec",
                "ref": "RP001"
            },
            "callNbr": "4568-09"
        },
        "title": "Marriage Registry",
        "article": "…",
        "author": "California State Board of Health",
        "URI": "…",
        "publishing": "…",
        "note": "…",
        "changed": "…"
    }
]
 ```

#### Book
```
"sources":[
   {
        "id": "SR003",
        "type": "book",
        "title": "Prominent Families of Early Boston",
        "URI": "https://books.google.com/book.pdf"
        "publishing": "Lynn, Mass.: The Stuart Little Co., 1936"
    }
]
 ```

#### Video Tape
```
"sources":[
    {
        "id": "SR004",
        "type": "video tape",
        "lang": "de",
        "title": "Kunzle Family Reunion",
        "author": "…",
        "URI": "http://www.kunzlefam.org/famreun.mov",
        "publishing": "…",
        "note": "…",
        "changed": "…"
    }
]
 ```

