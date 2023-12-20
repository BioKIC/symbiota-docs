---
title: "Data Import Fields"
date: 2021-10-22
authors: ["Ed Gilbert"]
weight: 10
editors: ["Katie Pearson"]
keywords: ["data upload","data import","file upload","IPT"]
---

{{< notice note >}}
  This page lists the possible specimen fields that can be imported into a Symbiota data portal. The type of field (text, number, etc.) is listed in the **Type** field. The number of characters allowed in that field is displayed in parentheses.
{{</ notice >}}

If the data portal is being used to displaying a “snapshot” of your data stored in your local central database, the upload file MUST have a field that serves as the unique identifier for each incoming specimen record (dbpk). This field serves a link between the source record and the snapshot record within the portal. If import is a CSV file, the first row must contain field names. Note that field names do not have to match the name used below, but there cannot be any characters ($#@&%) in the column names.

For more information about data fields, also see our [Symbiota Data Fields](https://biokic.github.io/symbiota-docs/editor/edit/fields/) page.

*Italic* = Darwin Core fields<br/>
**Bold** = strongly encouraged fields, though none of the fields are technically required<br/>
\* = for import only, merged into another field after import

{{< notice info >}}
  For Darwin Core fields, click on the link in the "Name" column to see the DwC field definition.
{{</ notice >}}

| Name | Type | Notes |
|-|-|-|
| **dbpk** | Text (45) | Specimen record unique identifier (primary key) of source database (record id). Barcode, occurrenceID (GUID), or a database Primary Key is ideal. Can also be catalogNumber, given that it is populated for each record and enforced as unique. Required if collection is “snapshot” of a central database. Not needed if collection is managed directly within portal. |
| [**_occurrenceId_**](https://dwc.tdwg.org/terms/#dwc:occurrenceID) | Text (255) | Occurrence Global Unique Identifier (GUID) |
| [**_catalogNumber_**](https://dwc.tdwg.org/terms/#dwc:catalogNumber) | Text (32) | Barcode or Accession number |
| [_otherCatalogNumbers_](https://dwc.tdwg.org/terms/#dwc:otherCatalogNumbers) | Text (255) | To take advantage of the [Tag Name + Identifier system](https://biokic.github.io/symbiota-docs/editor/edit/fields/catno/) (in which you can tag an identifier/other catalog number with a specific title), enter the tag name followed by a colon and then the identifier value, e.g., "Old Accession Number: 12345". For multiple identifiers, separate the tag name + identifiers by semicolons, e.g., "NP #: 4321; Accession #: 9876" |
| [**_family_**](https://dwc.tdwg.org/terms/#dwc:family) | Text | This need only be provided when the scientific name is not in the taxonomic thesaurus, or you would like to override the automatically-assigned family that would come from the taxonomic thesaurus.
| [_scientificname_](https://dwc.tdwg.org/terms/#dwc:scientificName) | Text (255) | Scientific name w/ authorship. The authorship will be parsed from the name. |
| [**_sciname_**](https://dwc.tdwg.org/terms/#dwc:genericName) | Text (255) | Scientific name without author |
| [_genus_](https://dwc.tdwg.org/terms/#dwc:genus) | Text (255)  | |
| [_specificEpithet_](https://dwc.tdwg.org/terms/#dwc:specificEpithet) | Text (255) | |
| [_taxonRank_](https://dwc.tdwg.org/terms/#dwc:taxonRank) | Text (32) | Rank name of infraspecific abbreviation (e.g., var., subsp.) allowed |
| [_infraspecificEpithet_](https://dwc.tdwg.org/terms/#dwc:infraspecificEpithet) | Text (255) | |
| [_scientificNameAuthorship_](https://dwc.tdwg.org/terms/#dwc:scientificNameAuthorship) | Text (255) | Author of scientific name |
| [_identifiedBy_](https://dwc.tdwg.org/terms/#dwc:identifiedBy) | Text (255) | |
| [_dateIdentified_](https://dwc.tdwg.org/terms/#dwc:dateIdentified) | Text (45) | |
| [_identificationReferences_](https://dwc.tdwg.org/terms/#dwc:identificationReferences) | Text | |
| [_identificationRemarks_](https://dwc.tdwg.org/terms/#dwc:identificationRemarks) | Text | |
| [_identificationQualifier_](https://dwc.tdwg.org/terms/#dwc:identificationQualifier) | Text (255) | cf, aff. etc |
| [_typeStatus_](https://dwc.tdwg.org/terms/#dwc:typeStatus) | Text (255) | |
| [**_recordedBy_**](https://dwc.tdwg.org/terms/#dwc:recordedBy) | Text (255) | Primary collector/observer name. All other collectors should be placed in the "associatedCollectors" field. |
| [**_recordNumber_**](https://dwc.tdwg.org/terms/#dwc:recordNumber) | Text (45) | Collector number |
| \*recordNumberPrefix | Text (45)  | Merged into recordNumber |
| \*recordNumberSuffix | Text (45)  | Merged into recordNumber |
| associatedCollectors | Text (255) | All collectors except the primary collector. |
| [**_eventDate_**](https://dwc.tdwg.org/terms/#dwc:eventDate) | Date/Time | Date collected, or earliest date of collection, if a range is provided, formatted as YYYY-MM-DD. If other formatting is used, or if date ranges are included, map to the "verbatimEventDate" field instead. |
| eventDate2 | Date/Time | Latest date collected, when a range is provided. **Note:** This field is not yet accessible in the occurrence editor. |
| [_year_](https://dwc.tdwg.org/terms/#dwc:year) | Integer (4) | If eventDate is null, year-month-day will be used to build the eventDate. |
| [_month_](https://dwc.tdwg.org/terms/#dwc:month) | Integer (4) | |
| [_day_](https://dwc.tdwg.org/terms/#dwc:day) | Integer (4) | |
| [_verbatimEventDate_](https://dwc.tdwg.org/terms/#dwc:verbatimEventDate) | Text (255) | Map collection/observation date to this field when it is not YYYY-MM-DD standardized, when dates are incomplete, or when date ranges are present. |
| [_habitat_](https://dwc.tdwg.org/terms/#dwc:habitat) | Text | Information about the environmental conditions in which the specimen was collected. |
| substrate | Text (500) | The soil or other substrate (e.g., bark, rock) on which a sessile organism was found. In Darwin Core Archive exports, this field is concatenated into "habitat".| 
| host | | Currently concatenated into associatedTaxa |
| [_occurrenceRemarks_](https://dwc.tdwg.org/terms/#dwc:occurrenceRemarks) | Text | General notes or remarks about the occurrence/specimen. |
| [_dataGeneralizations_](https://dwc.tdwg.org/terms/#dwc:dataGeneralizations) | Text (250) | Notes or remarks about the record. This field is not publicly accessible, so it is a good place to put curatorial notes or temporary comments. |
| [_informationWithheld_](https://dwc.tdwg.org/terms/#dwc:informationWithheld) | Text (250) | E.g., "coordinates not provided due to rare species" |
| [_associatedTaxa_](https://dwc.tdwg.org/terms/#dwc:associatedTaxa) | Text | Associated taxa delimited by commas or semicolons |
| [_associatedMedia_](https://dwc.tdwg.org/terms/#dwc:associatedMedia) | Text | URL to jpg images, delimited by commas or semicolons. More information about uploading images can be found on [this page](https://biokic.github.io/symbiota-docs/editor/images/upload/). |
| [_associatedOccurrences_](https://dwc.tdwg.org/terms/#dwc:associatedOccurrences)  | | **Note:** This field is not yet accessible in the occurrence editor.|
| [_associatedSequences_](https://dwc.tdwg.org/terms/#dwc:associatedSequences) | | **Note:** This field is not yet accessible in the occurrence editor.|
| [_associatedReferences_](https://dwc.tdwg.org/terms/#dwc:associatedReferences) | | **Note:** This field is not yet accessible in the occurrence editor.|
| [_dynamicProperties_](https://dwc.tdwg.org/terms/#dwc:dynamicProperties) | Text | |
| verbatimAttributes | Text | Verbatim description of organism (e.g. 1.5m tall, flowers white with purple tips, etc). In the occurrence editor, this field is usually labeled "Description". |
| [_behavior_](https://dwc.tdwg.org/terms/#dwc:behavior) | Text (500) | |
| [_reproductiveCondition_](https://dwc.tdwg.org/terms/#dwc:reproductiveCondition) | Text (255) | e.g. sterile, flw, frt, asci, etc. Use of controlled vocabulary is preferred. |
| cultivationStatus | Integer | 0 = wild, 1 = cultivated |
| [_establishmentMeans_](https://dwc.tdwg.org/terms/#dwc:establishmentMeans) | Text (45) | Use of a controlled vocabulary is preferred (see Darwin Core link). |
| [_lifeStage_](https://dwc.tdwg.org/terms/#dwc:lifeStage) | Text (45) | |
| [_sex_](https://dwc.tdwg.org/terms/#dwc:sex) | Text (45) | |
| [_individualCount_](https://dwc.tdwg.org/terms/#dwc:individualCount) | Text (45) | |
| [_samplingProtocol_](https://dwc.tdwg.org/terms/#dwc:samplingProtocol) | Text (100) | |
| [_samplingEffort_](https://dwc.tdwg.org/terms/#dwc:samplingEffort) | Text (200) | |
| [_preparations_](https://dwc.tdwg.org/terms/#dwc:preparations) | Text (100) | |
| [_locationID_](https://dwc.tdwg.org/terms/#dwc:locationID) | | |
| [_parentLocationID_](https://dwc.tdwg.org/terms/#dwc:parentLocationID) | | **Note:** This field is not yet accessible in the occurrence editor. |
| [_continent_](https://dwc.tdwg.org/terms/#dwc:continent) | | **Note:** This field is not yet accessible in the occurrence editor. |
| [_waterBody_](https://dwc.tdwg.org/terms/#dwc:waterBody) | | **Note:** This field is not yet accessible in the occurrence editor. |
| [_islandGroup_](https://dwc.tdwg.org/terms/#dwc:islandGroup) | | **Note:** This field is not yet accessible in the occurrence editor. |
| [_island_](https://dwc.tdwg.org/terms/#dwc:island) | | **Note:** This field is not yet accessible in the occurrence editor. |
| [**_countryCode_**](https://dwc.tdwg.org/terms/#dwc:countryCode) | | |
| [**_country_**](https://dwc.tdwg.org/terms/#dwc:country) | Text (64) | |
| [**_stateProvince_**](https://dwc.tdwg.org/terms/#dwc:stateProvince) | Text (255) | |
| [**_county_**](https://dwc.tdwg.org/terms/#dwc:county) | Text (255) | |
| [_municipality_](https://dwc.tdwg.org/terms/#dwc:municipality) | Text (255) | |
| [**_locality_**](https://dwc.tdwg.org/terms/#dwc:locality) | Text | |
| [_locationRemarks_](https://dwc.tdwg.org/terms/#dwc:locationRemarks) | Text | |
| localitySecurity | Integer | 0=don’t hide locality details from general public, 1=hide locality |
| localitySecurityReason | Text (100) | Description of why a locality is hidden from public view. |
| [**_decimalLatitude_**](https://dwc.tdwg.org/terms/#dwc:decimalLatitude) | Double (8) | |
| [**_decimalLongitude_**](https://dwc.tdwg.org/terms/#dwc:decimalLongitude) | Double (8) | For USA records, value is negative |
| [_geodeticDatum_](https://dwc.tdwg.org/terms/#dwc:geodeticDatum) | Text (255) | WGS84, NAD83, NAD27, etc |
| [**_coordinateUncertaintyInMeters_**](https://dwc.tdwg.org/terms/#dwc:coordinateUncertaintyInMeters) | Integer | |
| [_footprintWKT_](https://dwc.tdwg.org/terms/#dwc:footprintWKT) | Text | |
| [_verbatimCoordinates_](https://dwc.tdwg.org/terms/#dwc:verbatimCoordinates) | Text (255) | e.g. UTM: 12N 334543 5463754; 34° 25’N 113° 43’W |
| \*verbatimLatittude | Text (255) | These and following fields are used to generate decimal lat/lng; merged into verbCoor. |
| \*verbatimLongitude | Text (255) | |
| \*latDeg | Integer | Latitude degrees |
| \*latMin | Double | Latitude minutes |
| \*latSec | Double | Latitude seconds |
| \*latNS | Text (3) | North/south hemisphere. Should be either N or S. |
| \*lngDeg | Integer | Longitude degrees |
| \*lngMin | Double  | Longitude minutes |
| \*lngSec | Double | Longitude seconds |
| \*lngEW | Text (3) | East/west hemisphere. Should be either E or W. |
| \*UtmNorthing | Text (45) | The northing value for UTM coordinates (e.g., "5463754" for the UTM coordinates 12N 334543 5463754) |
| \*UtmEasting | Text (45) | The easting value for UTM coordinates (e.g., "334543" for the UTM coordinates 12N 334543 5463754) |
| \*UtmZoning | Text (45) | The zone value for UTM coordinates (e.g., "12N" for the UTM coordinates 12N 334543 5463754)|
| \*trsTownship | Text (45) | The township value (with direction) for U.S. township-range-section (TRS, or public land survey system) coordinates. (e.g., "6S" for the TRS coordinates T6S R23E section 34)|
| \*trsRange | Text (45) | The range value (with direction) for U.S. township-range-section (TRS, or public land survey system) coordinates. (e.g., "23E" for the TRS coordinates T6S R23E section 34)|
| \*trsSection | Text (45) | The section for U.S. township-range-section (TRS, or public land survey system) coordinates. (e.g., "34" for the TRS coordinates T6S R23E section 34)|
| \*trsSectionDetails | Text (45) | Any additional details, such as quarter or sixteenth sections, for U.S. township-range-section (TRS, or public land survey system) coordinates. |
| [_georeferenceProtocol_](https://dwc.tdwg.org/terms/#dwc:georeferenceProtocol) | Text (255) | |
| [_georeferenceSources_](https://dwc.tdwg.org/terms/#dwc:georeferenceSources) | Text (255) | |
| [_georeferenceRemarks_](https://dwc.tdwg.org/terms/#dwc:georeferenceRemarks) | Text (255) | |
| [_georeferencedBy_](https://dwc.tdwg.org/terms/#dwc:georeferencedBy) | Text (255) | |
| [_georeferencedDate_](https://dwc.tdwg.org/terms/#dwc:georeferencedDate) | | |
| [_georeferenceVerificationStatus_](https://dwc.tdwg.org/terms/#dwc:georeferenceVerificationStatus) | Text (32) | |
| [**_minimumElevationInMeters_**](https://dwc.tdwg.org/terms/#dwc:minimumElevationInMeters) | Integer | If the elevation is a single value in meters, only use this field |
| [_maximumElevationInMeters_](https://dwc.tdwg.org/terms/#dwc:minimumElevationInMeters) | Integer | |
| \*elevationNumber | Integer | Use this field for the elevation values (i.e., numbers) when your elevation values and units fields are separated. These will be concatenated into verbatimElevation. |
| \*elevationUnits | Text (45) | Use this field for the elevation units when your elevation values and units fields are separated. These will be concatenated into verbatimElevation. |
| [_verbatimElevation_](https://dwc.tdwg.org/terms/#dwc:verbatimElevation) | Text (255) | Use this field when your elevation values and units are in the same field (e.g., "1200 ft") and when your elevations are not consistently in meters. |
| [_minimumDepthInMeters_](https://dwc.tdwg.org/terms/#dwc:minimumDepthInMeters) | Integer | |
| [_maximumDepthInMeters_](https://dwc.tdwg.org/terms/#dwc:maximumDepthInMeters) | Integer | |
| [_verbatimDepth_](https://dwc.tdwg.org/terms/#dwc:verbatimDepth) | Text (50) | |
| [_disposition_](https://dwc.tdwg.org/terms/#dwc:disposition) | Text (32) | Can be used to put storage location information, if needed. |
| [_basisOfRecord_](https://dwc.tdwg.org/terms/#dwc:basisOfRecord) | Text (32) | |
| [_institutionCode_](https://dwc.tdwg.org/terms/#dwc:institutionCode) | Text (32) | Populate only if different than source collection (i.e., the [metadata](https://biokic.github.io/symbiota-docs/coll_manager/metadata/) associated with your collection) |
| [_collectionCode_](https://dwc.tdwg.org/terms/#dwc:collectionCode) | Text (32) | Populate only if different than source collection (i.e., the [metadata](https://biokic.github.io/symbiota-docs/coll_manager/metadata/) associated with your collection) |
| [_ownerInstitutionCode_](https://dwc.tdwg.org/terms/#dwc:ownerInstitutionCode) | | |
| [_organismID_](https://dwc.tdwg.org/terms/#dwc:organismID) | | |
| [_materialSampleID_](https://dwc.tdwg.org/terms/#dwc:materialSampleID) | | |
| exsiccatiIdentifier | Integer | Identifier from exsiccati indexing table |
| exsiccatiNumber | | (Documentation coming soon!) |
| exsiccatiNotes | | |
| duplicateQuantity | Used for printing labels. This field is not publicly accessible. | |
| labelProject | Used for printing labels. This field is not publicly accessible. | |
| processingStatus | Processing status for digitization tasks. This field is not publicly accessible. | |
| recordEnteredBy | Text (250) | Data entry personnel |
| [_modified_](https://dwc.tdwg.org/terms/#dcterms:modified) | Date/Time | Date last modified in the source database. Further edits within the Symbiota portal will be stored in a separate table. |
