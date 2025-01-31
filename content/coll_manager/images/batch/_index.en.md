---
title: "Batch Uploading/Linking Images"
date: 2021-10-06
modified: 2025-01-31
weight: 1
authors: ["Ed Gilbert","Katie Pearson"]
editors: ["Katie Pearson"]
keywords: ["images"]
---

{{< notice info >}}
  This page describes general workflows for adding multiple images to a portal at one time. Technically, images are not stored within a Symbiota database. Instead, the URLs of the images are mapped to specimen records. Contact the portal manager to inquire about the workflows supported by a given portal.
{{</ notice >}}

Images associated with records in a Symbiota portal may be **Externally Hosted** or **Internally Hosted**.

* **Externally Hosted** images are those stored on servers that are unrelated to the Symbiota portal (e.g., are housed at another institution). These external servers provide image links, which can then be loaded into the Symbiota database.

* **Internally Hosted** images are those stored on servers that are write-accessible to the Symbiota portal server. For example, if you coordinate with Arizona State University to batch upload images to one of their hosted portals (e.g., SEINet, Bryophyte Portal), your images are Internally Hosted.

{{< notice tip >}}
  Images uploaded or linked to specimens in a Symbiota portal should be JPGs or in another web-friendly format. It is recommended that individual files are no larger than 8 MB to allow users with slower connectivity to view them within a reasonable timeframe.
{{</ notice >}}

#### Batch Adding Externally Hosted Images

Externally Hosted images can be added to Symbiota records using one of three primary methods: (1) using the URL mapping tool and a [spreadsheet of catalog numbers with image URLs](/symbiota-docs/coll_manager/images/url_upload/); (2) mapping a column of image links to the associatedMedia field when conducting a Full Text File Upload or Skeletal File Upload. For more information about uploading text files, see [this page](/symbiota-docs/coll_manager/upload/). If you already have data in the portal, and you just want to add image links, do NOT use Full Text File Upload; or (3) importing a Darwin Core Archive of your data with a fully-populated <a href=https://rs.gbif.org/extension/gbif/1.0/multimedia.xml target=_blank>multimedia extension</a>.

#### Batch Adding Internally Hosted Images

There are several workflows used to batch upload/link internally hosted specimen images. Batch processing typically consists of two separate steps: (1) Loading images onto a web server, and (2) Mapping image URLs to Symbiota occurrence records. Step (2) is possible when images are named according to the catalog number or other catalog number associated with the record in the portal.

Storage of a large number of images on servers associated with a Symbiota portal may require an image-hosting agreement and/or incur image-hosting costs. Check with the portal administrator for more information about your portal's image hosting allowances and workflows. For ASU-hosted servers, contact the Symbiota Support Hub (help@symbiota.org).