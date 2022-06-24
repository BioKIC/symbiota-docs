---
title: "Redacting / Obscuring Data"
Date: 2021-11-01
lastmod: 2022-06-24
authors: ["Katie Pearson","Ed Gilbert"]
weight: 80
keywords: ["rare species", "data protection", "redaction"]
---

{{< notice info >}}
  This page explains how data redaction functions in a Symbiota portal.
{{</ notice >}}

Collection managers may wish to redact locality data for certain occurrences, for example, of rare or endangered species or for locations on private property. Locality data in Symbiota portals may be redacted in one of three ways: (a) individually (per occurrence), (b) globally (per taxon), or (c) by state.

Redacting locality data in Symbiota portals is currently binary: an occurrence can have its locality redacted (Locality Security = 1, checked) or not (Locality Security = 0, unchecked). When the Locality Security box is checked (or Locality Security is uploaded as 1) for a given occurrence, a user who does not have rare species reader or editor permissions will not be able to view that occurrence's:
  * Locality below the level of county
  * Coordinates (if provided)
  * Image

### Individually redacting locality data for certain specimens

The locality data can be redacted for individual occurrences by checking the Locality Security box in the Occurrence Editor.

If you wish to batch redact data, you can download a CSV file of all the specimen records you wish to redact using the Exporter tool, then add a column called LocalitySecurity. Enter a 1 in this column for all specimens for which you wish to redact data. Use the Skeletal File Uploader to upload this spreadsheet into the portal, mapping the new column to localitysecurity.

### Globally redacting locality data for certain taxa

Locality data and images can be redacted for all occurrences by a specific taxon by someone with superadministrator or taxon editor permissions. To do this, find the species in the Taxonomic Tree Viewer or Taxonomy Explorer and open the editor (either by clicking on the taxon name or clicking the pencil next to the name). Change the Locality Security field  to "hide locality data".

![Taxonomy Editor Example](/symbiota-docs/images/taxoneditorexample.PNG)

This will hide locality data for all occurrences of that taxon throughout the portal. Collections can opt out of this option by individually unchecking the Locality Security box or contacting their portal administrator for batch changes.

### Redacting data by state

Finally, locality data and images can be redacted for occurrences of a given taxon that were collected in a certain state by managing a "Rare, threatened, protected species list". A rare species administrator can create a species list specifically for managing sensitive species and then assign editing rights to one to several appropriate users for populating and managing the state list. The addition of a species to the list will automatically protect locality details of all specimens collected within the designated state. While localities details are protected from general users, collection managers and selected approved users will still be able to access the all locality information, map specimen records, and view label images.

#### Instructions for creating state-based redacted species lists

1. Create a new empty rare species checklist.
    * Click “My Profile”, select the Species Checklists tab, and click the green plus sign.
    * Change the Checklist Type to “Rare, threatened, protected species list”. If you don’t see the Checklist Type field located below the author field, then you probably do not have the necessary Rare Species Administration rights. In this case, you can continue creating the checklist and ask a portal administrator to change the checklist type at a later date.
    * Enter the state name in the locality field. Do not abbreviate or add any other text other than the state name.
    * The checklist can be private or public and made available to the general public
2. Add one to several editors
    * From the new checklists, click on the checklist administration editing pencil located towards the user right of the page
    * Checklist editors do not need Rare Species Administration or any other special editing rights to manage the list
3. Checklist editors add species needing protection using the normal checklist editing tools.
    * See [checklist tutorials](https://biokic.github.io/symbiota-docs/user/checklist/) for help creating and managing checklists
