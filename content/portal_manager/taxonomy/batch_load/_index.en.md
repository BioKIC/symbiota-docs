---
title: "Batch Loading Taxonomic Data"
date: 2022-07-06
lastmod: 2023-06-21
authors: ["Cat Chapman"]
editors: ["Katie Pearson, Lindsay Walker"]
draft: false
weight: 10
keywords: ["taxonomy","taxonomic thesaurus"]
---

{{< notice info >}} 
 This page describes how taxonomy can be added to a Symbiota portal in bulk.
 {{</ notice >}}

{{< notice note >}}
  A user must have Super Administrator or Taxonomic Administrator permissions to add to or edit the thesaurus.
{{</ notice >}}

## Input File Format
Taxonomic names can be batch loaded into the thesaurus from a flat, structured comma- or tab-delimited text file. To upload an Excel file, first save as a CSV (comma delimited) text file. Formatting this file correctly is important to ensuring your taxonomy is successfully imported. **At minimum, the file must include a column for _ScientificName_ and the parent taxon** (i.e. the taxon that nests immediately above the scientificName in your taxonomic hierarchy).

For example, to import the name _Buccinum polaris_ Gray, 1839 your input file could include the following fields: 
| Taxon Rank| Parent | ScientificName | Family | Author | RankID | Accepted |
| - | - | - | - | - | - | - |
| species | Buccinum | Buccinum polaris | Buccinidae | Gray, 1839 | 220 | 1 |

However, if the higher taxonomy does not already exist in your portal, the following rows should also be included in your file:
| Taxon Rank| Parent | ScientificName | Family | Author | RankID | Accepted |
| - | - | - | - | - | - | - |
| division | Animalia | Mollusca | | | 30 | 1 |
| class | Mollusca | Gastropoda | | | 60 | 1 |
| order | Gastropoda | Neogastropoda | | | 100 | 1 |
| superfamily | Neogastropoda | Buccinoidea | | | 130 | 1 |
| family | Buccinoidea | Buccinidae | Buccinidae | | 140 | 1 |
| genus | Buccinidae | Buccinum | Buccinidae | | 180 | 1 |
| species | Buccinum | Buccinum polaris | Buccinidae | Gray, 1839 | 220 | 1 |


{{< button href="../../../documents/Fresh_Symbiota_Install_Animalia_Sample_Taxonomy_2023-06-21.csv" text="Download example CSV" >}}
{{< button href="https://github.com/BioKIC/symbiota-docs/blob/master/static/documents/Fresh_Symbiota_Install_Animalia_Sample_Taxonomy_2023-06-21.csv" text="View example as a CSV" >}}

Note that *_rankid_* is assigned on the backend of your database in the table, _taxonunits_. This value may vary between Symbiota portals. 

## Using the Batch Loader
If your user account has the appropriate permissions, you can batch upload taxonomy from a spreadsheet (CSV) or text file by navigating to _Sitemap > Taxonomy > Batch Upload a Taxonomic Data File > Taxa Upload_.
![Taxonomy Batch Upload Tool](/symbiota-docs/images/taxonomybatchloader.png)

## Tips for batch importing taxonomy
- If you have never batch imported taxonomy into your portal before,do a few test imports first to be sure your new taxon records are ingesting correctly. 
- For especially complex taxonomic trees, import higher taxonomy first, then import new genera and species-level names.
- When the file containing is input, the rows/records will be imported in the order that they appear in your file i.e. row by row. For this reason, it is helpful to import higher
- If you need to add new ranks, contact the Hub or someone with backend access. Ranks are added on a per-kingdom basis. They may require community discussion in order to be added.
- When batch importing synonyms, first import all accepted names. Then import the synonyms (and their higher taxonomy, if needed). A column containing the accepted name can be included in your input file.

Parent taxa need to be already in the system or be included in the input file. As an alternative to a parent taxon column, the input file can contain columns for the core hierarchy that is defined within the taxonunits table (e.g. kingdom, division, class, subclass, order, family, etc). After selecting the upload file, it will be necessary to map the input columns to the Symbiota structure. Scientific name, with or without author imbedded, must be mapped to "scinameinput". If acceptance (0 = not accepted, 1 = accepted ) is not defined, all taxa will be assumed to be accepted. In the absence of a hierarchical definition (e.g. parent taxa), infraspecific, specific, and genus linkage will be determined from scientific name and linked to family. If family does not yet exist in thesaurus and hierarchy above family is not defined in upload field, family will be linked directly to kingdom. Make sure not to map more than one source column to the same target. Finally, make sure that source column names are unique from one another.
