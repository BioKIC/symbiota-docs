---
title: "Catalog Numbers"
date: 2022-02-28
lastmod: 2022-02-28
draft: false
authors: ["Katie Pearson, Ed Gilbert"]
keywords: ["edit","fields","data fields", "terms", "dwc terms","catalog number","tag names"]
---

### Catalog Numbers

Catalog numbers are important to assign to each record because they act as unique identifiers for each record. This field should be used to store the barcode or the accession number (herbaria only). This field should be unique for each collection, for example, by including the collection acronym (e.g., ASU00012345, WIS-L-001456). Use of leading zeros is recommended to enable correct sorting in the Symbiota interface.

### Other Catalog Numbers

The Other Catalog Number field can be used to store any other identifying number associated with a record (other than the collector number, which should be stored in the Number field, aligned with the [dwc:recordNumber](https://dwc.tdwg.org/terms/#dwc:recordNumber) field. This field is a text field that can accomodate multiple values of other catalog number. We recommend separating values by semicolons (;) or pipes (|).

In some portals, a user can define the type of Other Catalog Number that is being provided by including a value in the Tag Name field. These Tag Names may be collection-specific based on the type of identifier that is indicated. Common tags might be: previous catalog number, old catalog #, accession number, NPS #, NPS accession #, secondary occurrenceID, etc. Then, the value for this type of Other Catalog Number should be provided in the "Additional Identifier Value" field.

The Tag Name field is optional, and thus can be left blank with just an "Other Catalog Number" entered in the Additional Identifier Value field. The Additional Identifier Value field operates in the same way that the Other Catalog Number field previously did and can be used in the same way.

![Other Catalog Numbers](/symbiota-docs/images/othercatalognumbertag.PNG)

### Duplicate Catalog and Other Catalog Numbers

Collection administrators can identify and resolve duplicate catalog numbers or other catalog numbers using the [Data Cleaning Tools](https://biokic.github.io/symbiota-docs/coll_manager/data_cleaning/dupes/).
