---
title: "Importando y Subiendo Datos"
date: 2021-10-07
authors: ["Ed Gilbert"]
editors: ["Katie Pearson"]
translators: ["Katie Pearson"]
weight: 150
keywords: ["subir datos","importar datos","subir archivos","IPT"]
---

{{< notice note >}}
  Esta página provee instrucciones para subir datos en una colección existente dentro de un portal Symbiota. Contacte al administrador de su portal si aún no cuenta con una colección en el portal Symbiota deseado.
{{</ notice >}}

## Iniciar la Carga de Datos

1. Navegue al Panel de Control de Administración (Mi Perfil > Manejo de Ocurrencias > nombre de su colección).
2. Haga click en Importar/Actualizar Registros de Especímenes, luego seleccione "Crear un nuevo Perfil de Importación".
3. Crear un título para su perfil de carga en el campo Título.
4. Seleccione el Tipo de Carga deseado en el menú desplegable.
    * **Carga Manual de Archivo Darwin Core:** Use este tipo de carga si los datos que desea subir están en el formato de un [Archivo Darwin Core](http://en.wikipedia.org/wiki/Darwin_Core_Archive). Un Archivo Darwin Core (DwC-A) es un estándar de datos usado comúnmente para almacenar datos de ocurrencias de especies en un sólo conjunto de datos autónomo. Un DwC-A incluye metadatos, un archivo de ocurrencia de datos y, a menudo, archivos con determinaciones de especies (identificaciones) e imágenes.
    * **Recurso IPT / Proveedor de Archivo Darwin Core:** Use este tipo de carga si va a proveer una URL de un Archivo Darwin Core existente y ya publicado en la web, como los que son provistos por medio de una IPT.
    * **Carga de Archivos:** Use este tipo de carga si va a proveer un archivo separado por comas (CSV) o un archivo separado por tabulaciones (TSV) que contiene TODOS los campos de sus datos de ocurrencia. Puede convertir un documento de Excel en un archivo CSV haciendo click en Guardar Como, y luego seleccionando texto delimitado por comas (CSV) en los tipos de archivo. Notar que, si los datos existen en el portal para cualquiera de las ocurrencias que está cargando, esos datos serán sobreescritos por los datos que está subiendo. Para subir registros parciales, use una Carga de Archivos Esqueléticos.
    * **Carga de Archivos Esqueléticos:** Use este tipo de carga si va a proveer un archivo CSV o TSV conteniendo datos de sólo unos campos (e.g., georreferencias o algunos otros datos auxiliares). Notar que cualquier dato provisto en un archivo esquelético NO va a sobreescribir datos existentes en la base de datos, así que cualquier dato preexistente en los campos deseados deberá ser eliminado si desea reemplazarlos con los datos del archivo esquelético.
    * **Carga de Archivo de NfN:** Use este tipo de carga si va a proveer un archivo CSV producido a partir de Notes from Nature.
    * **Mapeo Directo de Base de Datos:**
    * **Procedimiento Almacenado:** Use esta opción si está transfiriendo desde una fuente de esquema a una base de datos Symbiota localizada en el mismo servidor de la base de datos MySQL.
    * **Carga de Script:** Use esta opción si está transfiriendo información desde una fuente MySQL a una base de datos Symbiota que está localizada en un servidor distinto.

5. Siga las siguientes indicaciones de acuerdo con el tipo de carga seleccionado.

### Carga Manual de Archivo Darwin Core
[¡Contribuya con esta sección!](https://biokic.github.io/symbiota-docs/es/contribute/)

### Recurso IPT / Proveedor de Archivo Darwin Core
[¡Contribuya con esta sección!](https://biokic.github.io/symbiota-docs/es/contribute/)

### Carga de Archivos o Carga de Archivos Esqueléticos 
1. Si usted o el administrador de su portal ha creado un Procedimiento Almacenado con limpieza de datos u otras revisiones, introduzca el nombre del procedimiento almacenado en el campo provisto. De otra manera, ignore este paso.
2. Haga click en el botón Crear Perfil. 
3. En la siguiente página, verá una lissta de los perfiles de carga existentes. Seleccione el perfil que desee usar (el que creó) y haga click en Iniciar Carga.
    * Para editar su perfil de carga en el futuro, puede hacer click en el ícono de lápiz en esta página.
4. Haga click en el botón de Elegir Archivo y navegue al archivo que desea subir en su Administrador de Archivos o ventana de Búsqueda. Seleccione el campo y haga click en Abrir.
5. Haga click en el botón Analizar Archivo.
6. Si la colección a la que está subiendo los datos es de manejo en vivo (el portal es su sistema de manejo de datos), proceda al paso 7. Si la colección a la que desea subir datos es un “snapshot” o una base de datos de especímenes manejada en la institución base, seleccione la llave primaria para la fuente del registro del espécime del menú desplegable. La llave primaria es un campo requerido para conjuntos de datos que servirán como el identificador primario del registro (el enlace permanente entre la base de datos original y el registro en el portal). Este campo debe estar completo para cada registro, con valores únicos. Estos valores también deben ser estables y no deben cambiar en la base de datos central con el tiempo. Las colecciones snapshot típicamente utilizarán el número de catálogo (número de acceso), código de barras, o la llave primaria de la base de datos original para este campo. 
7. Ahora verá un apágina que se verá similar a la mostrada abajo. La longitud y contenido de los campos Campos de Origen/Campos Objetivo de la tabla dependeràn de qué columnas fueron incluidas en el archivo CSV original.

![Ejemplo del Módulo de Carga de Datos](/symbiota-docs/images/DataUploadModule.png)

8. Select which fields in your CSV file (**Source Fields**) will correspond to which fields in the Symbiota portal (**Target Fields**). Check the [Symbiota Data Field Guide](http://symbiota.org/docs/symbiota-occurrence-data-fields-2/) for definitions of each data field. Also see the **Uploading Tips** section below.
9. Once you are satisfied with your field-to-field mapping (see next Notes), click the “Save Mapping” button.
10. Select whether you would like the script to match the data in your file to existing data in the portal based on Catalog Number or Other Catalog Numbers. You will only need to do this if you are adding data to records that already exist in the portal. Otherwise, leave these unchecked.
11. Select the Processing Status that you would like to apply to all your uploaded records (if desired) by selecting an option from the dropdown menu.
12. Click the Start Upload button. This will upload your data into a *temporary* table so you can review it before committing the final upload.
13. Verify that the correct number of records are being updated and/or added by viewing the Pending Data Transport Report on the next page.

![Screenshot of Pending Data Transfer Report](/symbiota-docs/images/PendingDataTransport.png)

14. View the data that have been stored in the temporary table to ensure correct mapping and formatting of the fields you are uploading. You can either:
    * Click the small box icon to the right of "Records to be updated" or "New records" to view the records in a table in your browser.
    * Click the multiple file icon to the right of the box icon to download a CSV file of the records to be updated or new records.
15. If anything is incorrect, fix your CSV file and re-upload it according to the steps you followed above, or return to your field mapping and fix the field mapping. If everything looks good, click the Transfer Records to Central Specimen Table button. **Note that this step is final and is not possible to undo!**

### Procedimiento Almacenado

1. Write a stored procedure used to transfer records (the collection cleanup scripts can be put in central stored procedure or kept separate)
2. Set up the script to run as a regular cronjob.

### Carga de Script

1. Write a stored procedure used to transfer records. A sample Linux script is located here: [SampleSystemUpload.sh](https://symbiota.org/wp-content/uploads/SampleSystemUpload.sh). The cleanup scripts can be put in central stored procedure or kept separate.
2. Set up the script to run as a regular cronjob.

## Consejos para Subir Datos

{{< notice tip >}}
  Una lista de campos que pueden ser importados a un portal de datos Symbiota puede ser [encontrado aquí](https://biokic.github.io/symbiota-docs/es/coll_manager/upload/fields/).
{{</ notice >}}

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
