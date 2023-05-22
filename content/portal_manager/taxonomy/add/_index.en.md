---
title: "Adding Taxa to the Taxonomic Thesaurus"
date: 2023-02-09
lastmod: 2023-02-09
authors: ["Katie Pearson"]
editors: [""]
draft: false
weight: 5
keywords: ["taxonomy","taxonomic thesaurus"]
---

{{< notice note >}}
  A user must have Super Administrator or Taxonomic Editor permissions to add to or edit the thesaurus.
{{</ notice >}}

There are three main ways that a user can add taxonomic names to the taxonomic thesaurus:
  1. Individually via the Taxonomy Explorer interface
  2. Automatically via the [Taxonomic Cleaning Tools](https://biokic.github.io/symbiota-docs/coll_manager/data_cleaning/taxonomy/)
  3. Batch via the [Taxonomic File Upload Tool](https://biokic.github.io/symbiota-docs/portal_manager/taxonomy/batch_load/)

Additional information about options 1 and 2 are provided below (see the link above for instructions for option 3).

### Adding taxa individually

{{< notice note >}}
  Both the parent taxon (e.g., genus of the species you would like to add) and the accepted name of the taxon (if not the name you are adding) must already be in the taxonomic thesaurus for you to add it. If either one of these is missing, you will get an error when you try to complete the form as below.
{{</ notice >}}

1. Navigate to the taxonomic thesaurus (Sitemap > scroll down to Taxonomy > Taxonomic Tree Viewer), or just add "taxa/taxonomy/taxonomydisplay.php" to your base path.
2. Click the green plus sign at the top right corner of the screen.
3. Enter information about the taxon in the provided form.
![Taxon Data Entry Form](/symbiota-docs/images/addnewtaxon.PNG)

* Enter the taxonomic name *without the authorship* in the **Taxon Name** field
* Enter the authorship into the **Author** field
* For hybrid taxa, select the multiplication symbol from the dropdown list in front of the UnitName2 field
* For infraspecific taxa, use the small UnitName3 field for the infraspecific epithet type (e.g., var., subsp., f.), if applicable, and the long UnitName3 field for the infraspecific epithet.
* Select the appropriate taxon rank from the dropdown **Taxon Rank** field
* The form will automatically parse out the UnitName1, UnitName2, and UnitName3. Adjust these if necessary.
* **IMPORTANT:** Add a link or citation for the source of the scientific name you are adding, for example, a Plants of the World Online entry, a literature citation with DOI, etc.
* If the taxonomic name you are adding is the currently accepted name, leave the *Accepted* radio button checked. If the taxonomic name is not accepted, select the *Not Accepted* radio button and enter the accepted name in the provided field. *If the name of the accepted species is not found in the taxonomic thesaurus (i.e., does not appear in the dropdown menu), you must add that name to the thesaurus first.*

{{< notice note >}}
  If you edit anything in the **Taxon Name** field after you have added to the **Author**, **Notes**, or **Source** fields, it will reset the form and clear anything you have entered into these fields.
{{</ notice >}}

### Batch adding taxa using the Taxonomic Cleaning Tool

The Taxonomic Cleaning Tool is useful not only for cleaning misspellings and errors, but also for adding taxaonomic names to the taxonomic thesaurus. If a taxonomic authority has been enabled in the symbini file, you will be able to cross-reference the un-indexed name in a collection with that taxonomic authority. Running the taxonomic cleaning tool will then auto-import any names that are not indexed in the collection that can be found in that taxonomic thesaurus. See the instructions for using the [Taxonomic Cleaning Tools](https://biokic.github.io/symbiota-docs/coll_manager/data_cleaning/taxonomy/).
