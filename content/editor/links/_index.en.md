---
title: "Linking Records/Resources"
date: 2021-12-08
draft: false
weight: 110
authors: ["Katie Pearson"]
keywords: ["genetic resources","DNA sequences","sequences","checklist","voucher","duplicate","associated occurrences"]
---

{{< notice info >}}
  This page describes how to link associated occurrences, checklists, duplicates, or genetic resources with occurrence records.
{{</ notice >}}

To link an occurrence with an external (or internal) resource or record, navigate to that record's occurrence editor page (see [this page](https://biokic.github.io/symbiota-docs/editor/edit/) for instructions) and click the Linked Resources tab.

![Linked Resources Tab](/symbiota-docs/images/linkedresourcestab.PNG)

### Linking associated occurrences

In the Associated Occurrences box of the Linked Resources tab, you can link an occurrence with (1) an occurrence in the portal you are currently working in, (2) an occurrence in another portal or database, and/or (3) an observational (non-vouchered) occurrence of a specific taxon.

#### Linking an occurrence to a record within the portal
1. Click the plus sign icon in the Associated Occurrences box to add a new link.
2. Enter the name of the identifier (catalog number, other catalog number, or occid/SymbiotaID number) for the occurrence to be linked in the **Identifier** box.
3. Select either Catalog Numbers or Occurrence PK from the **Search Target** dropdown list, depending on what you entered into the **Identifier** box.
4. Select the collection within the portal to which the occurrence to be linked belongs (if applicable).
5. Click the Search button.
6. From the search results, click the radio button to the left of the occurrence to which you would like to link your current occurrence.

{{< notice note >}}
  You can click the underlined portion of the occurrence search results to view the occurrence before linking it
{{</ notice >}}

![Create New Association Example](/symbiota-docs/images/createassociation.PNG)

7. Scroll down to the **Relationship** field and select the relationship term that best describes the relationship between your occurrence and the occurrence that is being linked.

{{< notice note >}}
  Note that the **subject** of the Relationship term corresponds to the occurrence that you are currently in the occurrence editor for, and the **object** of the Relationship term is the occurrence that you have searched for and are linking to. For example, if you are on the occurrence editor page for record 12345, then you use the Associated Occurrences box to find record 54321, and you select "partOf" from the dropdown menu, the relationship recorded is: "Record 12345 is part of record 54321".
{{</ notice >}}

8. Select a **Relationship subtype** and the **Basis of Record** from the dropdown menus, if applicable, and any notes in the **Notes** field.
9. If the relationship you selected was hasHost or hostOf, enter **Location on host** information, if available.
10. Click the Create Association button.

#### Linking an occurrence to a record in a different portal/database
1. Click the plus sign icon in the Associated Occurrences box to add a new link.
2. In the External Occurrence box, enter the catalog number or another identifier for the record to which you are linking in the **External Identifier** box.
3. Enter a URL that can be used to access the record to which you are linking in the **Resource URL** field. For example, here is a URL for a records from the Bryophyte Portal that could be entered: [https://bryophyteportal.org/portal/collections/individual/index.php?occid=4595185](https://bryophyteportal.org/portal/collections/individual/index.php?occid=4595185).
4. Complete steps 7-10 as above.

#### Linking an occurrence to an observation that lacks a record
1. Click the plus sign icon in the Associated Occurrences box to add a new link.
2. Enter the scientific name of the taxon that has a relationship with your occurrence.
3. Complete steps 7-10 as above.

### Linking an occurrence to a checklist
1. In the **Checklist Voucher Linkages** box of the Linked Resources tab, select the checklist to which you would like to link you occurrence from the dropdown menu. Note that you will only see checklists for which you have editor or administrator permissions.

{{< notice note >}}
  To batch link vouchers to a checklist, see the [Adding Vouchers to Checklist page](https://biokic.github.io/symbiota-docs/user/checklist/voucher/).
{{</ notice >}}

### Linking an occurrence to a duplicate specimen
There are several ways to link an occurrence to duplicate specimens. You can:
* In the Linked Resource tab of the occurrence editor, click the Search for Records to Link button in the **Specimen Duplicates** box. This will open a search window that you can use to identify and link duplicate specimens. You can search according to collector name, collector number, date, catalog number, or occid (SymbiotaID) using this tool.
* In the main Occurrence Data tab of the occurrence editor, click the Duplicates button. This will search the portal for occurrences with the same collector last name, number, and date. If a potential identical duplicate is identified, you can check the box next to Link as Duplicate, then click Transfer All Fields or Transfer to Empty Fields Only to initiate the link. This will also transfer any data from that duplicate into your specimen record. Newly transferred data will be highlighted in blue.
* Batch link records to their duplicates using the [Duplicate Clustering tool](https://biokic.github.io/symbiota-docs/coll_manager/dup).

### Linking an occurrence to a genetic resource
In the **Genetic Resources** box of the Linked Resources tab, enter information about the genetic sequence associated with your occurrence in the provided fields. Be sure to provide a URL to the sequence. Here is an example for a URL from GenBank: [https://www.ncbi.nlm.nih.gov/nuccore/BV165924.1](https://www.ncbi.nlm.nih.gov/nuccore/BV165924.1).