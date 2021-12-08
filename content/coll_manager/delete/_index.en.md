---
title: "Deleting Records"
date: 2021-12-08
draft: false
weight: 60
authors: ["Katie Pearson"]
keywords: ["delete","remove"]
---

{{< notice info >}}
  This page describes how to delete records from your collection.
{{</ notice >}}

Only users with Administrator permissions can delete a specimen record, and only the portal manager(s) or someone with backend access can delete more than one specimen record at a time. This is designed to protect data integrity, such as GUIDs and links to other tables in the database.

Deleting a specimen record is only appropriate when that specimen no longer exists or the record was added erroneously (e.g., it was an exact duplicate of an existing record). You should not delete a record for the purpose of updating it or adding a new version of the record.

To delete a record, navigate to the occurrence editor page of that record (see [this page](https://biokic.github.io/symbiota-docs/editor/edit/) for help navigating to specific records) and click the Admin tab. Click the “Evaluate record for deletion” button to determine whether the record can be safely deleted. If an image exists for the record, you will need to disassociate the image from the specimen (see the [deleting/remapping images page](https://biokic.github.io/symbiota-docs/editor/images/delete/)) prior to deleting the record. If there are no warnings at this point, click the Delete Occurrence button.

To batch delete records, contact your portal manager.