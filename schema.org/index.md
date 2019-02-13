# Schema.org as a foundation
Schema.org is an established organziation with well defined schema objects (types). It is a collaborative, community activity with a mission to create, maintain, and promote schemas for [structured data](https://schema.org/docs/datamodel.html) on the Internet, on web pages, in email messages, and beyond.

Another approach to developing a GEDCOM standard could be to take the existing schema.org definitions and packaging them up in a form specific to the genealogical industry. An advantage to this would be that the it could also be used to view the genealogical data in HTML in [Microdata](https://en.wikipedia.org/wiki/Microdata_(HTML)) format. This would make the data uniformly searchable by Google etc.

For example a GEDCOM document could be crafted using standard types from schema.org.

- [Person](https://schema.org/Person)
- [Place](https://schema.org/Place)
- [Event](https://schema.org/Event)
- Family [Organization](https://schema.org/Organization), [Affiliation](https://schema.org/affiliation)
- [Digital Document](https://schema.org/DigitalDocument)
- [Sources](https://schema.org/CreativeWork)

### Extensions
To fill in the gaps that are not coered by schema.org, [Extensions](https://pending.schema.org/docs/extension.html) can easily be created via hosted or external extensions.
- More robust Naming standard
- Dates to support different calendars and cultures.


### Example openGEDCOM file using schema.org
The folling is an example of how an openGEDCOM file could be created using schema.org.
```
// Family
{
	"@context": "http://schema.org",
	"@type": "Person",
	"@id": "ID001",
	"name": "Bob Jones",
	birthDate: "1845-02-12",
	deathDate: "1913-06-08",
	"image": "http://example.com/bob.jpg",
	"url": "http://bob.example.com",
	"spouse": {
			"@type": "Person",
			"@id": "ID002",
			"name": "Suzy Robinson"
	}
	"children": [
		{
			"@type": "Person",
			"@id": "ID003",
			"name": "Joey Jones"
		},
		{
			"@type": "Person",
			"@id": "ID004",
			"name": "Sally Jones"
		}
	]
}

// Marriage
{
	"@context": "http://schema.org",
	"@type": "MarryAction",
	"@id": "M001",
	"startTime": "1960-02-12T22:42:41Z",
	"endTime": "2010-02-12T22:42:41Z",
	"image": "http://example.com/marriage_certification.jpg",
	"agent": {
		"@type": "Person",
		"@id": "ID001",
		"name": "Joey"
	},
	"object": {
		"@type": "Person",
		"@id": "ID002",
		"name": "Suzy"
	},
	"location": {
		"@type": "Place",
		"address": {
			"@type": "PostalAddress",
			"addressLocality": "Denver",
			"addressRegion": "CO",
			"postalCode": "80209",
			"streetAddress": "7 S. Broadway"
		}
	}
}

// Source (Book)
{
	"@context": "http://schema.org",
	"@type": "Book",
	"@id": "S001",
	"mentions": {
		"@type": "Person",
		"value": "ID001",
 	},
	"bookFormat": "EBook/DAISY3",
	"copyrightHolder": {
		"@type": "Organization",
		"name": "Holt, Rinehart and Winston"
	},
	"copyrightYear": "2007",
	"description": "This book contains the paternal lineage of the Jones family starting on page 34",
	"genre": "Family History",
	"inLanguage": "en-US",
	"isFamilyFriendly": "true",
	"isbn": "9780030426599",
	"name": "Holt Physical Science",
	"numberOfPages": "598",
	"publisher": {
		"@type": "Organization",
		"name": "Holt, Rinehart and Winston"
	}
}

// Source (Website)
{
  "@context": "http://schema.org",
  "@type": "WebPage",
  "@id": "S002",
	"mentions": [
		{ "@type": "Person", "value": "ID001" },
		{ "@type": "Person", "value": "ID002" }
 	],
  "breadcrumb": "Search > Records > Collection: United States Census, 1940",
  "url": "https://familysearch.org/ark:/61903/1:1:VYGH-JCK"
  "mainEntity":{
          "@type": "Book",
          "author": "United States Census Bureau",
          "bookFormat": "http://schema.org/Paperback",
          "datePublished": "14 March 2018",
          "image": "https://www.familysearch.org/ark:/61903/3:1:3QS7-L9MR-FNR7?cc=2000219",
          "inLanguage": "English",
          "publisher": "United States Government",
        }
}
```