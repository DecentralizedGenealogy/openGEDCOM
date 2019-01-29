### Header
Contains information about the software product that generated the file along with information about the user who maintains the genealogical data. A `header` element is not required but is highly recommended, and should occure first in the file to ease human readability.

```
"header": {
    "fileCreation": {
        "Date": "2 OCT 2000",
        "Time": "15:20:2.3"
    },
    "Product": {
            "ProductId": "DAS",
            "Version": "6.3",
            "Name": "Deluxe Ancestral System",
            "Company": "XYX Inc.",
            "url": "xyx.example.com"
    },
    "submitter": {
    	"name": "John Doe",
    	"address": {
    		"street": [ "123 N. Canyon Rd.", "Apartment 13" ],
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
