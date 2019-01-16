# openGEDCOM
GEDCOM was developed by the Family and Church History Department of The Church of Jesus Christ of Latter-day Saints in 1984 to provide a flexible, uniform format for exchanging computerized genealogical data. GEDCOM is an acronym for GEnealogical Data COMmunication.

GEDCOM 5.5 has become the de facto industry standard. All genelaogical software products that support importing or exporting data support the GEDCOM 5.5 standard.

The GEDCOM 5.5 specificaiton has not changed since Oct 2 1999. The past 20 years have brought many new advances in technology that the GEDCOM standard is lacking. This project aims to bring the standard up to date, and make the standard open to the community so it will continue to be maintained.

## [specification/index.md](Table of contents for the full openGEDCOM specification)

## What changes are in openGEDCOM?
- A naming standard developed by [http://www.cavanaughconsulting.org/richard-dick-ph-d/](Richard Dick, Ph.D.)called C2D2 that allows all names across all languages and cultures to be represented without ambiguity.
- Support for digital media (audio, images, video, etc)
- Use of the JSON industry standard instead of a propriatey file format.
- Native support for hyper-linking (ie sources, documents, media, etc.)
- Improved sourcing meta data
- Allows future extensibility

## Can I start using openGEDCOM now?
Yes and no. Please start to experiment with openGEDCOM. It needs to mature a little bit more and get community feeback and support. That's why it's still in a "draft" state. We hope to release version 7.0 soon.

## How can I get involved?
- Watch and Star this project
- Ask questions and maks sugestions using the Issues feature
- Fork the repo, and begin to make suggestions and improvements through pull requests

## Example openGEDCOM files
Here is a simplified example of an openGEDCOM file and should not be used as a reference for generating an openGEDCOM file (see full specification).
```
{
    "GEDCOM": {
        "version": "7.0 draft",
        "family": {
            "id": "FM001",
            "parents": [
                { "ref": "IN001" },
                { "ref": "IN002" }
            ]
            },
            "children": [
                { "ref": "IN003" }
            ]
        },
        "individuals": [
            { "id": "IN001" },
            {
                "id": "IN002",
                "name": {
                    "value": "Sarah Jane Williams",
                },
                "sex": "female",
                "living": "false"
            },
            { "id": "IN003" }
        ],
        "events": [
            {
                "id": "EV001",
                "type": "marriage",
                "participant": [
                    { "ref": "IN001", "role": "husband" },
                    { "Ref": "IN002", "role": "wife" }
                ],
                "date": { "text": "7 NOV 1834" },
            }
        ]
    }
}
```
Legacy GEDCOM examples can be found at: [LegacyExamples/gedcom53.ged](5.3), 5.4, 5.5, 5.5.1, 5.6, 6.0

## What about GEDCOM X?
FamilySearch released an open source project called GEDCOM X in 2011. GEDCOM X was designed to be a [http://www.gedcomx.org/FAQ.html]("clean break from legacy GEDCOM and clearly communicates a new revision that is different in scope and technology"). It is maintained by FamilySearch, and welcomes pull requests from the community.

In August 2012 FamilySearch employee and GEDCOM X project leader Ryan Heaton dropped the claim that GEDCOM X is the new industry standard, and repositioned GEDCOM X as another FamilySearch open source project. - [https://www.tamurajones.net/GEDCOMXNoIndustryStandard.xhtml](Tamura Jones)

openGEDCOM is community focused, and seeks to be maintained and supported by the entire geneoligcial industry.
