---
title: "Processing Status"
date: 2024-06-10
draft: false
authors: ["Lindsay Walker"]
keywords: ["crowdsourcing", "transcription", "editing"]
---

{{< notice info >}}
 This page explains how to automatically update _Processing Status_ while editing occurrence records.
{{</ notice >}}

{{< notice note >}}
 _Processing Status_ integrates with the [Crowdsourcing module](/symbiota-docs/editor/crowdsource/) when _Processing Status_="Unprocessed" **and** a record has at least one associated image. Additionally, this field can be used to track workflow- or project-specific needs as it is not publicly visible.
{{</ notice >}}

{{< notice note >}}
_Status Auto-Set_ is user-specific and relies on browser cookies to function.
{{</ notice >}}

### Set Processing Status
_Processing Status_ and _Status Auto-Set_ are located under the Curation section of the Occurrence Editor form:
![Occurrence Editor Tabs](/symbiota-docs/images/processingstatus.png)

#### Manually
_Processing Status_ can be manually updated from within the Curation box on the Occurrence Editor. This method is most useful when making on-off edits to records that do not requiore extensive workflow tracking.

#### Automatically
The _Status Auto-Set_ menu is used for making changes to _Processing Status_ when multiple records are to be edited. If a user needs to edit numerous records, but they do not want to remember to manually update the _Processing Status_ as they work, _Status Auto-Set_ can be used to automatically update this field, for example, during image transcription. Once _Status Auto-Set_ is set, any records a user subsequently edits will receive that new _Processing Status_ value. 

### Query Records by _Processing Status_
_Processing Status_ values can be queried using the Data Editor Search Form (_Data Editor Control Panel > Edit Existing Occurrence Records_): 
![Occurrence Editor Tabs](/symbiota-docs/images/processingstatusquery.png)