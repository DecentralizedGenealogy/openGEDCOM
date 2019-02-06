# openGEDCOM Methodology

Outlined below are some of the principles behind how we got to this point, and various options we could pursue going forward as more people get involved.

### W3C
W3C Is a great example of how a governing body works together with the community to establish open standards around technology to foster innovation in an efficient manner. Many of the models they've established could be mimicked to expedite organizing the openGEDCOM specification.

### JSON-LD
[JSON-LD](https://json-ld.org/) was chosen as the syntax for the current version due to its pervasive adoption in the web ecosystem.

"Linked Data empowers people that publish and use information on the Web. It is a way to create a network of standards-based, machine-readable data across Web sites. It allows an application to start at one piece of Linked Data, and follow embedded links to other pieces of Linked Data that are hosted on different sites across the Web."

"JSON-LD is a lightweight Linked Data format. It is easy for humans to read and write. It is based on the already successful JSON format and provides a way to help JSON data interoperate at Web-scale. JSON-LD is an ideal data format for programming environments, REST Web services, and unstructured databases such as CouchDB and MongoDB." -[JSON-LD](https://json-ld.org/)

### Schema.org
Schema.org could be harnessed and would allow openGEDCOM to be compatible with an already established and prolific set of vocabularies and syntax to aid in compatibility as well as ease of adoption for developers.

Any areas where schema.org is lacking, we could [extend](https://schema.org/docs/extension.html) the vocabulary or attributes to reach our needs. One example would be [Person](https://schema.org/Person). Schema.org's Person Name is not robust enough to eliminate all ambiguity in representing a person's name. Thus we'd need to augment it with C2D2.

"Schema.org is a collaborative, [community](https://www.w3.org/community/schemaorg/) activity with a mission to create, maintain, and promote schemas for structured data on the Internet, on web pages, in email messages, and beyond."

"A shared vocabulary makes it easier for webmasters and developers to decide on a schema and get the maximum benefit for their efforts. It is in this spirit that the founders, together with the larger community have come together - to provide a shared collection of schemas."

### Governance
Creating an official W3C group could be the model we choose to organize and direct the efforts of this community.

[W3C Groups](https://www.w3.org/community/about/faq/#how-do-we-get-started-in-a-new-group)

[Running a Group](https://www.w3.org/community/about/good-practice-for-running-a-group/)

### Open Standards Examples
- HTML [body tag](https://www.w3.org/community/about/good-practice-for-running-a-group/)
- SVG [Circle Element](https://www.w3.org/TR/SVG11/shapes.html#CircleElement)