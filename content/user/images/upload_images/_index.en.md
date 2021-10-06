---
title: "Uploading Images"
date: 2021-10-06
weight: 3
draft: false
authors: ["Ed Gilbert","Katie Pearson"]
keywords: ["images"]
---

{{< notice info >}}
  This page describes how to upload *field* and *specimen* images directly into a Symbiota portal. It is also possible to link images that are stored in external servers. For information about the latter option, visit the [Linking Images from External Sources](https://biokic.github.io/symbiota-docs/user/images/linking_images/) page.
{{</ notice >}}

There are three catefories of images that can be linked to a Symbiota portal. Instructions for uploading each of these types are provided below.

### Field image without location information

Images without specific locality information (e.g. lat/long coordinates) are linked only to the scientific name of the organism. These images can be viewed on the Taxon Profile Page, which has general information such as descriptions, distribution maps, synonyms, and common names. To upload an image:

1. Log in to your account in the portal.
{{< notice note >}}
  You must have Taxon Profile Editor permissions to do the following
{{</ notice >}}
2. Navigate to the page of the taxon you wish to edit. To do so, you may be able to:
    *  Click Sitemap, then Taxonomic Tree Viewer or Taxonomy Explorer. Search for the taxon of interest and click its name.
    *  Perform a quick search on the home page for the taxon of interest.
3. Click the pencil icon at the top right corner of the taxon page.
4. Click the Add Image tab.
5. Select the image file you would like to upload from Choose File, then enter any additional information in the provided fields.
    * The **Sort Sequence** field allows you to determine the order of the images that will show up on the taxon profile. The higher the number, the further down the priority list the image will be.
7. Click the Upload Image button.
8. Field images are uploaded and managed through the Taxon Profile Editing interface. Users with Taxon Profile editing permissions can submit an image by clicking on the editing symbol located in the upper right of any Taxon Profile page, or through the image submission links available on the sitemap page. Field images with specific locality details (e.g. coordinates) can be loaded as Image Vouchers (see below). 

### Image Vouchers (field images with location information)

### Specimen images
Note that if the image is given a sort order value of greater than 500, that image will be displayed on the Occurrence Details page but not on the Species Profile display. This is typically done for images of poor quality or due to aesthetic issues (e.g. road kills). Specimen images can be added via the user interface by clicking on the Image tab within the Occurrence Editor. See below for screen captures of the Occurrence Editor interface. See the Image Batch Loading page for workflows being used to load images in mass. A field image can be linked to a specimen record, but the image must be of the specific individual that was collected. Field images of a vouchered specimen are considered high valued images since species identifications can be verified or annotated years afterwards by close inspection of the physical specimen.
