---
title: "Batch Uploading/Linking Images"
date: 2021-10-06
weight: 1
authors: ["Ed Gilbert","Katie Pearson"]
keywords: ["images"]
---

{{< notice info >}}
  This page describes how to upload multiple images at a time or link multiple images from an external location.
{{</ notice >}}

There are several workflows used to batch upload/link specimen images. Batch processing typically consists of two separate steps: 1) Batch loading images onto a web server, and 2) Mapping image URLs to specimen records residing within the Symbiota portal. Technically, images are not stored within a Symbiota database. Instead, the URLs of the images are mapped to specimen records. Contact the portal manager to inquire about the workflow details supported by a given portal.

{{< notice tip >}}
  Images uploaded or linked to specimens in a Symbiota portal should be JPGs or in another web-friendly format. It is recommended that individual files are no larger than 8 MB to allow users with slower connectivity to view them within a reasonable timeframe.
{{</ notice >}}

### Common Workflows
* **Image Drop Folder:** Using a mapped network drive, FTP, SFTP, Dropbox, or other cloud storage, a drop folder is made available so that imaging team can regularly deposit new images. This folder is referred to as the "source folder". Once images are uploaded to the source folder, you can use the Processing Toolbox to create web-ready derivatives and move the images to a local server. The derivatives are then mapped to specimen records through image URLs.

* **Local Storage:** If images are stored on a local server that is write-accessible to the portal code, image processing can be performed directly through the portal interface. Image URLs stored locally can be mapped into the database using relative links without the domain name. In this case, the the web server user (e.g. Apache user) must have write access to both the source and target folders.

* **Remote Image Storage:** Images can also be processed and stored on a remote server and mapped to the specimen image through the full image URL. Standalone image processing scripts will be needed to process images and map image URLs to the portal database. Scripts can be configured to write the image URL directly to the database or image metadata can be written to a log file, which is loaded into the database afterwards. Remote images must be mapped into the database using the full image URL with the domain name.
  * If only a large image is made available from the remote server, the image URL can be mapped to the _urloriginal_ field, and then portal will then create local web and thumbnail dirivatives. If the images are named using the catalog number, and the web server is configured to display directory contents, the Processing Toolbox within the collection's management menu contains a method to harvest image links from the directory listing. Alternatively, one can perform a "skeletal record import" that contains a column with the catalogNumber and another associatedMedia column with the image URL.

* **CyVerse Image Storage:** This method requires an agreement of a collection with CyVerse. CyVerse can store images as Community Data files and use BisQue to create web-accessible URLs for these files. You can then use the Processing Toolbox to map CyVerse URLs to specimen records in your portal.
