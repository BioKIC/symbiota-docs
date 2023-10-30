---
title: "Linked Resources / Associations"
date: 2023-10-30
lastmod: 2023-10-30
draft: false
weight: 40
authors: ["Katie Pearson"]
keywords: ["associated occurrences","extended specimen","linked resources","batch upload"]
---

{{< notice info >}}
  This page describes how to batch upload associated occurrences or other linked resources to your records. For general information about linked resources or to upload individual linked resources, see [this page](https://biokic.github.io/symbiota-docs/editor/links).
{{</ notice >}}

There are four types of associations supported by the tool described here:
1. **General Resource:** a URL to an external resource (e.g., record in a non-Symbiota database, repository for field notes) that provides information or extended data relating to the occurrence
2. **Occurrence - Externally Managed:** **Symbiota Occurrence - Other portal:** a link to an occurrence (specimen/observation) that is available in another Symbiota-based portal. 
3. **Occurrence - Internally Managed:** **Symbiota Occurrence - This portal:** a link to an occurrence (specimen/observation) that exists in the same portal as the occurrence you are linking to; when creating associations within a portal, the portal will automatically update the corresponding occurrence with the reciprocal relationship
4. **Simple Observation:** the assertion of a taxon being associated with the occurrence you are linking to. This may be, for example, the host taxon of the occurrence, a parasite, a taxon sharing the same habitat, etc.

### General Resource Uploads
A template for this upload type can be found here[LINK].

The required fields for this upload type are (1) an identifier field for the occurrence you are linking to (occurrenceID, catalog number, and/or other catalog number), (2) association type (selected from the pulldown menu), and (3) resourceUrl.

### Linked Resources Upload Fields

| Field Name                           | Data Type                                     | Description                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**_occurrenceId_**](https://dwc.tdwg.org/terms/#dwc:occurrenceID)                           | Text (255 characters)                               | The global unique identifier (GUID) of a record. |


![Create New Association Example](/symbiota-docs/images/createassociation.PNG)


{{< notice note >}}
  Note that the **subject** of the Relationship term corresponds to the occurrence that you are currently in the occurrence editor for, and the **object** of the Relationship term is the occurrence that you have searched for and are linking to. For example, if you are on the occurrence editor page for record 12345, then you use the Associated Occurrences box to find record 54321, and you select "partOf" from the dropdown menu, the relationship recorded is: "Record 12345 is part of record 54321".
{{</ notice >}}

