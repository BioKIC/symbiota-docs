---
title: "Importing & Uploading Data"
authors: ["Ed Gilbert"]
editors: ["Katie Pearson"]
draft: true
keywords: ["data upload","data import","file upload","IPT"]
---

{{< notice note >}}
  This page provides instructions for uploading data into an existing collection in a Symbiota portal. Contact your portal manager if you do not already have a collection in your desired Symbiota portal.
{{</ notice >}}

# Initiating the Upload

1. Navigate to your Administration Control Panel (My Profile > Occurrence Management > name of your collection).
2. Click Import/Update Specimen Records, then select "Create a new Import Profile".
3. Create a title for your upload in the Title field.
4. Select the desired Upload Type from the dropdown menu.
    * **Darwin Core Archive Manual Upload:** Use this upload type if the data you wish to upload is in the format of a [Darwin Core Archive](http://en.wikipedia.org/wiki/Darwin_Core_Archive). A Darwin Core Archive (DwC-A) is a data standard that is commonly used to package species occurrence data into a single, self-contained dataset. A DwC-A includes metadata, a file of occurrence data, and, often, files for determinations (identifications) and images.
    * **IPT Resource / Darwin Core Archive Provider:** Use this upload type if you will provide a URL to an existing Darwin Core Archive published on the web, such as one provided through an IPT.
    * **File Upload:** Use this upload type if you will provide a comma-separated value (CSV) or tab-separated value (TSV) file containing ALL fields of your occurrence data. You can convert an Excel document into a CSV file by clicking Save As, then selecting comma-delimited (CSV) from the file types. Note that, if data exists in the portal for any of the occurrences you are uploading, those data will be overwritten by the incoming data. To upload partial records, use a Skeletal File Upload.
    * **Skeletal File Upload:** Use this upload type if you will provide a CSV or TSV file containing data from only a few fields (e.g., georeferences or other ancillary data). Note that any data provided in a skeletal file upload will NOT overwrite existing data in the database, so any pre-existing data in the desired fields must be deleted if you wish to replace it with the data from the skeletal file.
    * **NfN File Upload:** Use this upload type if you will provide a CSV file produced from Notes from Nature.
    * **Direct Database Mapping:**
    * **Stored Procedure:** Use this option if you are transferring from a source schema to a Symbiota database located on the same MySQL database server.
    * **Script Upload:** Use this option if you are transferring from a MySQL source to Symbiota database that is located on a different server.

5. Follow the directions below according to the Upload Type you have selected.

## Darwin Core Archive Manual Upload
[Contribute to this section!](https://biokic.github.io/symbiota-docs/contribute/)

## IPT Resource / Darwin Core Archive Provider
[Contribute to this section!](https://biokic.github.io/symbiota-docs/contribute/)

## File Upload or Skeletal File Upload
1. If you or your portal manager have created a Stored Procedure with data cleaning or other checks, enter the name of the stored procedure in the provided field. Otherwise, ignore this step.
2. Click the Create Profile button.
3. On the next page, you will see a list of existing upload profiles. Select the profile that you wish to use (the one you just greated) and click Initialize Upload.
    * To edit your upload profile in the future, you can click the pencil icon on this page.
4. Click the Choose File button and navigate to the file that you wish to upload in your File Manager or Finder window. Select that file and click Open.
5. Click the Analyze File button.
6. If the collection to which you are uploading data is live managed (the portal is your database system), proceed to step 7. If the collection to which you are uploading data is a “snapshot” of a specimen database managed within the home institution, select the primary key for the source specimen record from the dropdown menu. The primary key is a required field for snapshot datasets that will serve as the primary record identifier (the permanent link between the source database and the portal records). This field must be populated for every record with unique values. These values must also be stable and not changed in the central database over time. Snapshots will typically use the catalog number (accession number), barcode, or database primary key from the source database specimen table for this field.
7. You will then see a page that will look similar to the one shown below. The length and contents of the Source Field/Target Field table will depend on what columns were included in the original CSV file.

![Example of Data Upload Module](https://github.com/BioKIC/symbiota-docs/blob/master/static/images/DataUploadModule.png)

8. Select which fields in your CSV file (**Source Fields**) will correspond to which fields in the Symbiota portal (**Target Fields**). Check the [Symbiota Data Field Guide](http://symbiota.org/docs/symbiota-occurrence-data-fields-2/) for definitions of each data field. Also see the **Uploading Tips** section below.
9. Once you are satisfied with your field-to-field mapping (see next Notes), click the “Save Mapping” button.
10. Select whether you would like the script to match the data in your file to existing data in the portal based on Catalog Number or Other Catalog Numbers. You will only need to do this if you are adding data to records that already exist in the portal. Otherwise, leave these unchecked.
11. Select the Processing Status that you would like to apply to all your uploaded records (if desired) by selecting an option from the dropdown menu.
12. Click the Start Upload button. This will upload your data into a *temporary* table so you can review it before committing the final upload.
13. Verify that the correct number of records are being updated and/or added by viewing the Pending Data Transport Report on the next page.

![Screenshot of Pending Data Transfer Report](https://github.com/BioKIC/symbiota-docs/blob/master/static/images/PendingDataTransport.png)

14. View the data that have been stored in the temporary table to ensure correct mapping and formatting of the fields you are uploading. You can either:
    * Click the small box icon to the right of "Records to be updated" or "New records" to view the records in a table in your browser.
    * Click the multiple file icon to the right of the box icon to download a CSV file of the records to be updated or new records.
15. If anything is incorrect, fix your CSV file and re-upload it according to the steps you followed above, or return to your field mapping and fix the field mapping. If everything looks good, click the Transfer Records to Central Specimen Table button. **Note that this step is final and is not possible to undo!**

## Stored Procedure

1. Write a stored procedure used to transfer records (the collection cleanup scripts can be put in central stored procedure or kept separate)
2. Set up the script to run as a regular cronjob.

## Script Upload

1. Write a stored procedure used to transfer records. A sample Linux script is located here: [SampleSystemUpload.sh](http://symbiota.org/docs/wp-content/uploads/SampleSystemUpload.sh). The cleanup scripts can be put in central stored procedure or kept separate.
2. Set up the script to run as a regular cronjob.

# Uploading Tips

* If the scientific names in your CSV file include taxonomic authorship (e.g., *Acer circinatum* Pursh), map this field to the Target Field “scientificname.” If the scientific names included in your CSV file do NOT include taxonomic authorship (e.g., *Acer circinatum*), map this field to “sciname.” 
* Collection dates mapped to eventDate will be evaluated and validated. Illegal dates will be placed in the verbatimEventDate field. The majority of the standard date formats are accepted, including Gregorian dates and Excel numeric date format (US only).
eventDate will be generated from separate year,month, and day field values. If month or day fields are left null, ’00’ values will be used (ex: 1954-03-00, 1965-00-00). Month field values can be numeric or text (English or Spanish).
* Scripts attempt to extract valid date values from verbatimEventDate field when the eventDate field is null. Values of ’00’ are used for missing month or day (ex: 1954-03-00, 1965-00-00)
* If your elevation field is not consistently in meters, map it to the verbatimElevation field. Elevations in feet will be converted to meters as long as the units are specified in the field.
* Coordinate values:
  * Upon upload, background scripts will attempt to extract lat/long coordinate values from the verbatimCoordinates field. The field is evaluated for DMS and UTM formats, which are converted to decimal latitude and longitude.
  * If you have lat/long in a single field, you can map this field to verbatimCoordinates, and decimal latitude and longitude fields will be automatically parsed.
  * If you have UTM coordinates in multiple fields, map the fields (northing, easting, zone) to their matching UTM fields (utmnorthing, utmeasting, utmzone). This will instigate conversion of UTM coordinates to decimal latitude and longitude. The values will additionally be stored in the verbatiumCoordinates field.
  * If you have UTM coordinates in a single field, map this field to utmnorthing and leave other UTM fields null in order to direct scripts to parse using only the UTM parser.
  * TRS coordinates (Public Lands Survey System) can be entered as a single field into verbatimCoordinates, or into separate fields (trstownship, trsrange, trssection, trssectiondetails); however, these coordinates will not be automatically converted into decimal degrees due to potential differences in interpretation. See the georeferencing section of this guide (coming soon) for information about converting TRS coordinates to decimal degrees.
