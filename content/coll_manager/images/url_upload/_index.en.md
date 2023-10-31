---
title: "Image URL Upload"
date: 2023-10-31
lastmod: 2023-10-31
weight: 1
authors: ["Katie Pearson"]
keywords: ["images"]
---

{{< notice info >}}
  This page describes how to link images to records from a CSV of image links/URLs.
{{</ notice >}}

### Adding Images via URLs
  1. Navigate to your Administration Control Panel (My Profile > Occurrence Management > name of your collection).
  2. Click Import/Update Specimen Records, then select "Extended Data Import".
  3. Click the "Choose File" button to upload a properly formatted associations file into the uploader (see sections below for formatting requirements).
  4. Select "Image Field Map" from the Import Type dropdown menu.
  5. Click the "Initialize Import" button.
  6. Map the fields in your input file (shown on the left) to appropriate target fields (see table below).
  7. If you would like to create a new record for each identifier that does not match an existing identifier in the system, check the box labeled "Link image to new blank record if catalog number does not exist."
  8. Click the Import Data button.

### Setting Up an Image Import File
A template for this upload type can be found [here](https://biokic.github.io/symbiota-docs/documents/GeneralResourceUploadTemplate.xlsx).

The required fields for this upload type are (1) a subject identifier for the occurrence you are linking to (occurrenceID, catalog number, and/or other catalog number), and (2) originalUrl. The originalUrl should include a direct link to the desired image (i.e., ideally ending in .jpg or .tif or some other image file extension). Note that uploading a link to a webpage where that image may be found rather than directly to the image may result in images not displaying as expected.

Optional fields are listed in the table below.

### Image Url Mapping Fields

|--------------------------------|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| subject identifier: [**catalogNumber**](https://dwc.tdwg.org/terms/#dwc:catalogNumber)                           | Text (32)                               | The primary human-readable identifier for the record you are linking the image to. |
| subject identifier: [**otherCatalogNumbers**](https://dwc.tdwg.org/terms/#dwc:otherCatalogNumbers)                           | Text (45)                               | An alternative catalog number stored as an "Additional Identifier" in the portal for the record you are linking the image to. See [this page](https://biokic.github.io/symbiota-docs/editor/edit/fields/catno/) for more context. |
| subject identifier: [**occurrenceID**](https://dwc.tdwg.org/terms/#dwc:occurrenceID)                           | Text (255)                               | The global unique identifier (GUID) of the record you are linking the image to. |
| [**accessRights**](https://dwc.tdwg.org/terms/#dcterms:accessRights)                           | Text (255)                               | Information about who can access the resource or an indication of its security status.
 |