# openGEDCOM
GEDCOM, a lineage-linked genealogical data format was developed by the Family and Church History Department of The Church of Jesus Christ of Latter-day Saints in 1984 to provide a flexible, uniform format for exchanging computerized genealogical data. GEDCOM is an acronym for GEnealogical Data COMmunication.

GEDCOM 5.5 has become the de facto industry standard. All genealogical software products that support importing or exporting data support the GEDCOM 5.5 standard.

The GEDCOM 5.5 specification has not changed since Oct 2 1999. The past 20 years have brought many new advances in technology that the GEDCOM standard is lacking. This project aims to bring the standard up to date, and make the standard open to the community so it will continue to be maintained.

The liberation of genealogical data will revolutionize the way family history is done, and will free the user community from the shackles of proprietary formats allowing this industry to flourish.

### [Full openGEDCOM specification](specification/index.md)

### What changes are in openGEDCOM?
- A [naming standard](specification/names.md) developed by [Richard Dick, Ph.D.](http://www.cavanaughconsulting.org/richard-dick-ph-d/) that allows all names across all languages, cultures, and time to be represented without ambiguity
- Support for [digital media](specification/sources.md#photo) (audio, images, video, etc)
- Use of the JSON industry standard file format
- Native support for hyper-linking (i.e. relationships, sources, documents, events, media, etc.)
- Improved [sourcing](specification/sources.md)
- Future [extensibility](specification/extensions.md)
- Support for [DNA](specification/sources.md#dna)

### Distributed Tree Model
openGEDCOM natively supports referencing objects (persons, sources, events, media, etc) in other trees or database. This makes all the data more accessible. You can see this in the example below. The child in family `FM001` is not actually located inside the openGEDCOM file, it is contained in another user's tree or database. This allows better collaboration with other users and less duplication. As we stop duplicating and copying the family tree data around the Internet, the data will begin to gather in the locations where the best steward of that data can manage it. This will result in higher quality data, and less user frustration.

### Example openGEDCOM file
Here is a simplified example of an openGEDCOM file and should not be used as a reference for generating an openGEDCOM file ([see full specification](specification/index.md)).
```
{
    "GEDCOM": {
        "version": "7.0 draft",
        "families": {
            "id": "FM001",
            "parents": [
                { "ref": "IN001" },
                { "ref": "IN002" }
            ]
            },
            "children": [
                { "ref": "http://williamsfamily.example.com/tree/IN003" }
            ]
        },
        "individuals": [
            { "id": "IN001" },
            {
                "id": "IN002",
                "name": [
                    { "NAM": "Sarah Jane Williams" }
                ],
                "sex": [
                    { "value": "female" }
                ],
                "living": "false"
            }
        ],
        "events": [
            {
                "id": "EV001",
                "type": "marriage",
                "participant": [
                    { "ref": "IN001", "role": "husband" },
                    { "Ref": "IN002", "role": "wife" }
                ],
                "date": [
                    {
                        "value": "1/6/1965 03:14:00",
                        "date": "1/6/1965",
                        "time": "03:14:00",
                        "zone": "America MST",
                        "calendar": "gregorian"
                    }
                ]
            }
        ]
    }
}
```

### Can I start using openGEDCOM now?
Yes and no. Please start to experiment with openGEDCOM. It needs to mature a little bit more and get community feedback and support. That's why it's still in a "draft" state. We hope to release version 7.0 soon.

### How can I get involved?
- Watch and Star this project
- Ask questions and make suggestions using the Issues feature
- Fork the repo, and begin to make suggestions and improvements through pull requests

### What about [GEDCOM X](http://www.gedcomx.org/)?
FamilySearch released an open source project called GEDCOM X in 2011. GEDCOM X was designed to be a ["clean break from legacy GEDCOM and clearly communicates a new revision that is different in scope and technology"](http://www.gedcomx.org/FAQ.html). It is maintained by FamilySearch, and welcomes pull requests from the community.

"*In August 2012 FamilySearch employee and GEDCOM X project leader Ryan Heaton dropped the claim that GEDCOM X is the new industry standard, and repositioned GEDCOM X as another FamilySearch open source project.* - [Wikipedia](https://en.wikipedia.org/wiki/GEDCOM#GEDCOM_X)

openGEDCOM is community focused, and seeks to be maintained and supported by the entire genealogical industry.

### Legacy GEDCOM
GEDCOM was a big milestone in the history of genealogy. It's legacy and history needs to be preserved. For those interested in past information and docments, this section is for you.
[Legacy examples and documents](legacy/index.md)


### Community Endorsements
Please consider putting down your name or organization to show support, and help build a community.
* ?