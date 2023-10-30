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

In this documentation, we use the terms **subject** and **object** to refer to two different types of occurrences. The **subject** record is the occurrence that you are adding associations to. The **object** record is the association or other occurrence that is being added or linked to the subject record.

### Navigating to the uploader
1. Navigate to your Administration Control Panel (My Profile > Occurrence Management > name of your collection).
2. Click Import/Update Specimen Records, then select "Extended Data Import".
3. Click the "Choose File" button to upload a properly formatted associations file into the uploader (see sections below for formatting requirements).
4. Select "Associations" from the Import Type dropdown menu.
5. Select the desired Association Type (of the four described below) from the next dropdown menu.

#### General Resource Uploads

**General Resource:** a URL to an external resource (e.g., record in a non-Symbiota database, repository for field notes) that provides information or extended data relating to the occurrence

A template for this upload type can be found here[LINK].

The required fields for this upload type are (1) an identifier for the occurrence (subject) you are linking to (occurrenceID, catalog number, and/or other catalog number), (2) association type (selected from the pulldown menu), and (3) resourceUrl. The resourceUrl should be a link to the external resource that you would like associated with your records.

#### "Occurrence - Externally Managed" Uploads

**Occurrence - Externally Managed:** a link to an occurrence (specimen/observation) that is available in another Symbiota-based portal. 

A template for this upload type can be found here[LINK].

The required fields for this upload type are (1) an identifier for the occurrence (subject) you are linking to (occurrenceID, catalog number, and/or other catalog number), (2) association type (selected from the pulldown menu), and (3) resourceUrl.

Optional fields include identifier (of the associated occurrence "object"), relationshipID, subType, basisOfRecord, verbatimSciname, locationOnHost, conditionOfAssociate, establishedDate, dynamicProperties, notes, and accordingTo.

#### "Occurrence - Internally Managed" Uploads

**Occurrence - Internally Managed:** a link to an occurrence (specimen/observation) that exists in the same portal as the occurrence you are linking to; when creating associations within a portal, the portal will automatically update the corresponding occurrence with the reciprocal relationship

A template for this upload type can be found here[LINK].

The required fields for this upload type are (1) an identifier for the occurrence (subject) you are linking to (occurrenceID, catalog number, and/or other catalog number), (2) association type (selected from the pulldown menu), and (3) an identifier for the occurrence object you are linking to the subject occurrence (occurrenceID or catalog number). The object identifier will be used to link to an existing record within the portal.

Optional fields include: 

#### Simple Observation Uploads

**Simple Observation:** the assertion of a taxon being associated with the occurrence you are linking to. This may be, for example, the host taxon of the occurrence, a parasite, a taxon sharing the same habitat, etc.

A template for this upload type can be found here[LINK].

The required fields for this upload type are (1) an identifier for the occurrence (subject) you are linking to (occurrenceID, catalog number, and/or other catalog number) and (2) scientific name (of the object association being added).

Optional fields include:


### Linked Resources Upload Fields

| Field Name                           | Data Type                                     | Description                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**_occurrenceId_**](https://dwc.tdwg.org/terms/#dwc:occurrenceID)                           | Text (255 characters)                               | The global unique identifier (GUID) of a record. |
| [**_occurrenceId_**](https://dwc.tdwg.org/terms/#dwc:occurrenceID)                           | Text (255 characters)                               | The global unique identifier (GUID) of a record. |

![Create New Association Example](/symbiota-docs/images/createassociation.PNG)


{{< notice note >}}
  Note that the **subject** of the Relationship term corresponds to the occurrence that you are currently in the occurrence editor for, and the **object** of the Relationship term is the occurrence that you have searched for and are linking to. For example, if you are on the occurrence editor page for record 12345, then you use the Associated Occurrences box to find record 54321, and you select "partOf" from the dropdown menu, the relationship recorded is: "Record 12345 is part of record 54321".
{{</ notice >}}

