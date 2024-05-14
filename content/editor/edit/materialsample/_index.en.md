---
title: "Material Samples"
date: 2023-09-29
draft: false
authors: ["Lindsay Walker"]
weight: 10
keywords: ["Material Sample"]
---

{{< notice info >}}
  This page describes how to add and edit material sample records associated with specimen occurrences. This tab will only be visible if it has been activated for your collection. Contact your Collection Administrator or Portal Manager to find out if this tab has been configured for your Symbiota portal.
{{</ notice >}}

| ![Material Sample Module](/symbiota-docs/images/materialsampleblank.png) |
|:--:|
| Material Sample tab within the Occurrence Editor |

## Material Sample Data Fields

Definitions for data fields displayed on the Material Sample tab are defined in the [Symbiota Data Fields](/symbiota-docs/editor/edit/fields/#material-sample-fields) documentation.

## Adding/Editing Material Sample Records

{{< notice note >}}
 One specimen occurrence in a Symbiota portal can be associated with one or more material samples. 
{{</ notice >}}

### Adding Individual Material Samples

| ![Material Sample Example](/symbiota-docs/images/materialsampleeditor.png) |
|:--:|
| Specimen occurrence with multiple associated material sample records as viewed from within the Occurrence Editor. [This example](https://biorepo.neonscience.org/portal/collections/individual/index.php?occid=277316) is from the NEON Biorepository's Symbiota portal. |

**To add a new material sample to an existing catalog record:**

1) Navigate to the Occurrence Editor: _My Profile > Occurrence Records > name of collection > Edit Existing Records_
2) [Search](/symbiota-docs/editor/edit) for the record that the sample will be associated with. Open the record so that the Occurence Editor form appears.
3) At the top of the form, select the Material Sample tab.
4) Select the plus sign icon to begin adding a new material sample.
5) As you fill out the form, consult the [Symbiota definitions for Material Sample data fields](/symbiota-docs/editor/edit/fields/#material-sample-fields) if you are unfamiliar with these terms.
6) Select the "Add Record" button to save the new material sample record.
7) Repeat, starting at step 5, to add additional material sample records.

{{< notice tip >}}
  To **edit** existing material sample records, navigate to the Material Sample tab and select the pencil icon (✏️) to reopen the editable form.
{{</ notice >}}

### Batch Adding Material Samples

At present, material sample records cannot be [batch uploaded](/symbiota-docs/coll_manager/upload/) from within a Symbiota portal's user interface, which is a task reserved for users with Administrator permissions. Collection Administrators are advised to contact the Symbiota Support Hub for assistance if this is desired. 

### Downloading Material Samples
Data entered into the Material Sample tab can be [downloaded](/symbiota-docs/editor/download/dwc/) from Symbiota as Darwin Core Archive or Symbiota data backup file. The output file will be named _materialSample.csv_.
