---
title: "Batch Loading Taxonomic Data"
date: 2022-07-06
lastmod: 2022-07-27
authors: ["Cat Chapman"]
editors: ["Katie Pearson"]
draft: false
weight: 10
keywords: ["taxonomy","taxonomic thesaurus"]
---

{{< notice note >}}
  A user must have Super Administrator or Taxonomic Administrator permissions to add to or edit the thesaurus.
{{</ notice >}}

Taxanomic names can be batch loaded into the taxonomic thesaurus from a flat, structured comma- or tab-delimited text file. To upload an Excel file, first save as a CSV (comma delimited) text file. The following fields can be included in your CSV file:
* **Scientific name** (required)
* Taxon author
* Parent taxon name
* Family
* Accepted taxon name (if different then scientific name)

Parent taxa need to be already in the system or be included in the input file. As an alternative to a parent taxon column, the input file can contain columns for the core hierarchy that is defined within the taxonunits table (e.g. kingdom, division, class, subclass, order, family, etc). After selecting the upload file, it will be necessary to map the input columns to the Symbiota structure. Scientific name, with or without author imbedded, must be mapped to "scinameinput". If acceptance (0 = not accepted, 1 = accepted ) is not defined, all taxa will be assumed to be accepted. In the absence of a hierarchical definition (e.g. parent taxa), infraspecific, specific, and genus linkage will be determined from scientific name and linked to family. If family does not yet exist in thesaurus and hierarchy above family is not defined in upload field, family will be linked directly to kingdom. Make sure not to map more than one source column to the same target. Finally, make sure that source column names are unique from one another.
