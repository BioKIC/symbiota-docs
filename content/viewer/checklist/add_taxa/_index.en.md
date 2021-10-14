---
title: "Adding Taxa to Checklist"
date: 2021-10-14
authors: ["Katie Pearson; Mary Barkworth; Ed Gilbert"]
draft: false
keywords: ["checklist","inventory","flora"]
---

{{< notice info >}} This page describes how to add taxa (species) to a checklist in a Symbiota portal. {{</ notice >}}

There are two ways to add taxa to a checklist, either individually or via batch upload. You may want to start by adding them individually so you can become familiar with the information that can be uploaded and the care one needs to take in doing so.

### Adding Individual Taxa

{{< youtube jm2_mn2nClo >}}

1. On the checklist page, click the rightmost pencil icon (labeled spp.) at the top right of the page. This will bring up a panel on the lower right side of the screen.
2. Add the name of a taxon you wish to add. Do NOT include the authorship of the taxon. You can start typing, and a dropdown list will allow you to select the taxon from available options.
    * You cannot add a name that is not present in the taxonomic thesaurus (it will tell you if this is the case). If you find that the taxon you wish to add is not present:
      1. Check that your spelling is correct. Use a vetted taxonomic resources, such as [Tropicos](http://tropicos.org) or [IPNI](http://www.ipni.org/) to check.
      2. If your spelling is correct, contact your portal manager with the name, authorship, and a reference or link to that name in another taxonomic database, and it will be added for you.
3. Fill in the other fields if desired. All of these fields can be left blank:
    * **Family Override**: If you enter the family name here, you will override the family provided by the taxonomic thesaurus. It is advised not to enter anything in this field.
    * **Habitat**: If the taxon is usually found in a particular habitat in the area circumscribed by the checklist, you can include this information here.
    * **Abundance**: Here you can note how frequently/abundantly this taxon is found in the area circumscribed by the checklist. For example, you can use terms like “common,” “frequent,” or “rare.”
    * **Notes**: Any other comments about this taxon pertaining to your checklist area can be put here, for example: “Cultivated ornamental” or “favored by honeybees” 
    * **Internal notes**: This field, unlike the others, will be visible only to people authorized to edit the checklist. You might make a note “need to check the species” or “no picture available” for example.
    * **Source**: This field is more likely to be used for research and teaching checklists. For such checklists, it is useful to know whether the information came from a flora, some other publication, or a report by some
4. Click the “Add species to List” button.

### Batch Adding Taxa

{{< youtube Hnk09MYlMVg >}}

If you have several taxa to add at one time, you can upload them in a CSV (comma separated value) file. The easiest way to create the desired listing is to use Microsoft Excel or OpenOffice Calc and then save the file as a CSV file.
In your CSV file, one column in the file should be labeled sciname. This should contain the scientific name of the taxon WITHOUT the authorship included. In this CSV file, you must be very careful to spell the scientific names correctly. If you have an error in your spelling, you will not be able to load that name into your checklist.
You can also include “family”, “habitat”, “abundance”, and “notes” columns (see above for descriptions of these fields) in this file. An example is shown below.

| Sciname             | Habitat             | Abundance | Notes                           |
|---------------------|---------------------|-----------|---------------------------------|
| Asystasia gangetica | Middle of the field | Rare      | Demonstration; correct spelling |
| Asystasia gangetca  | field               | unknown   | Demonstration; wrong spelling   |

Below is a screenshot of uploading the previous example “file”. Note that only one name, the one that was correctly spelled, was uploaded.

![Sample Checklist](/symbiota-docs/images/samplechecklist.png)

To return to the Checklist, click “Return to Checklist” at the top left of the page (underlined below).

![Return to Checklist](/symbiota-docs/images/returntochecklist.jpg)

You can then view the taxa that were added to the checklist.

![View Checklist Taxa](/symbiota-docs/images/viewchecklisttaxa.jpg)
