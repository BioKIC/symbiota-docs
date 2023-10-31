---
title: "Importing Determinations"
date: 2023-10-31
lastmod: 2023-10-31
authors: ["Lindsay Walker"]
editors: ["Katie Pearson"]
weight: 150
keywords: ["data upload","data import","determinations", "annotations"]
---

{{< notice info >}}
  This page provides instructions for bulk uploading specimen determinations/annotations and associating them with their respective specimen records. For instructions for adding individual determinations or the batch annotation tool, see [this page](https://biokic.github.io/symbiota-docs/editor/edit/annotations/).
{{</ notice >}}

{{< notice tip >}}
  **If you are new to using this tool**, try importing only a few new determinations to familiarize yourself with how the tool behaves before ingesting a large batch. For instance, **this tool cannot be used to overwrite existing determinations**; it can only be used to add new determinations to one or more occurrence records. Contact the Symbiota Support Hub or your Portal Manager if you need assistance deleting or replacing determinations.
 {{</ notice >}}
  
  | ![Single Determination History Form](/symbiota-docs/images/determinationhistoryform.png) |
|:--:|
| Data associated with specimen identifications (aka taxonomic determinations or annotations) can be added to specimen records in bulk using the **Extended Data Importer** tool. |


### Initiating the Upload

1. Navigate to your Administration Control Panel (_My Profile > Occurrence Management > name of your collection_).
2. Within the Administration Control Panel, navigate to _Import/Update Specimen Records > Extended Data Import_.
3. Select the file containing your determinations to be imported. See below for tips regarding the contents and formatting of this file.
4. Choose _Import Type_ = "Determinations".
5. Select the desired Upload Type from the dropdown menu.
6. If your upload was successful, the message "Done process input file" will appear in the Action Panel. 

#### Example Data Import File

Files containing determinations to be bulk imported must be in CSV format and include the following: 1) an identifier for the associated specimen occurrence (_catalogNumber_, _otherCatalogNumber_, or _occurrenceID_), 2) _dateIdentified_, 3) _identifiedBy_, and 4) _sciname_.

For example:

  | catalogNumber | identifiedBy | dateIdentified | sciname |
| --- | --- | --- | --- |
| OBI000001 | Don Cole | 1950 | Rosa woodsii var. gratissima |
| OBI000001 | unknown |  | Rosa |
| OBI000002 | Edward Gilbert | 2023-10-01 | Rosa woodsii |

### Data Import Fields

{{< notice tip >}}
 Refer to the [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/) and [Data Import Fields](/symbiota-docs/coll_manager/upload/fields/) guides for more information about some of the fields listed below.
{{</ notice >}}

{{< notice tip >}}
  Not all fields available through the Extended Data Importer for bulk determination ingestion are visible through the Occurrence Editor interface. However, once imported, these values can be exported, for example, through a [data backup](/symbiota-docs/coll_manager/download/).
  {{</ notice >}}

| Target Field (🔸 = required)| Data Type (Length)| Notes |
| --- | --- | --- |
| subject identifier 🔸 | | catalogNumber, otherCatalogNumber, or occurrenceID | 
| appliedStatus | Integer (2) | ???? ["applied" worked but "1" did not] |
| [**dateIdentified**](https://dwc.tdwg.org/terms/#dwc:dateIdentified) 🔸 | Text (45) | The date the identification was made. |
| detType | Text (45) | ???? |
| family | Text (255) | The family to which the taxon belongs. If the scientific name provided is matched to one in the taxonomic thesaurus, this will be auto-filled according to the thesaurus entry. |
| higherClassification | | ???? |
| [**identificationQualifier**](https://dwc.tdwg.org/terms/#dwc:identificationQualifier) | Text (255) | The determiner's expression of uncertainty in their identification. This will be listed on the label along with the scientific name. (e.g., cf., aff.) |
| [**identificationReferences**](https://dwc.tdwg.org/terms/#dwc:identificationReferences) | Text (2000) | The reference source used to make the identification. |
| [**identificationRemarks**](https://dwc.tdwg.org/terms/#dwc:identificationRemarks) | Text (2000) | Any additional notes regarding the identification of the specimen. |
| identificationUncertain | | ???? |
| identificationVerificationStatus | Text (45) | ???? |
| [**identifiedBy**](https://dwc.tdwg.org/terms/#dwc:identifiedBy)🔸 | Text (255) | The name of the person who identified the specimen. Also called a determiner. |
| isCurrent | Integer (2) | Use the value "Y" to flag a determination as the most current. However, doing so will not override existing determinations that have already been flagged as the most current. [Y worked but 1 didn't?!] |
| printQueue | Integer (2) | Use the value "1" to add a determination to the annotation print queue. |
| [**scientificNameAuthorship**](https://dwc.tdwg.org/terms/#dwc:scientificNameAuthorship) | Text (255) | The name of the person who first named the taxon. If the scientific name provided is matched to one in the taxonomic thesaurus, this will be auto-filled according to the thesaurus entry. |
| sciname 🔸 | | Taxonomic identification without authorship string. See [Data Import Fields](/symbiota-docs/coll_manager/upload/fields/). |
| securityStatus | Integer (11) | Use the value "1" to [redact images and locality data](/symbiota-docs/coll_manager/data_publishing/redaction/) for the associated occurrence record; use "0" to keep all details visible. See [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/). [DOES NOT SEEM TO WORK?] |
| securityStatusReason | Text (100) | Explanation for data redaction. See [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/). |
| sortSequence | Integer (10) | Specifies the sequential sort order of multiple determinations on the determination history tab and in the public display. Low numbers will sort higher than high numbers. |
| sourceIdentifier | Text (45) | Identifier for the source of the taxonomic information, such as [https://powo.science.kew.org/taxon/](https://powo.science.kew.org/taxon/urn:lsid:ipni.org:names:673954-1) [urn:lsid:ipni.org:names:673954-1](https://powo.science.kew.org/taxon/urn:lsid:ipni.org:names:673954-1) |
| [**taxonConceptID**](https://dwc.tdwg.org/terms/#dwc:taxonConceptID) | Text (45) | An identifier for the taxonomic concept to which the determination refers. |
| [**taxonRemarks**](https://dwc.tdwg.org/terms/#dwc:taxonRemarks) | Text (2000) | Any additional notes regarding the taxonomic name to which the specimen was identified. |
| verbatimIdentification | Text (250) | See [dwc:verbatimIdentification](https://dwc.tdwg.org/terms/#dwc:verbatimIdentification) [UNCLEAR WHERE THIS FIELD LIVES.] |
