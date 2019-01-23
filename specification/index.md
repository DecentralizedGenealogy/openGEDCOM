# openGEDCOM
The openGEDCOM file specification is a set of standards that allow the community to interchange genealogical information without loss of meta data. This standard is not owned by any one entity. It is open and maintained by the community.

This specification is intentionally simple. There may be some ambiguity or assumptions that are left up to the developer. Let's work as a community to make this robust enough to be useful, but not overly burdened with details and bureaucracy that detract from progress. Brevity over verbosity.

## Table of Contents
* [Version](version.md)
* [Header](header.md)
* [Names](names.md)
* [Individuals](individuals.md)
* [sex](sex.md)
* [Families](families.md)
* [Sources](sources.md)
* [Events](events.md)
* [User extensions](extensions.md)
* [DNA](sources.md#dna)
* [Digital Media](source.md#photo)
* [Dates](dates.md)

## Examples
The following are examples of a full openGEDCOM. The Full example is more comprehensive, while the simplified one contains less meta data to provide a higher level view of the structure of the document. The intent is that these files become a type of ["acid"](https://en.wikipedia.org/wiki/Acid3) test for software products to use as a guide in their implementation.

* [Full Example](example_full.json)
* [Simplified Example](example_simple.json)
