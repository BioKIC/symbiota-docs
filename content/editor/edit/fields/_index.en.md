---
title: "Symbiota Data Fields"
date: 2014-07-21
lastmod: 2023-12-19
draft: false
authors: ["Ed Gilbert"]
editors: ["Laura Rocha Prado","Katie Pearson", "Lindsay Walker"]
keywords: ["edit","fields","data fields", "terms", "dwc terms", "paleontology fields", "material sample fields"]
---

The Symbiota data schema is strongly aligned to the <a href="https://www.tdwg.org/standards/dwc/" target="_blank" rel="noopener noreferrer">Darwin Core</a> data exchange standard. For more details, links to the Darwin Core definitions are supplied for each term. Learn more about Darwin Core terms in the following TDWG pages:
- [TDWG - Darwin Core quick reference guide](https://dwc.tdwg.org/terms/)
- [TDWG - List of Darwin Core terms](https://dwc.tdwg.org/list)

{{< notice note >}}
  Fields listed here differ from the fields visible in the data uploading tools. For field information specific to the data upload tools, see the [Data Import fields page](https://biokic.github.io/symbiota-docs/coll_manager/upload/fields/).
{{</ notice >}}

 ### Table of Contents
 - [Standard Fields](#standard-fields)
 - [Material Sample Fields](#material-sample-fields)
 - [Paleontology Fields](#paleontology-fields)

{{< notice note >}}
  Since portals have the ability to customize the field names found on their data entry form, field names may differ from the core field definition and how it is mapped to Darwin Core export tools.
{{</ notice >}}

{{< button href="../../../documents/SymbiotaDataFields_202111.csv" text="Download full content as a CSV" >}}
{{< button href="https://github.com/BioKIC/symbiota-docs/blob/master/static/documents/SymbiotaDataFields_202111.csv" text="See full content as a CSV" >}}

### Standard Fields

{{< dwc-term id="catalogNumber" verbatim="Catalog Number" descr="The unique identifier (primary key) for the specimen record. This field should be used to store the barcode or the accession number (herbaria only). This field is enforced to be unique per collection" ex="WIS-L-0123456, ASU0012345, 12345" dwc="catalogNumber" >}}


<a id="otherCatalogNumbers"><b>Additional Identifier Values:</b></a> Any other identifier for a specimen record that is not the central catalog number. This field is typically used to store the old catalog numbers, accession numbers, National Park identifiers, etc. Identifiers can be assigned a tag name to distinguish it from other identifiers (e.g. old accession #, NPS#, etc). These identifiers map best to dwc:otherCatalogNumbers definition, and thus included in the exports under this field. More information about this system can be found on the <a href="https://biokic.github.io/symbiota-docs/editor/edit/fields/catno/" target="_blank" rel="noopener noreferrer">Catalog Numbers documentation page</a>.<br>Ex: 12345, TUZI 3082, NPS Acc #: GUIS-M-00126.<br>See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:otherCatalogNumbers" target="_blank" rel="noopener noreferrer">otherCatalogNumbers</a>

{{< dwc-term id="recordedBy" verbatim="Collector" descr="The name of the person who collected the specimen or made the observation." ex="C.G. Pringle, Goodding, L.N." dwc="recordedBy" >}}

{{< dwc-term id="associatedCollectors" verbatim="Associated Collectors" descr="Other collectors that were present at the time of collection." ex="John R. Reeder, A. Nelson" obs="This field is not defined by the Darwin Core standard, which places primary and secondary collectors concatenated the recordedBy field." >}}

{{< dwc-term id="recordNumber" verbatim="Number" descr="The collection number assigned to the specimen by the collector." ex="1294, 12490b, 94-132" dwc="recordNumber" >}}

{{< dwc-term id="eventDate" verbatim="Date" descr="The date the specimen was collected or, if a range of dates is indicated, the first day in the range of collecting dates. While dates can be entered using your preferred format, the value will be converted and stored as an ISO-8601 numeric format (YYYY-MM-DD). Note that unknown month and days can be entered as \"00\". For example, a collection with a date of \"March 1956\" can be entered as \"1956-03-00\"." ex="1983-09-15, 1983-07-00, 1934-00-00" dwc="eventDate" >}}

<a id="endDate"><b>End Date: </b></a>The last date of collection, in the case of a range of collecting dates. While dates can be entered using your preferred format, the value will be converted and stored as an ISO-8601 numeric format (YYYY-MM-DD). Note that unknown month and days can be entered as \"00\". For example, a collection with a date of \"March 1956\" can be entered as \"1956-03-00\".<br>Ex: 1983-09-15, 1983-07-00, 1934-00-00 </br> See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:eventDate" target="_blank" rel="noopener noreferrer">eventDate</a>

{{< dwc-term id="verbatimEventDate" verbatim="Verbatim Date" descr="Can be used to record date exactly as entered on label. Particularly useful for non-standard date formats or date ranges." ex="Spring 1901, March-April 1952, late Sept. 1909" dwc="verbatimEventDate" >}}

{{< dwc-term id="year" verbatim="Year" descr="The numeric value of the year at the time of collection. This field (along with month and day) is automatically populated when the date is entered." ex="1959" dwc="year" >}}

{{< dwc-term id="month" verbatim="Month" descr="The numeric value of the month at the time of collection. This field (along with year and day) is automatically populated when the date is entered." ex="10" dwc="month" >}}

{{< dwc-term id="day" verbatim="Day" descr="The numeric value of the day at the time of collection. This field (along with year and month) is automatically populated when the date is entered." ex="28" dwc="day" >}}

<a id="dayRange"><b>Day of year range:</b></a> A range of collection dates can be represented here as numeric day of year values. These values will be automatically calculated if you enter a date range in the verbatim date field (e.g. 12 Sept 1968 to 19 Sept 1968, 1968-09-12 to 1968-09-19) <br>
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:startDayOfYear" target="_blank" rel="noopener noreferrer">startDayOfYear</a>, <a href="http://rs.tdwg.org/dwc/terms/index.htm#endDayOfYear" target="_blank" rel="noopener noreferrer">endDayOfYear</a>.

{{< dwc-term id="scientificName" verbatim="Scientific Name" descr="The Latin name of the specimen without the author. Could be anything from kingdom down to subspecies or variety, depending on the level of the identification." ex="Pinaceae, Pinus, Pinus edulis, Pinus edulis var. fallax" dwc="scientificName" >}}

{{< dwc-term id="scientificNameAuthorship" verbatim="Author" descr="The name of the person who first named the taxa. This field autofills after entering the scientific name." ex="L., Asa A. Gray" dwc="scientificNameAuthorship" >}}

{{< dwc-term id="identificationQualifier" verbatim="Identification Qualifier" descr="The determiner's expression of uncertainty in their identification. This will be listed on the label along with the scientific name." ex="cf., aff." dwc="identificationQualifier" >}}

{{< dwc-term id="family" verbatim="Family" descr="The family to which the taxa belongs. This field autofills after entering the scientific name." ex="Pinaceae" dwc="family" >}}

{{< dwc-term id="identifiedBy" verbatim="Identified By" descr="The name of the person who identified the specimen. Also called a determiner." ex="L. R. Landrum" dwc="identifiedBy" >}}

{{< dwc-term id="dateIdentified" verbatim="Date Identified" descr="The date the identification was made. Date can be entered as free form text and do not need to be in a standard date format." ex="1992, May 1992, 2 May 1992" dwc="dateIdentified" >}}

{{< dwc-term id="identificationReferences" verbatim="ID References" descr="The reference source used to make the identification." ex="Nesom, Guy L. 2006. Flora of North America - Asteraceae. vol. 20" dwc="identificationReferences" >}}

{{< dwc-term id="identificationRemarks" verbatim="ID Remarks" descr="Any additional notes regarding the identification of the specimen." dwc="identificationRemarks" >}}

{{< dwc-term id="taxonRemarks" verbatim="Taxon Remarks" descr="Any additional notes regarding the taxonomic name to which the specimen was identify." dwc="taxonRemarks" >}}

{{< dwc-term id="continent" verbatim="Continent" descr="The name of the continent in which the specimen was collected." ex="North America, Africa" dwc="continent" >}}

{{< dwc-term id="waterBody" verbatim="Water Body" descr="The name of the water body in which the specimen was collected." ex="Pacific Ocean, Black Sea" dwc="waterBody" >}}

{{< dwc-term id="islandGroup" verbatim="Island Group" descr="The name of the island group in which the specimen was collected." ex="Hawaiian Islands, Alexander Archipelago" dwc="islandGroup" >}}

{{< dwc-term id="island" verbatim="Island" descr="The name of the island on which the specimen was collected." ex="Cayo Coco, Maui" dwc="island" >}}

{{< dwc-term id="country" verbatim="Country" descr="The name of the country in which the specimen was collected. To aid data entry, a drop down menu will appear as one types, though names outside of the list can still be entered." ex="USA, Canada, Mexico" dwc="country" >}}

{{< dwc-term id="stateProvince" verbatim="State/Province" descr="The name of the state or province in which the specimen was collected. As one types, a selection list will appear for the given country." ex="New York, Arizona, Sonora" dwc="stateProvince" >}}

{{< dwc-term id="county" verbatim="County" descr="The name of the county in which the specimen was collected. Choose one from the drop down menu. For specimens collected outside of the United States, enter the next geographic region below state/province." ex="Maricopa" dwc="county" >}}

{{< dwc-term id="municipality" verbatim="Municipality" descr="The name of the municipality in which the specimen was collected. For specimens collected outside of the United States, enter the 4th level geographic designation." ex="Paradise Valley" dwc="municipality" >}}

{{< dwc-term id="locality" verbatim="Locality" descr="The detailed location in which the specimen was collected." ex="9.5 miles NW of Sedona along Boynton Pass Rd." dwc="locality" >}}

{{< dwc-term id="locationID" verbatim="Location ID" descr="An identifier for the set of location information (data associated with dcterms:Location). May be a global unique identifier or an identifier specific to the dataset." ex="https://opencontext.org/subjects/768A875F-E205-4D0B-DE55-BAB7598D0FD1" dwc="locationID" >}}

<a id="localitySecurity"><b>Locality Security:</b></a> Checking the Locality Security checkbox will hide locality details below the level of county from unauthorized users. This is typically done because the species is rare or threatened. Images are also hidden to protect locality details that might be viewable from the label. Users that are logged into the system and have the necessary permission to view locality details (e.g. collection managers) will continue to have access to all data. This box will automatically be checked if the species name is on any of the rare species lists &nbsp;(see sitemap). If one wishes to lock protection (on or off), click the Lock Security checkbox and/or enter a reason for security override in the text field. Leaving the locality security unlocked will allow default settings to be applied as determined by the sensitive species administrators, which is the recommendation for most records. <br>
For more information on sensitive species protection, see the page on <a href="https://biokic.github.io/symbiota-docs/user/redaction/">Sensitive Species Protection</a>. <br>
This field is not defined by the Darwin Core standard.

{{< dwc-term id="locationRemarks" verbatim="Location Remarks" descr="Comments or notes about the locality" ex="Previously known as Mt. Evans" dwc="locationRemarks" >}}

{{< dwc-term id="decimalLatitude" verbatim="Latitude and Longitude (decimal format)" descr="The geographic latitude and longitude in decimal degrees. Latitudes from the southern hemisphere and longitudes in the western hemisphere (e.g. USA) should be entered as negative values. Click on the \"Tools\" button to enter the coordinates in the degree, minute, seconds (DMS) or the UTM formats. Decimal degrees are the preferred coordinate standard as defined by Darwin Core. See below for more information on using this tool." ex="34.874022, -111.75774" dwc="decimalLatitude" >}}

{{< dwc-term id="coordinateUncertaintyInMeters" verbatim="Uncertainty (meters)" descr="The accuracy of the georeference coordinates in meters (numeric value only). This is measured as the radius of a circle where the true point would be found if known. If coordinates are collected using a GPS, than the accuracy would be the error found within the GPS unit (usually around 10m). While previously collected specimens that have coordinates on the label recorded by the collector typically do not state the source of the coordinates (GPS, map, etc), it is typically a good assumption that the coordinates are accurate within one to two hundred meters. If the locality details are vague such as just \"Grand Canyon\", then the coordinates should be the centroid within the uncertainty encompassing the greater area where the specimen may have been collected. If the locality is \"Boynton Canyon, Sedona\", the uncertainty would be about 1500 m. This field autofills when using GeoLocate for georeferencing." ex="42000 for Phoenix, 20000 for Salt Lake City" dwc="coordinateUncertaintyInMeters" >}}

{{< dwc-term id="geodeticDatum" verbatim="Datum" descr="The geographic system that was used to get the coordinates. This field autofills when using [http://www.museum.tulane.edu/geolocate/|GeoLocate] or the Mapping tool for georeferencing." ex="NAD27, NAD83, WGS84" dwc="geodeticDatum" >}}

<a id="verbatimCoordinates"><b>Verbatim Coordinates:</b></a> If the coordinates recorded on the specimen label are in a format other than decimal degrees, enter them here. When decimal lat/long fields are blank and one enters UTM or DMS using one of the formats displayed in the example below, decimal lat/long values will be automatically generated. Click the "&lt;&lt;" symbol to replace existing decimal values. This field autofills when using the DMS, UTM, and TRS georeferencing tools.<br>
Ex: 34° 13.940' N 112° 2.370' W, 12 420944E 4064025N, TRS: T40N R32E S29 <br>
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:verbatimCoordinates" target="_blank" rel="noopener noreferrer">verbatimCoordinates</a>.

{{< dwc-term id="minimumElevationInMeters" verbatim="Elevation in Meters" descr="The elevation in meters at which the specimen was collected. Also called altitude. Use only the left field with the right field blank when a single elevation exists." ex="1400, 2000-2200" dwc="minimumElevationInMeters" >}}

<a id="verbatimElevation"><b>Verbatim Elevation:</b></a> The verbatim elevation at which the specimen was collected. This is typically used to record an elevation measurement that was recorded in feet or an uncertainty designation. When the elevation in meters field is left blank, the value will automatically be converted to meters. Click the "&lt;&lt;" symbol to replace the previously entered meters values.<br>
Ex: 4500ft, 4500 feet, ca 4500', ca 2000m, 4500' +-300'<br>
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:verbatimElevation" target="_blank" rel="noopener noreferrer">verbatimElevation</a>.

<a id="minimumDepthInMeters"><b>Depth in Meters:</b></a> The range of depth below the local surface, in meters.<br>
Ex: 100, 150-200<br>
See Darwin Core's <a href="http://rs.tdwg.org/dwc/terms/minimumDepthInMeters" target="_blank" rel="noopener noreferrer">minimumDepthInMeters</a>, <a href="https://dwc.tdwg.org/terms/#dwc:maximumDepthInMeters" target="_blank" rel="noopener noreferrer">maximumDepthInMeters</a>.

{{< dwc-term id="verbatimDepth" verbatim="Verbatim Depth" descr="The original verbatim description of the depth below the local surface at which the specimen was collected." ex="100ft, 100 feet, ca 100', ca 30m, 100' +-10'" dwc="verbatimDepth" >}}

{{< dwc-term id="georeferencedBy" verbatim="Georeferenced By" descr="The name of the person who georeferenced the specimen record. This field autofills when using GeoLocate for georeferencing." ex="A. Gonzales, emakings, acbarber" dwc="georeferencedBy" >}}

{{< dwc-term id="georeferenceProtocol" verbatim="Georeference Protocol" descr="The source of the standards used to georeference." ex="Georeferencing Quick Guide. Zermoglio et al. 2020" dwc="georeferenceProtocol" >}}

{{< dwc-term id="georeferenceSources" verbatim="Georeference Sources" descr="The tool or tools used to georeference." ex="GeoLocate, Google Earth, USGS map" dwc="georeferenceSources" >}}

{{< dwc-term id="georeferenceVerificationStatus" verbatim="Georef Verificiation Status" descr="Says whether or not the georeference has been reviewed or verified." ex="reviewed, not reviewed" dwc="georeferenceVerificationStatus" >}}

{{< dwc-term id="georeferenceRemarks" verbatim="Georeference Remarks" descr="Any additional notes regarding the georeferencing of the specimen." dwc="georeferenceRemarks" >}}

{{< dwc-term id="habitat" verbatim="Habitat" descr="The description of the habitat in which the specimen was collected." ex="Wet areas along a small stream in chaparral." dwc="habitat" >}}

{{< dwc-term id="substrate" verbatim="Substrate" descr="The substrate on which the specimen was collected. Mostly used for lichen and bryophyte specimens." ex="On basalt, trunk of oak" obs="Darwin Core lumps this information into habitat." >}}

{{< dwc-term id="associatedTaxa" verbatim="Associated Taxa" descr="A list of the names of other species occurring with the collected specimen." ex="Quercus, Arctostaphylos, Ceanothus, Rhus, Eriogonum, Salvia" dwc="associatedTaxa" >}}
* In MycoPortal, this is also the field where "host" information is stored. See [this comment for instructions](https://github.com/BioKIC/symbiota-docs/issues/36#issuecomment-1015733243).

{{< dwc-term id="verbatimAttributes" verbatim="Description" descr="A physical description of the specimen at the time of collection. This often includes information that can be lost or difficult to observe after the collection and preservation process." ex="Shrub 3 m tall, corolla yellow" >}}

{{< dwc-term id="occurrenceRemarks" verbatim="Notes" descr="Any additional notes regarding the specimen." dwc="occurrenceRemarks" >}}

{{< dwc-term id="dynamicProperties" verbatim="Dynamic Properties" descr="A list of additional measurements, facts, characteristics, or assertions about the specimen in a format that allows programmatic parsing of the data. See the Darwin Core link below for further details." ex="awnLengthInMeters=0.014, heightInMeters=1.5, relativeHumidity=28, airTemperatureInC=22" dwc="dynamicProperties" >}}

{{< dwc-term id="lifeStage" verbatim="Life Stage" descr="The age or stage of the organism at the time of collection/observation. Typically used for zoological collections." ex="larva, juvenile" dwc="lifeStage" >}}

{{< dwc-term id="sex" verbatim="Sex" descr="The biological sex of the occurrence." ex="female, male" dwc="sex" >}}

{{< dwc-term id="individualCount" verbatim="Individual Count" descr="The number of individuals represented by the occurrence" ex="2, 15" dwc="individualCount" >}}

{{< dwc-term id="samplingProtocol" verbatim="Sampling Protocol" descr="The names and references to methods used to collect or sample an occurrence" ex="UV light trap, mist net, Takats et al. 2001. Guidelines for Nocturnal Owl Monitoring in North America. Beaverhill Bird Observatory and Bird Studies Canada, Edmonton, Alberta. 32 pp., http://www.bsc-eoc.org/download/Owl.pdf" dwc="samplingProtocol" >}}

<a id="preparations"><b>Preparations:</b></a> Preparation or preservation method for a specimen. While no universal controlled vocabulary currently exists for this field, a practical example can be found <a href="https://github.com/tdwg/cd/issues/64#issuecomment-781653290" target="_blank" rel="noopener noreferrer">here</a>.<br>
Ex: in ethanol, skeleton, pressed and dried.<br>
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:preparations" target="_blank" rel="noopener noreferrer">preparations</a>.

{{< dwc-term id="reproductiveCondition" verbatim="Phenology (Reproductive Condition)" descr="The reproductive stage the specimen is in. Typically used for plant and fungal collections." ex="flower, fruit, sterile" dwc="reproductiveCondition" >}}

{{< dwc-term id="behavior" verbatim="Behavior" descr="The behavior exhibited by the organism/occurrence at the time of collection/observation." ex="flying, sitting on eggs" dwc="behavior" >}}

{{< dwc-term id="vitality" verbatim="Vitality" descr="An indication of whether the organism was alive or dead at the time of collection or observation." ex="live, dead" dwc="vitality" >}}

{{< dwc-term id="establishmentMeans" verbatim="Establishment Means" descr="The state of establishment at the time of collection." ex="cultivated, invasive, native" dwc="establishmentMeans" >}}

{{< dwc-term id="isCultivated" verbatim="Cultivated Checkbox" descr="Check when the organism was established with the aid of humans and would not be able to exist on their own. This true/false field enables the ability to filter non-native or naturalized species." obs="Not currently exported in DwC format.">}}

{{< dwc-term id="typeStatus" verbatim="Type Status" descr="The type designation of a specimen, if it is a type specimen" ex="HOLOTYPE, ISOTYPE, PARATYPE" dwc="typeStatus" >}}

{{< dwc-term id="disposition" verbatim="Disposition" descr="The location or status of the physical specimen." ex="missing, on loan, in collection" dwc="disposition" >}}

{{< dwc-term id="occurrenceid" verbatim="Occurrence ID" descr="This is the Global Unique Identification (GUID) for the specimen. This identification code should be stable and uniquely identify the specimen relative to all other specimens within the world. If your collection is set to have occurrenceIDs/GUIDs generated by the portal (this is the suggested setting for all live-managed collections), this field will appear blank in the occurrence editor form. To view the occurrenceID value associated with your specimen, click the Public Display link at the top of the page." ex="000866d2-c177-4648-a200-ead4007051b9, urn:catalog:UWBM:Bird:89776" dwc="occurrenceID" >}}

{{< dwc-term id="fieldnumber" verbatim="Field Number" descr="An identifier given to the collecting event in the field. This number often serves as a link between the event indicated in the field notes and the specimen record." ex="2024-04-05-00045, JOSHUATREE_35" dwc="fieldNumber" >}}

{{< dwc-term id="language" verbatim="Language" descr="The language of the label information" ex="English, Spanish, Portuguese" dwc="language" >}}

{{< dwc-term id="labelproject" verbatim="Label Project" descr="Used for printing labels. You can create a label project and print that set of labels after you've entered the data." ex="Plants of Sedona 2012" >}}

{{< dwc-term id="duplicatequantity" verbatim="Duplicate Quantity" descr="The number of duplicate specimens created. This will dictate the number of labels printed for specimen." ex="10" >}}

{{< dwc-term id="institutionCode" verbatim="Institution Code" descr="The acronym of the institution that stewards this occurrence. Only enter a value if the institution is different than what was entered when the metadata for the institution was added to the portal." ex="NMNH, FLMNH" dwc="institutionCode" >}}

{{< dwc-term id="collectionCode" verbatim="Collection Code" descr="The acronym of the collection that stewards this occurrence. Only enter a value if the collection is different than what was entered when the metadata for the collection was added to the portal." ex="Herps, F" dwc="collectionCode" >}}

{{< dwc-term id="ownerInstitutionCode" verbatim="Owner Code" descr="The name (or acronym) in use by the institution having ownership of the object(s) or information referred to in the record." ex="NPS" dwc="ownerInstitutionCode" >}}

{{< dwc-term id="basisOfRecord" verbatim="Basis of Record" descr="The type of record the specimen is classified as. For physical collections, this field defaults to “PreservedSpecimen” (aka herbarium specimen) and for observation projects, the default is “Observation”." ex="PreservedSpecimen, LivingSpecimen, Observation" dwc="basisOfRecord" >}}

{{< dwc-term id="processingStatus" verbatim="Processing Status" descr="The status of the digital record. This field is used for internal data management and review. The values used are dictated by the specific workflow of each institution." >}}

{{< dwc-term id="dataGeneralizations" verbatim="Data Generalizations" descr="Internal notes associated with the occurrence record. Data entered in this field is not visible to the public and is not downloaded in a Darwin Core Archive." >}}


### Material Sample Fields

| ![Material Sample Module](/symbiota-docs/images/materialsampleblank.png) |
|:--:|
| Material Sample tab |

{{< notice note >}}
  Controlled vocabularies for Material Sample data fields are managed per portal, and the suggested examples provided below are derived from vocabularies used for the [NEON Biorepository](https://biorepo.neonscience.org/portal/). These vocabularies vary by portal, and modifications may require community input. Contact your Portal Administrator for more information.
{{</ notice >}}

{{< dwc-term id="sampleType" verbatim="Sample Type" descr="Controlled vocabulary defining the sample type, which is often anatomical in nature." ex="skull, liver, gastrointestinal tract, ectoparasite" dwc="" >}}

{{< dwc-term id="catalogNumber" verbatim="Catalog Number / Barcode" descr="A unique identifier for the material sample, analagous to _catalogNumber_ for specimen occurrences." ex="WIS-L-0123456, ASU0012345" dwc="catalogNumber" >}}

{{< dwc-term id="matSampleID" verbatim="Material Sample ID (GUID)" descr="A globally unique identifier for the material sample. In the absence of a persistent global unique identifier, construct one from a combination of identifiers in the record that will make this identifier globally unique." ex="06809dc5-f143-459a-be1a-6f03e63fc083" dwc="materialSampleID" >}}

{{< dwc-term id="sampleCondition" verbatim="Condition" descr="Free text field to describe the physical condition of the sample. Use of a controlled vocabulary is recommended but not forced." ex="very poor, poor, fair, good, unknown" dwc="" >}}

{{< dwc-term id="disposition" verbatim="Disposition" descr="Controlled vocabulary describing the current state of a sample with respect to its collection." ex="in collection, being processed, consumed, on loan" dwc="disposition" >}}

{{< dwc-term id="preservationType" verbatim="Preservation type" descr="Controlled vocabulary defining the physical storage/preservation method of a sample." ex="dry, ethanol, frozen, pinned" dwc="" >}}

{{< dwc-term id="preparationDate" verbatim="Preparation date" descr="The date of a sample's physical preparation. Dates in this field visually conform to MM/DD/YYYY formatting. Manual data entry into this field is validated using a calendar form." ex="08/01/2022" dwc="" >}}

{{< dwc-term id="preparedByUid" verbatim="Prepared by" descr="Name of the individual who prepared a sample. The individual must have an user account in the portal to be recorded in this field." ex="Liao, Rosie; Johnston, Andrew" dwc="" >}}

{{< dwc-term id="preparationDetails" verbatim="Preparation details" descr="Free text field to record notes providing more context about the physical preparation and condition of the sample." ex="upper and lower GI tract; kidney, left, whole; prepared with borax" dwc="" >}}

{{< dwc-term id="individualCount" verbatim="Individual count" descr="The number of loanable objects associated with the sample, i.e. all pieces of the sample assigned to the same unique materialSampleID (see above)." ex="0, 1, 100" dwc="individualCount" >}}

{{< dwc-term id="sampleSize" verbatim="Sample Size" descr="Free text field to quantify the sample beyond counted number of objects, e.g. dry weight." ex="200 uL" dwc="" >}}

{{< dwc-term id="storageLocation" verbatim="Storage Location" descr="Free text field to describe a sample's permanent physical storage location." ex="Freezer 3; Oversize Storage; Cab011, Dwr002" dwc="" >}}

{{< dwc-term id="remarks" verbatim="Remarks" descr="Free text field to provide additional notes, comments, and context unique to a sample that cannot be captured by other existing data fields. Limited to 250 characters." ex="genotype sampling; left jaw consumed in research; with post-cranial skeleton" dwc="" >}}

### Paleontology Fields

| ![Paleo Module](/symbiota-docs/images/paleo_module.png) |
|:--:|
| Paleo Module on the Occurrence Data tab |

{{< notice note >}}
  Controlled vocabularies for the following data fields are managed per portal. Modifications to these values may require community discussion. Contact your Portal Administrator for more information.
{{</ notice >}}

<a id="eon"><b>Eon:</b></a> The longest geologic time intervals.
Ex: Archean, Proterozoic, Phanerozoic
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:earliestEonOrLowestEonothem" target="_blank" rel="noopener noreferrer">earliestEonOrLowestEonothem</a>, <a href="https://dwc.tdwg.org/terms/#dwc:latestEonOrHighestEonothem" target="_blank" rel="noopener noreferrer">latestEonOrHighestEonothem</a>

<a id="era"><b>Era:</b></a> A subdivision of an eon that is a shorter interval of geologic time.<br>
Ex: Paleozoic, Mesozoic, Cenozoic.<br>
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:earliestEraOrLowestErathem" target="_blank" rel="noopener noreferrer">earliestEraOrLowestErathem</a>, <a href="https://dwc.tdwg.org/terms/#dwc:latestEraOrHighestErathem" target="_blank" rel="noopener noreferrer">latestEraOrHighestErathem</a>

<a id="period"><b>Period:</b></a> A subdivision of an era that is a shorter interval of geologic time.<br>
Ex: Ordovician, Silurian, Devonian, Carboniferous, Mississippian, Pennsylvanian, Permian, Triassic, Jurassic, Cretaceous, Paleogene, Neogene, Quaternary.<br>
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:earliestPeriodOrLowestSystem" target="_blank" rel="noopener noreferrer">earliestPeriodOrLowestSystem</a>, <a href="https://dwc.tdwg.org/terms/#dwc:latestPeriodOrHighestSystem" target="_blank" rel="noopener noreferrer">latestPeriodOrHighestSystem</a>

<a id="epoch"><b>Epoch:</b></a> A subdivision of a period that is a shorter interval of geologic time.<br>
Ex: Lower, Middle, Upper Ordovician; Wenlock; Pridoli; Lower, Middle, Upper Devonian; Lower, Middle, Upper Mississippian; Lower, Middle, Upper Pennsylvanian; Cisuralian; Lower, Middle, Upper Jurassic; Lower, Upper Cretaceous; Paleocene; Eocene; Oligocene; Miocene; Pliocene; Pleistocene; Holocene.<br>
The Epoch field is currently being recorded using Series, the chronostratigraphic units.<br>
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:earliestEpochOrLowestSeries" target="_blank" rel="noopener noreferrer">earliestEpochOrLowestSeries</a>, <a href="https://dwc.tdwg.org/terms/#dwc:latestEpochOrHighestSeries" target="_blank" rel="noopener noreferrer">latestEpochOrHighestSeries</a>

<a id="stage"><b>Stage:</b></a> The chronostratigraphic term given to the succession of rock strata laid down in a single geochronologic age.<br>
Ex: Lochkovian, Emsian, Eifelian, Givetian, Frasnian, Tournaisian, Serpukhovian, Moscovian, Changhsingian, Norian, Oxfordian, Hauterivian, Albian, Maastrichtian, Thanetian, Messinian, etc.<br>
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:earliestAgeOrLowestStage" target="_blank" rel="noopener noreferrer">earliestAgeOrLowestStage</a>, <a href="https://dwc.tdwg.org/terms/#dwc:latestAgeOrHighestStage" target="_blank" rel="noopener noreferrer">latestAgeOrHighestStage</a>

{{< dwc-term id="localStage" verbatim="Local Stage" descr="A local name for a stage that was applied to this specimen." ex="Ulatsian, Helvetian." >}}

{{< dwc-term id="earlyInterval" verbatim="Early Interval" descr="Name of the earliest possible geochronologic eon, era, period, epoch or age, or the lowest chronostratigraphic eonothem, erathem, system, series, or stage attributable to the stratigraphic horizon from which the cataloged specimen was collected." ex="Aalenian, Aeronian, Albian, Anisian, Aptian, Aquitanian, Archean, Artinskian, Asselian, Bajocian, Barremian, Bartonian, etc." >}}

{{< dwc-term id="lateInterval" verbatim="Late Interval" descr="Name of the latest possible geochronologic eon, era, period, epoch or age, or the highest chronostratigraphic eonothem, erathem, system, series or stage attributable to the stratigraphic horizon from which the cataloged specimen was collected." ex="Aalenian, Aeronian, Albian, Anisian, Aptian, Aquitanian, Archean, Artinskian, Asselian, Bajocian, Barremian, Bartonian, etc." >}}

{{< dwc-term id="absoluteAge" verbatim="Absolute Age" descr="Field to record the age of specimen/rock in years determined using radioactive decay of isotopes (Carbon-14, argon-argon, potassium-argon, uranium-lead, etc.) and other quantitative dating methods." ex="20 Ma, 75 ka, 10.5 – 12.7 +/- 0.5 Ma, etc." >}}

{{< dwc-term id="storageAge" verbatim="Storage Age" descr="Field for institutions that arrange collections by geologic time or biostratigraphy. The physical location of a specimen within the collection space." ex="Miocene, Wasatchian, Paleocene, Bridgerian, etc." >}}

{{< dwc-term id="biota" verbatim="Biota (Flora/Fauna)" descr="Name given to collections of fossils of the same age from a single locality or multiple localities within a specific geographic area." ex="Chalk Bluffs, Stewart Valley, Bridge Creek, Mazon Creek, etc." >}}

<a id="biostratigraphy"><b>Biostratigraphy (Biozone):</b></a> The name of the lowest possible geological biostratigraphic zone of the stratigraphic horizon from which the cataloged item was collected.<br>
Ex: “Wa0”, “Uvigerinella sparsicostata Zone”, “Ogygiocaris”<br>
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:lowestBiostratigraphicZone" target="_blank" rel="noopener noreferrer">lowestBiostratigraphicZone</a>, <a href="https://dwc.tdwg.org/terms/#dwc:highestBiostratigraphicZone" target="_blank" rel="noopener noreferrer">highestBiostratigraphicZone</a>

<a id="group"><b>Group:</b></a> The name of the lithostratigraphic group from which the cataloged specimen was collected. The <a href="https://ngmdb.usgs.gov/Geolex/search" target="_blank" rel="noopener noreferrer">National Geologic Map Database Geolex Search</a> is a great resource for the named lithostratigraphic units accepted by the USGS.<br>
Ex: Bathurst, Lower Wealden, Monte Cristo, Contra Costa, Panoche, etc.<br>
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:group" target="_blank" rel="noopener noreferrer">group</a>

<a id="formation"><b>Formation:</b></a> The name of the lithostratigraphic formation from which the cataloged specimen was collected. The <a href="https://ngmdb.usgs.gov/Geolex/search" target="_blank" rel="noopener noreferrer">National Geologic Map Database Geolex Search</a> is a great resource for the named lithostratigraphic units accepted by the USGS.<br>
Ex: Notch Peak, House Limestone, Fillmore, Chinle, etc.<br>
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:formation" target="_blank" rel="noopener noreferrer">formation</a>

<a id="member"><b>Member:</b></a> The name of the lithostratigraphic member from which the cataloged item was collected. The <a href="https://ngmdb.usgs.gov/Geolex/search" target="_blank" rel="noopener noreferrer">National Geologic Map Database Geolex Search</a> is a great resource for the named lithostratigraphic units accepted by the USGS.<br>
Ex: Lava Dam, Hellnmaria, Brown Mountain Sandstone<br>
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:member" target="_blank" rel="noopener noreferrer">member</a>

<a id="bed"><b>Bed:</b></a> The name of the lithostratigraphic bed from which the cataloged item was collected. The <a href="https://ngmdb.usgs.gov/Geolex/search" target="_blank" rel="noopener noreferrer">National Geologic Map Database Geolex Search</a> is a great resource for the named lithostratigraphic units accepted by the USGS.<br>
Ex: Harlem coal<br>
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:bed" target="_blank" rel="noopener noreferrer">bed</a>

{{< dwc-term id="taxonEnvironment" verbatim="Taxon Environment" descr="The depositional environment of the rock unit from which cataloged specimen was collected." ex="marine, lacustrine, non-marine, marine-non-marine" >}}

{{< dwc-term id="lithology" verbatim="Lithology" descr="Field for terms to describe the types of rock/sediment from which the cataloged specimen was collected." ex="sandstone, mudstone, siltstone, shale, etc." dwc="lithostratigraphicTerms" >}}

{{< dwc-term id="stratRemarks" verbatim="Strat Remarks" descr="Field to record additional details about the geology, stratigraphy, more detailed lithology description, palynological sampling info, core data, etc." >}}

{{< dwc-term id="element" verbatim="Element" descr="Field to record type of plant organ cataloged specimen represents." ex="stem, strobilus, sterile leaf, fertile leaf, pinnule(s), rooting organ, rootlet, megasporangium, sporangium, spore, sterile axis, fertile axis, root, etc." >}}

{{< dwc-term id="slideProperties" verbatim="Slide Properties" descr="Field to record types of prepared slides of specimens, noting the type of preparation and mounting medium, and to provide England Finder coordinates for palynomorph slides." ex="strewn, petrographic thin-section, mounted peel" >}}

{{< dwc-term id="geologicalContextID" verbatim="Geological Context ID" descr="An identifier for the set of information associated with a GeologicalContext (the location within a geological context, such as stratigraphy). May be a global unique identifier or an identifier specific to the data set." ex="https://opencontext.org/subjects/e54377f7-4452-4315-b676-40679b10c4d9" dwc="geologicalContextID" >}}
