---
title: "Redacting / Obscuring Data"
Date: 2021-11-01
authors: ["Katie Pearson"]
weight: 80
keywords: ["rare species", "data protection", "redaction"]
---

{{< notice info >}}
  This page explains how data redaction functions in a Symbiota portal.
{{</ notice >}}

Collection managers may wish to redact locality data for certain occurrences, for example, of rare or endangered species or for locations on private property. Locality data in Symbiota portals may be redacted in one of two ways: (a) individually (per occurrence) or (b) globablly (per taxon).

Redacting locality data in Symbiota portals is currently binary: an occurrence can have its locality redacted (Locality Security = 1, checked) or not (Locality Security = 0, unchecked). When the Locality Security box is checked (or Locality Security is uploaded as 1) for a given occurrence, a user who does not have rare species reader or editor permissions will not be able to view that occurrence's:
  * Locality below the level of county
  * Coordinates (if provided)
  * Image

### Individually redacting locality data for certain specimens

The locality data can be redacted for individual occurrences by checking the Locality Security box in the Occurrence Editor.

If you wish to batch redact data, you can download a CSV file of all the specimen records you wish to redact using the Exporter tool, then add a column called LocalitySecurity. Enter a 1 in this column for all specimens for which you wish to redact data. Use the Skeletal File Uploader to upload this spreadsheet into the portal, mapping the new column to localitysecurity.

### Globally redacting locality data for certain taxa

In addition, locality data and images can be redacted on a per-species level by someone with superadministrator or taxon editor permissions. To do this, find the species in the Taxonomic Tree Viewer or Taxonomy Explorer and open the editor (either by clicking on the taxon name or clicking the pencil next to the name). Change the Locality Security field  to "hide locality data".

![Taxonomy Editor Example](/symbiota-docs/images/taxoneditorexample.PNG)

This will hide locality data for all occurrences of that taxon throughout the portal. Collections can opt out of this option by individually unchecking the Locality Security box or contacting their portal administrator for batch changes.
