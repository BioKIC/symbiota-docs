---
title: "Linking Records/Resources"
date: 2021-12-08
lastmod: 2025-03-27
draft: false
weight: 110
authors: ["Katie Pearson"]
editors: ["Lindsay Walker"]
keywords: ["genetic resources","DNA sequences","sequences","checklist","voucher","duplicate","associated occurrences"]
---

{{< notice info >}}
  This page describes how to link single associated occurrences, checklists, duplicates, or genetic resources with occurrence records. For batch adding linked resources, see [this page](https://biokic.github.io/symbiota-docs/coll_manager/upload/links). Note that you must be a collection administrator to use the batch upload tool.
{{</ notice >}}

To link an occurrence with an external (or internal) resource or record, navigate to that record's occurrence editor page (see [this page](https://biokic.github.io/symbiota-docs/editor/edit/) for instructions) and click the Linked Resources tab.

 ### Table of Contents
 - [Linking to Associated Resources](#linking-associations)
   - Such as other specimen occurrences, observations, and related resources
 - [Linking to Specimen Duplicates](#linking-to-a-duplicate-specimen)
 - [Linking to Genetic Resources](#linking-to-genetic-resources-and-sequences)


![Linked Resources Tab](/symbiota-docs/images/linkedresourcestab.PNG)

### Linking Associations
### (External/Internal Resources or Occurrences)

In the Associated Occurrences box of the Linked Resources tab, you can link an occurrence with a(n) (1) external resource (not another specimen or observation) or website ("[Non-Occurrence Resource Link](#linking-an-occurrence-to-an-external-non-occurrence-resource)"), (2) Internal Occurrence ("[Occurrence - Internal (this portal)](#linking-an-occurrence-to-a-record-within-the-portal-occurrence---internal-this-portal)"), (3) occurrence in another portal or database ("[Occurrence - External Link](#linking-an-occurrence-to-a-record-in-a-different-portaldatabase)"), and/or (4) observational (non-vouchered) occurrence of a specific taxon ("[Taxon Observation](#linking-an-occurrence-to-an-observation-that-lacks-a-record)").

#### Linking to an external (non-occurrence) resource

**Non-occurrence Resource:** a URL to an external resource that provides information or extended data relating to the occurrence, but is itself not an [occurrence](https://dwc.tdwg.org/terms/#occurrence). Examples include field notes, a compiled dataset, etc.

1. Click the plus sign icon in the Associated Occurrences box to add a new link.
2. In the **Association Type** field, select "Non-Occurrence Resource Link" from the dropdown menu.
3. In the **Relationship** field, select the term that defines the relationship between your occurrence and the link that you are adding to that occurrence. The term you select refers to the occurrence as the "subject" and the linked resource as the "object". For example, if you select the relationship "siblingOf", the inferred relationship is "My occurrence is the sibling of this external link."
4. (Optional) In the **Relationship Subtype** field, select the subtype of relationship between your occurrence and the link that you are adding.
5. In the **Resource URL** field, enter the URL/link to the external resource that you would like to link to your occurrence.
6. (Optional) In the **Additional Identifier of Object** field, enter any unique identifier that belongs to the link you are adding to your occurrence.
7. Click the Create Association button.

{{< notice note >}}
  📚 **How do I create links between my specimen records and literature?**<br>
  You can use the "Non-occurrence Resource" option to create linkages between your specimen records and digitially available literature. This can be accomplished using the Linked Resources tab or by bulk importing references using the [Extended Data Import Tool](/symbiota-docs/coll_manager/upload/links/). The latter option includes [additional fields](/symbiota-docs/images/linkedresources_literatureimport.png) that are not available on the Linked Resources data entry form.
  <br><br>If you opt to directly enter create a link to a publication using the Linked Resources tab, you can create this associate by using the **Association Type** = "Non-occurrence Resource" + **Relationship** = "isReferencedBy" and including a stable **Resource URL** (permalink or DOI) that points directly to the external resource, as shown below ([example](https://library.big-bee.net/portal/collections/individual/index.php?occid=4003313)). 
  ![Linked Resources Tab](/symbiota-docs/images/linkedresources_literaturedirectentry.png)
{{</ notice >}}

#### Linking to a record within the same portal

**Occurrence - Internal (this portal):** a link to an occurrence (specimen/observation) that exists in the same portal as the occurrence you are linking to; when creating associations within a portal, the portal will automatically update the corresponding occurrence with the reciprocal relationship

1. Click the plus sign icon in the Associated Occurrences box to add a new link.
2. In the **Association Type** field, select "Occurrence - Internal (this portal)" from the dropdown menu.
3. In the **Relationship** field, select the term that defines the relationship between your occurrence and the link that you are adding to that occurrence. The term you select refers to the occurrence as the "subject" and the linked resource as the "object". For example, if you select the relationship "siblingOf", the inferred relationship is "My occurrence is the sibling of this external link."
4. (Optional) In the **Relationship Subtype** field, select the subtype of relationship between your occurrence and the link that you are adding.
5. (Optional) In the **Basis of Record** field, select the basis of the evidence of a relationship between your occurrence and the link that you are adding.
6. (Optional) In the **Location on host** field, enter the location of the occurrence on the host occurrence (e.g., "mid-gut").
7. (Optional) In the **Notes** field, enter any notes associated with the relationship.
8. In the **Identifier** field, enter the catalog number or Symbiota number ("occid") of the occurrence that exists in this same portal that you you would like to link to this occurrence, then select either Catalog Numbers or Occurrence PK (occid) from the **Search Target** dropdown menu, depending on what you entered.
9. In the **Search Collections** dropdown menu, select which collection you would like to search through to find the occurrence you want to link to this occurrence, or leave at "All Collections" to search all collections in this portal. Click the Search button.
10. In the **Occurrence Matches Available to Link** box, click the radio button to the left of the occurrence to which you would like to link your current occurrence. If there is a scientific name in that occurrence, it will automatically populate the **Verbatim Scientific Name** field.
11. Click the Create Association button.

{{< notice note >}}
  You can click the underlined portion of the occurrence search results to view the occurrence before linking it
{{</ notice >}}

![Create New Internal Association Example](/symbiota-docs/images/createinternalassociation.PNG)

#### Linking to a record in a different portal/database

**Occurrence - External Link:** a link to an occurrence (specimen/observation) that is available in another data portal / database (e.g., another Symbiota portal, GBIF, Arctos, etc.). 

1. Complete the same steps 1-7 from "[Occurrence - Internal](#linking-an-occurrence-to-a-record-within-the-portal-occurrence---internal-this-portal)", as applicable, but select "Occurrence - External Link" from the **Association Type** dropdown menu.
2. In the **Resource URL** field, enter the URL/link to the external resource that you would like to link to your occurrence.  For example, here is a URL for a records from the Bryophyte Portal that could be entered: [https://bryophyteportal.org/portal/collections/individual/index.php?occid=4595185](https://bryophyteportal.org/portal/collections/individual/index.php?occid=4595185).
3. (Optional) In the **Additional Identifier of Object** field, enter any unique identifier that belongs to the occurrence object that you are linking to your occurrence subject.
4. (Optional) In the **Verbatim Scientific Name** field, enter the name of the taxon represented by your external resource that you would like to link to your occurrence.
5. Click the Create Association button.

{{< notice note >}}
  📸 **How do I create links between my specimen records and [iNaturalist](https://www.inaturalist.org/)?**<br>
  If your collection contains a preserved specimen that directly corresponds to an observation in iNaturalist, you can use the "Occurrence - External Link" option to create a link between these records. This can be accomplished using the Linked Resources tab or by bulk importing references using the [Extended Data Import Tool](/symbiota-docs/coll_manager/upload/links/). (Note: If the iNaturalist image does not precisely capture a preserved specimen but still contains relevant information, we suggest using the "Non-occurrence Resource Link Option", described above.)
  <br><br>You can create this association by using the **Association Type** = "Occurrence - External Link" + **Relationship** = "derivedFromSameIndividual" + **Basis of Record** = "HumanObservation" and including the direct URL to the iNaturalist record as the **Resource URL**, as shown below.
  ![Linked Resources Tab](/symbiota-docs/images/linkedresources_iNaturalist.png)
{{</ notice >}}

#### Linking to an observation that lacks a record ("Taxon Observation")

**Taxon Observation:** the assertion of a taxon being associated with the occurrence you are linking to. This may be, for example, the host taxon of the occurrence, a parasite, a taxon sharing the same habitat, etc.

1. Complete the same steps 1-7 from "[Occurrence - Internal](#linking-an-occurrence-to-a-record-within-the-portal-occurrence---internal-this-portal)", as applicable, but select "Taxon Observation" from the **Association Type** dropdown menu.
2. In the **Verbatim Scientific Name** field, enter the name of the taxon that you would like to link to your occurrence.
3. Click the Create Association button.

### Linking to a Checklist
* In the **Checklist Voucher Linkages** box of the Linked Resources tab, select the checklist to which you would like to link you occurrence from the dropdown menu. Note that you will only see checklists for which you have editor or administrator permissions.

{{< notice note >}}
  To batch link vouchers to a checklist, see the [Adding Vouchers to Checklist page](https://biokic.github.io/symbiota-docs/user/checklist/voucher/).
{{</ notice >}}

### Linking to a Duplicate Specimen
There are several ways to link an occurrence to duplicate specimens. You can:
* In the Linked Resource tab of the occurrence editor, click the Search for Records to Link button in the **Specimen Duplicates** box. This will open a search window that you can use to identify and link duplicate specimens. You can search according to collector name, collector number, date, catalog number, or occid (SymbiotaID) using this tool.
* In the main Occurrence Data tab of the occurrence editor, click the Duplicates button. This will search the portal for occurrences with the same collector last name, number, and date. If a potential identical duplicate is identified, you can check the box next to Link as Duplicate, then click Transfer All Fields or Transfer to Empty Fields Only to initiate the link. This will also transfer any data from that duplicate into your specimen record. Newly transferred data will be highlighted in blue.
* Batch link records to their duplicates using the [Duplicate Clustering tool](https://biokic.github.io/symbiota-docs/coll_manager/dup).


### Linking to Genetic Resources and Sequences
* In the **Genetic Resources** box of the Linked Resources tab, enter information about the genetic sequence associated with your occurrence in the provided fields. Be sure to provide a URL to the sequence. Here is an example of an acceptable URL from GenBank: [`https://www.ncbi.nlm.nih.gov/nuccore/BV165924.1`](https://www.ncbi.nlm.nih.gov/nuccore/BV165924.1). In addition to adding these links one-by-one through the Linked Resources tab, genetic data can also be associated with specimen records in batch by mapping these URLs to _associatedSequences_ as a [bulk data upload](https://biokic.github.io/symbiota-docs/coll_manager/upload/).

  {{< youtube H76eeKxECEs >}}