---
title: "Importing Determinations"
date: 2023-10-30
authors: ["Lindsay Walker"]
weight: 150
keywords: ["data upload","data import","determinations", "annotations"]
---

{{< notice note >}}
  This page provides instructions for bulk uploading specimen determinations/annotations and associating them with their respective specimen records.
{{</ notice >}}

{{< notice tip >}}
  **This tool cannot be used to overwrite existing determinations**; it can only be used to add new determinations to one or more occurrence records. Contact the Symbiota Support Hub or your Portal Manager if you need assistance deleting or replacing determinations from a large number of occurrence records. For example: 
  
  {{</ notice >}}

## Initiating the Upload

1. Navigate to your Administration Control Panel (_My Profile > Occurrence Management > name of your collection_).
2. Within the Administration Control Panel, navigate to _Import/Update Specimen Records > Extended Data Import_.
3. Select the file containing your determinations to be imported.
4. Choose _Import Type_ = "Determinations".
5. Select the desired Upload Type from the dropdown menu.


10. If your upload was successful, the message "Done process input file" will appear in the Action Panel. 


## Data Import Fields

{{< notice tip >}}
  Files containing determinations to be bulk imported must be in CSV format. Refer to the [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/) and [Data Import Fields](/symbiota-docs/coll_manager/upload/fields/) guides for more information about some of the fields listed below.
{{</ notice >}}

{{< notice tip >}}
  Not all fields available through the Extended Data Importer for bulk determination ingestion are visible through the Occurrence Editor interface. However, once imported, these values can be exported via a [full data backup](/symbiota-docs/coll_manager/download/) 
  {{</ notice >}}

| Target Field | Sample Value | Notes (🔸 = required field) |
| --- | --- | --- |
| subject identifier | | 🔸 catalogNumber, otherCatalogNumber, or occurrenceID | 
| appliedStatus | | |
| dateIdentified | | 🔸 |
| detType | | |
| family | | |
| higherClassification | | |
| identificationQualifier | | |
| identificationReferences | | |
| identificationRemarks | | |
| identificationUncertain | | |
| identificationVerificationStatus | | |
| identifiedBy | | 🔸 |
| isCurrent | Y | Use to flag a determination as the most current. Will not override existing determinations that have already been flagged at the most current. |
| printQueue | | Adds determination to the annotation print queue |
| scientificNameAuthorship | | |
| sciname | | 🔸 Does not include authorship string |
| securityStatus | | |
| securityStatusReason | | |
| sortSequence | | |
| sourceIdentifier | | |
| taxonConceptID | | |
| taxonRemarks | | |
| verbatimIdentification | | |








{{< notice tip >}}
 If you are new to bulk importing data into your portal, it is highly recommended that you import only a few records to begin with to familiarize yourself with how the tool behaves.  
  {{</ notice >}}


  

![Darwin Core Import Profile Mapping Page](/symbiota-docs/images/dwc_import_profile.JPG)


