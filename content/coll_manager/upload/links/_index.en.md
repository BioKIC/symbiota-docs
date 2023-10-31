---
title: "Linked Resources / Associations"
date: 2023-10-30
lastmod: 2023-10-30
draft: false
weight: 40
authors: ["Katie Pearson"]
keywords: ["associated occurrences","extended specimen","linked resources","batch upload","relationships"]
---

{{< notice info >}}
  This page describes how to batch upload associated occurrences or other linked resources to your records. For general information about linked resources or to upload individual linked resources, see [this page](https://biokic.github.io/symbiota-docs/editor/links).
{{</ notice >}}

This tool uses terms **subject** and **object** to refer to two different types of occurrences. The **subject** record is the occurrence that you are adding associations to. The **object** record is the association or other occurrence that is being added or linked to the subject record.

### Uploading Linked Resources / Associations
  1. Navigate to your Administration Control Panel (My Profile > Occurrence Management > name of your collection).
  2. Click Import/Update Specimen Records, then select "Extended Data Import".
  3. Click the "Choose File" button to upload a properly formatted associations file into the uploader (see sections below for formatting requirements).
  4. Select "Associations" from the Import Type dropdown menu.
  5. Select the desired Association Type (of the four described below) from the next dropdown menu.
  6. Click the "Initialize Import" button.
  7. Select the desired Relationship type from the dropdown menu 
  8. Map the fields in your input file (shown on the left) to appropriate target fields (see table below).
  9. If you would like to overwrite previously-uploaded associations with identical values of the "identifier" field, check the box labeled "Update records with matching 'identifiers' ".
  10. Click the Import Data button.

#### General Resource Uploads

**General Resource:** a URL to an external resource (e.g., record in a non-Symbiota database, repository for field notes) that provides information or extended data relating to the occurrence

A template for this upload type can be found [here](https://biokic.github.io/symbiota-docs/documents/GeneralResourceUploadTemplate.xlsx).

The required fields for this upload type are (1) a subject identifier for the occurrence you are linking to (occurrenceID, catalog number, and/or other catalog number), (2) association type (selected from the pulldown menu in the portal), (3) relationships type (selected from the pulldown menu in the portal), and (4) resourceUrl. The resourceUrl should be a link to the external resource that you would like to be associated with your records.

Optional fields include accordingTo, basisOfRecord, establishedDate, identifier, notes, object identifier (catalog number, occurrenceID, or occid), relationshipID, subType, or verbatimSciname.

#### "Occurrence - Externally Managed" Uploads

**Occurrence - Externally Managed:** a link to an occurrence (specimen/observation) that is available in another Symbiota-based portal. 

A template for this upload type can be found [here](https://biokic.github.io/symbiota-docs/documents/OccurrenceExternalUploadTemplate.xlsx).

The required fields for this upload type are (1) a subject identifier for the occurrence you are linking to (occurrenceID, catalog number, and/or other catalog number), (2) association type (selected from the pulldown menu in the portal), (3) relationship (selected from the pulldown menu in the portal), and (4) resourceUrl.

Optional fields include accordingTo, basisOfRecord, establishedDate, identifer, notes, object identifier (catalog number, occurrenceID, or occid), relationshipID, resourceUrl, subType, or verbatimSciname.

#### "Occurrence - Internally Managed" Uploads

**Occurrence - Internally Managed:** a link to an occurrence (specimen/observation) that exists in the same portal as the occurrence you are linking to; when creating associations within a portal, the portal will automatically update the corresponding occurrence with the reciprocal relationship

A template for this upload type can be found [here](https://biokic.github.io/symbiota-docs/documents/OccurrenceInternalUploadTemplate.xlsx).

The required fields for this upload type are (1) a subject identifier for the occurrence you are linking to (occurrenceID, catalog number, and/or other catalog number), (2) association type (selected from the pulldown menu), (3) relationship (selected from the pulldown menu in the portal), and (4) an object identifier for the occurrence object you are linking to the subject occurrence (occid, occurrenceID, or catalog number). The object identifier will be used to link to an existing record within the portal.

Optional fields include accordingTo, basisOfRecord, establishedDate, identifer, notes, relationshipID, resourceUrl, subType, and verbatimSciname.

#### Simple Observation Uploads

**Simple Observation:** the assertion of a taxon being associated with the occurrence you are linking to. This may be, for example, the host taxon of the occurrence, a parasite, a taxon sharing the same habitat, etc.

A template for this upload type can be found [here](https://biokic.github.io/symbiota-docs/documents/SimpleObservationUploadTemplate.xlsx).

The required fields for this upload type are (1) an identifier for the occurrence (subject) you are linking to (occurrenceID, catalog number, and/or other catalog number) and (2) scientific name (of the object association being added).

Optional fields include accordingTo, basisOfRecord, establishedDate, identifer, notes, object identifier (catalog number, occurrenceID, or occid), relationshipID, resourceUrl, and subType.

### Linked Resources Upload Fields

| Field Name                           | Data Type (Length in characters)                                     | Description                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| subject identifier: [**catalogNumber**](https://dwc.tdwg.org/terms/#dwc:catalogNumber)                           | Text (32)                               | The primary human-readable identifier for the subject record you are linking to. |
| subject identifier: [**otherCatalogNumbers**](https://dwc.tdwg.org/terms/#dwc:otherCatalogNumbers)                           | Text (45)                               | An alternative catalog number stored as an "Additional Identifier" in the portal for the subject record you are linking to. See [this page](https://biokic.github.io/symbiota-docs/editor/edit/fields/catno/) for more context. |
| subject identifier: [**occurrenceID**](https://dwc.tdwg.org/terms/#dwc:occurrenceID)                           | Text (255)                               | The global unique identifier (GUID) of the subject record you are linking to. |
| [**accordingTo**](https://dwc.tdwg.org/terms/#dwc:relationshipAccordingTo)                           | Text (45)                               | The source asserting the relationship between the subject and object. |
| [**basisOfRecord**](https://dwc.tdwg.org/terms/#dwc:basisOfRecord)                           | Text (45)                               | The nature of the record, from the Darwin Core controlled vocabulary. The most commonly used are _PreservedSpecimen_, _FossilSpecimen_, and _HumanObservation_. |
| [**establishedDate**](https://dwc.tdwg.org/terms/#dwc:relationshipEstablishedDate)                           | Datetime                               | The date when the relationship between the subject and the object was asserted. |
| identifier                          | Text (250)                               | A string used to identify the object record that it is not its catalog number or occurrenceID. For reference only, not used to link directly to the external or internal resource. |
| [**notes**](https://dwc.tdwg.org/terms/#dwc:relationshipRemarks)                          | Text (250)                               | Comments about the relationship between the subject and the object. |
| object identifier: [**catalogNumber**](https://dwc.tdwg.org/terms/#dwc:catalogNumber)                           | Text (32)                               | The primary human-readable identifier for the object record you are linking to the subject. |
| object identifier:occid                           | Integer (10)                               | The occid (internal Symbiota reference number) for the object record you are linking to the subject. The occid is not the same as the occurrenceID (see below). |
| object identifier: [**occurrenceID**](https://dwc.tdwg.org/terms/#dwc:occurrenceID)                           | Text (255)                               | The global unique identifier (GUID) of the object record you are linking to the subject. |
| [**relationship**](https://dwc.tdwg.org/terms/#dwc:relationshipOfResource)                           | Text (150)                               | The relationship of the subject to the object. |
| [**relationshipID**](https://dwc.tdwg.org/terms/#dwc:relationshipOfResourceID)                           | Text (45)                               | An identifier for the relationship type that connects the subject to its object.|
| resourceUrl                           | Text (250)                               | A URL/link to the object in the association/relationship.|
| subType                           | Text (45)                               | A relationship type that falls hierarchically beneath the selected relationship type.|
| verbatimSciname                           | Text (250)                               | The taxonomic name of the object of the association/relationship.|