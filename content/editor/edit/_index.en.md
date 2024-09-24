---
title: "Editing Records"
date: 2021-10-26
lastmod: 2024-09-24
draft: false
authors: ["Katie Pearson"]
weight: 60
keywords: ["edit","change","record search form","search"]
---

{{< notice info >}}
  This page provides instructions on how to search for and edit records.
{{</ notice >}}

* To batch edit records (only available to collection administrators), visit [this page](https://biokic.github.io/symbiota-docs/coll_manager/edit/batch/).
* For an overview of fields in the occurrence editor form, visit [this page](https://biokic.github.io/symbiota-docs/editor/edit/fields).
* For an explanation of the record editor tabs, visit [this page](https://biokic.github.io/symbiota-docs/editor/edit/tabs/).

To edit individual records, select "Edit Existing Occurrence Records" from the Data Editor Control Panel (accessed via My Profile > Occurrence Management > name of collection). From this page, you can search for specific records by entering search terms into the Record Search Form. You can search by multiple search terms using this form.

![Record Search Form](/symbiota-docs/images/recordsearchform.PNG)

To search according to fields not explicitly stated in the Record Search Form, select the field from the dropdown menu after Custom Field 1. You can include up to 8 Custom fields in your search. The second dropdown lists after the Custom Fields will allow you to conduct more specific searches, such as for ranges or fields that are null. The options include:
* EQUALS: the field contains **only** the provided text
* NOT EQUALS: the field does not match the provided text exactly (does not only contain the provided text)
* STARTS WITH: the field starts with the provided text
* CONTAINS: the field contains the provided text anywhere in the field
* DOESN'T CONTAIN: the field does not contain the provided text anywhere in the field
* GREATER THAN
* LESS THAN
* IS NULL: the entire field contains no value
* IS NOT NULL: the field contains any value

To conduct a search, click the Display Editor (to view one record at a time) or Display Table (to view the first 1000 records at a time) buttons.

{{< notice note >}}
  When searching for the characters "_" or "%" in your record fields, you must precede this character with the backwards slash "escape" character (\). E.g., when searching for the value "_1", you should enter "\_1".
{{</ notice >}}

To search by specimens entered by you (the current user), click the CU button.

To sort your search results, select a field from the dropdown menu after Sort By (bottom right of Record Search Form), then select whether you wish to sort in ascending or descending order.

To view a specific record from the Table Display, click the Symbiota ID number or the Open in New Window icon in the leftmost SymbiotaID column.

To re-open the record search form after you have conducted a search, click the Toggle Record Search Form button.

![New Return to Record Search Form](/symbiota-docs/images/returntorecordsearchform_new.PNG)

In older versions of Symbiota, you can toggle the search form by clicking the magnifying glass icon to the right of the name of the collection at the top of the window.

![Old Return to Record Search Form](/symbiota-docs/images/returntorecordsearchform.PNG)
