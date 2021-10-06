---
title: "Importing & Uploading Data"
authors: ["Ed Gilbert"]
editors: ["Katie Pearson"]
draft: true
keywords: ["data upload","data import"]
---

{{< notice note >}}
  This page provides instructions for uploading data into an existing collection in a Symbiota portal. Contact your portal manager if you do not already have a collection in your desired Symbiota portal.
{{</ notice >}}

1. Navigate to your Administration Control Panel (My Profile > Occurrence Management > name of your collection).
2. Click Import/Update Specimen Records, then select "Create a new Import Profile".
3. Create a title for your upload in the Title field.
4. Select the desired Upload Type from the dropdown menu.
  * **Darwin Core Archive Manual Upload:** Use this upload type if the data you wish to upload is in the format of a [Darwin Core Archive](https://dwc.tdwg.org/text/). A Darwin Core Archive (DwC-A) is a data standard that is commonly used to package species occurrence data into a single, self-contained dataset ([http://en.wikipedia.org/wiki/Darwin_Core_Archive](http://en.wikipedia.org/wiki/Darwin_Core_Archive)). A DwC-A includes metadata, a file of occurrence data, and, often, files for determinations (identifications) and images.
  * **IPT Resource / Darwin Core Archive Provider:** Use this upload type if you will provide a URL to an existing Darwin Core Archive published on the web, such as one provided through an IPT.
  * **File Upload:** Use this upload type if you will provide a comma-separated value (CSV) or tab-separated value (TSV) file containing your occurrence data. You can convert an Excel document into a CSV file by clicking Save As, then selecting comma-delimited (CSV) from the file types.
  * **Skeletal File Upload:** Use this upload type if you will provide a CSV or TSV file containing data from only a few fields (e.g., georeferences or other ancillary data). Note that any data provided in a skeletal file upload will NOT overwrite existing data in the database, so any pre-existing data in the desired fields must be deleted if you wish to replace it with the data from the skeletal file.
  * **NfN File Upload:** Use this upload type if you will provide a CSV file produced from Notes from Nature.
  * **Direct Database Mapping:**
  * **Stored Procedure:**
  * **Script Upload:**
6. Create new profile with the following fields: profile title, database platform, server name or IP address, port, login name, password, schema (database) name, stored procedure with instructions for data cleaning this specific upload, and SQL statement used in querying data. Note that SQL can be written only to return a subset of data, such as records modified or added within the last month.
If collection type is a data “snapshot” of a specimen database managed within the home institution, select the primary key for source specimen record. Snapshot datasets must contain a field that will serve as the primary record identifier. This field will serve as the permanent link between the source database and the portal records. This field must be populated for every record with unique values. The values need to be stable without changing over time. Field can be numeric or text field type. The typical data used for this field is the catalog number (accession number), barcode, or database primary key from the source database specimen table.
Map source fields to the Symbiota fields. Source column names do not have to match those of Symbiota, but data type and definitions must comply with one of the Darwin Core Standards. The Automap button will automatically map and save all matching field names for future uploads. If the source SQL statement is changed, mapping will have to be adjusted to match new upload definition.
Upload data. During upload, data is placed in a temporary specimen table (uploadspectemp) so that data cleaning and integrity checks can be performed by the collection specific stored procedure.
Perform final transfer.

##Darwin Core Archive Manual Upload


##IPT Resource / Darwin Core Archive Provider


##File Upload or Skeletal File Upload


CSV File Upload – Upload flat CSV files that have been extracted from source database.

Create new profile with the following fields: profile title, stored procedure for data cleaning and integrity checks.
Select primary key for source specimen record. Field must be a non-null, unique ID for the specimen record. Field can be numeric or text field type. This field will be used to update modified records during future uploads, therefore field is required and must remain the same for all uploads.
Map source fields to the Symbiota fields. Source column names do not have to match those of Symbiota, but data type and definitions must be compliant to the one of the Darwin Core Standards. The Automap button will automatically map and save all matching field names for future uploads. If the source field definition changes, mapping will have to be adjusted to match new upload definition.
Upload data. During upload, data is placed in temporary specimen table (uploadspectemp) so that data cleaning and integrity checks can be performed. Cleaning stored procedure specific for this collection is performed on this table.
Perform final transfer.
System Script – MySQL source to Symbiota database that islocated on a different server

Write file script used to transfer records. A sample Linux script is located here: SampleSystemUpload.sh
Collection cleanup scripts can be put in central stored procedure or kept separate
Setup script to run as a regular cronjob
SQL Stored Procedure – transfer from source schema to Symbiota database located on the same MySQL database server

Write file stored procedure used to transfer records
Collection cleanup scripts can be put in central stored procedure or kept separate
Setup script to run as a regular cronjob

##Uploading Tips

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
