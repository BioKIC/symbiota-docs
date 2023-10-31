---
title: "Importing Determinations"
date: 2023-10-31
lastmod: 2023-10-31
authors: ["Lindsay Walker"]
editors: ["Katie Pearson"]]
weight: 150
keywords: ["data upload","data import","determinations", "annotations"]
---

{{< notice note >}}
  This page provides instructions for bulk uploading specimen determinations/annotations and associating them with their respective specimen records.
{{</ notice >}}

{{< notice tip >}}
  **If you are new to using this tool**, it is highly recommended that you first import only a few new determinations to familiarize yourself with how the tool behaves before ingesting numerous records. For instance, **this tool cannot be used to overwrite existing determinations**; it can only be used to add new determinations to one or more occurrence records. Contact the Symbiota Support Hub or your Portal Manager if you need assistance deleting or replacing determinations.
 {{</ notice >}}
  
  | ![Example GBIF publisher page](/symbiota-docs/images/determinationhistoryform.png) |
|:--:|
| Data associated with specimen identifications (aka taxonomic determinations or annotations) can be added to specimen records in bulk using the **Extended Data Importer** tool. |


## Initiating the Upload

1. Navigate to your Administration Control Panel (_My Profile > Occurrence Management > name of your collection_).
2. Within the Administration Control Panel, navigate to _Import/Update Specimen Records > Extended Data Import_.
3. Select the file containing your determinations to be imported. See below for tips regarding the contents and formatting of this file.
4. Choose _Import Type_ = "Determinations".
5. Select the desired Upload Type from the dropdown menu.
6. If your upload was successful, the message "Done process input file" will appear in the Action Panel. 

### Example Data Import File

Files containing determinations to be bulk imported must be in CSV format and include the following: 1) an identifier for the associated specimen occurrence (_catalogNumber_, _otherCatalogNumber_, or _occurrenceID_), 2) _dateIdentified_, 3) _identifiedBy_, and 4) _sciname_.

For example:

  | catalogNumber | identifiedBy | dateIdentified | sciname |
| --- | --- | --- | --- |
| OBI000001 | Don Cole | 1950 | Rosa woodsii var. gratissima |
| OBI000001 | unknown |  | Rosa |
| OBI000002 | Edward Gilbert | 2023-10-01 | Rosa woodsii |

## Data Import Fields

{{< notice tip >}}
 Refer to the [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/) and [Data Import Fields](/symbiota-docs/coll_manager/upload/fields/) guides for more information about some of the fields listed below.
{{</ notice >}}

{{< notice tip >}}
  Not all fields available through the Extended Data Importer for bulk determination ingestion are visible through the Occurrence Editor interface. However, once imported, these values can be exported, for example, through a [data backup](/symbiota-docs/coll_manager/download/).
  {{</ notice >}}

| Target Field (🔸 = required)| Type | Notes |
| --- | --- | --- |
| subject identifier 🔸 | | catalogNumber, otherCatalogNumber, or occurrenceID | 
| appliedStatus | int(2) | ???? ["applied" worked but "1" did not] |
| dateIdentified 🔸 | | See [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/) |
| detType | varchar(45) | ???? |
| family | | ???? See [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/). |
| higherClassification | | ???? |
| identificationQualifier | | See [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/). |
| identificationReferences | varchar(2000) | See [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/). |
| identificationRemarks | varchar(2000) | See [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/). |
| identificationUncertain | | ???? |
| identificationVerificationStatus | varchar(45) | ???? |
| identifiedBy🔸 | | See [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/). |
| isCurrent | int(2) | Use the value "Y" to flag a determination as the most current. However, doing so will not override existing determinations that have already been flagged as the most current. [Y worked but 1 didn't?!] |
| printQueue | int(2) | Use the value "1" to add a determination to the annotation print queue. |
| scientificNameAuthorship | | See [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/). |
| sciname 🔸 | | Taxonomic identification without authorship string. See [Data Import Fields](/symbiota-docs/coll_manager/upload/fields/). |
| securityStatus | int(11) | Use the value "1" to [redact images and locality data](/symbiota-docs/coll_manager/data_publishing/redaction/) for the associated occurrence record; use "0" to keep all details visible. See [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/). [DOES NOT SEEM TO WORK?] |
| securityStatusReason | varchar(100) | Explanation for data redaction. See [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/). |
| sortSequence | int(10) | Specifies the sequential sort order of multiple determinations [ON THE DETERMINATION HISTORY TAB?] |
| sourceIdentifier | varchar(45) | Identifier for the source of the taxonomic information, such as https://powo.science.kew.org/taxon/urn:lsid:ipni.org:names:673954-1 |
| taxonConceptID | varchar(45) | See [dwc:taxonConceptID](https://dwc.tdwg.org/terms/#dwc:taxonConceptID). |
| taxonRemarks | varchar(2000) | See [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/). |
| verbatimIdentification | | See [dwc:verbatimIdentification](https://dwc.tdwg.org/terms/#dwc:verbatimIdentification) [UNCLEAR WHERE THIS FIELD LIVES.] |



