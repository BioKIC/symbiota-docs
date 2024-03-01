---
title: "Campos de Datos en Symbiota"
date: 2014-07-21
lastmod: 2024-03-01
draft: false
authors: ["Ed Gilbert"]
editors: ["Laura Rocha Prado","Katie Pearson, Lindsay Walker"]
translators: ["Samanta Orellana"]
keywords: ["editar","campos","campos de datos", "términos", "términos dwc"]
---

El esquema de datos Symbiota está fuertemente alineado con el del estándar de intecambio de datos <a href="https://www.tdwg.org/standards/dwc/" target="_blank" rel="noopener noreferrer">Darwin Core</a>. Para más detalles, enlaces a las definiciones Darwin Core definitions son proporcionadas para cada término. Aprenda más acerca de los términos Darwin Core en las siguientes páginas de TDWG:
- [TDWG - Darwin Core quick reference guide](https://dwc.tdwg.org/terms/)
- [TDWG - List of Darwin Core terms](https://dwc.tdwg.org/list)

{{< notice note >}}
  Ya que los portales tienen la habilidad de personalizar los nombres de los campos de sus formularios de ingreso de datos, los nombres de los campos pueden diferir de los encontrados en las definiciones de los campos centrales y cómo están mapeados a las herramientas de exportación de Darwin Core.
{{</ notice >}}

{{< button href="../../../documents/SymbiotaDataFields_202111.csv" text="Descargar contenido completo como un archivo CSV" >}}
{{< button href="https://github.com/BioKIC/symbiota-docs/blob/master/static/documents/SymbiotaDataFields_202111.csv" text="Ver contenido completo como un archivo CSV" >}}


### Standard Fields

{{< dwc-term id="catalogNumber" verbatim="Número de Catálogo" descr="El identificador único (clave primaria) para el registro del espécimen. Este campo deberís ser usado para almacenar códigos de barra o número de acceso (herbarios). Se requiere que este campo sea de carácter único por colección" ex="WIS-L-0123456, ASU0012345, 12345" dwc="catalogNumber" >}}

{{< dwc-term id="otherCatalogNumbers" verbatim="Otros Números de Catálogo" descr="Cualquier otro identificador del registro del espécimen que no es el número de catálogo. Este campo est típicamente usado para almacenar los números de catálogo antiguos de colecciones que están en el proceso de transferirse de un sistema de digitalización a otro (e.g. sistema de código de barras)." ex="12345" dwc="otherCatalogNumbers" >}}

{{< dwc-term id="recordedBy" verbatim="Colector" descr="El nombre de la persona que colectó el espécimen o hizo la observación." ex="C.G. Pringle, Goodding, L.N." dwc="recordedBy" >}}

{{< dwc-term id="associatedCollectors" verbatim="Colectores Asociados" descr="Otros colectores que estuvieron presentes durante la colecta." ex="John R. Reeder, A. Nelson" obs="Este campo no está definido por el estándar Darwin Core, que coloca colectores primarios y secundarios en el campo recordedBy." >}}

{{< dwc-term id="recordNumber" verbatim="Número" descr="El número de colecta asignado al espécimen por el colector." ex="1294, 12490b, 94-132" dwc="recordNumber" >}}

{{< dwc-term id="eventDate" verbatim="Fecha" descr="La fecha en la que el espécimen fue colectado. Mientras que las fechas pueden ser introducidas usando su formato preferido, el valor será convertido y almacenado con un formato numérico ISO-8601 (YYYY-MM-DD). Note que los meses y días desconocidos pueden ser añadidos como \"00\". Por ejemplo, una colecta con fecha \"Marzo 1956\" puede ser introducida como \"1956-03-00\"." ex="1983-09-15, 1983-07-00, 1934-00-00" dwc="eventDate" >}}

{{< dwc-term id="verbatimEventDate" verbatim="Fecha Literal" descr="Puede ser utilizado para registrar la fecha tal y como se encuentra en la etiqueta. Particularmente útil para formatos de fecha no estandarizados o rangos de fechas." ex="Primavera 1901, Marzo-Abril 1952, finales Sept. 1909" dwc="verbatimEventDate" >}}

{{< dwc-term id="year" verbatim="Año" descr="El valor numérico del año en el momento de la colecta. Este campo (junto con el mes y el día) es añadido automáticamente cuando la fecha es introducida." ex="1959" dwc="year" >}}

{{< dwc-term id="month" verbatim="Mes" descr="El valor numérico del mes en el momento de la colecta. Este campo (junto con el año y el día) es añadido automáticamente cuando la fecha es introducida." ex="10" dwc="month" >}}

{{< dwc-term id="day" verbatim="Día" descr="El valor numérico del día en el momento de la colecta. Este campo (junto con el año y el mes) es añadido automáticamente cuando la fecha es introducida." ex="28" dwc="day" >}}

<a id="dayRange"><b>Rango de día del año:</b></a> Un rango de fechas de colectas pueden ser representados aquí como valores numéricos de valores de días de año. Estos valores serán calculados automáticamente si introduce un rago en el campo de fecha literal (e.g. 12 Sept 1968 a 19 Sept 1968, 1968-09-12 a 1968-09-19) <br>
See Darwin Core's <a href="https://dwc.tdwg.org/terms/#dwc:startDayOfYear" target="_blank" rel="noopener noreferrer">startDayOfYear</a>, <a href="http://rs.tdwg.org/dwc/terms/index.htm#endDayOfYear" target="_blank" rel="noopener noreferrer">endDayOfYear</a>.

{{< dwc-term id="sciname" verbatim="Nombre Científico" descr="El nombre en latín del espécimen sin el autor. Puede ser cualquier nivel desde reino hasta subespecie o variedad, dependiendo del nivel de identificación." ex="Pinaceae, Pinus, Pinus edulis, Pinus edulis var. fallax" dwc="scientificName" >}}

{{< dwc-term id="scientificNameAuthorship" verbatim="Autor" descr="El nombre de la persona que nombró por primera vez el taxón. Este campo se llena automáticamente luego de introducir el nombre científico." ex="L., Asa A. Gray" dwc="scientificNameAuthorship" >}}

{{< dwc-term id="identificationQualifier" verbatim="Calificador de Identificación" descr="La expresión de incertidumbre del determinador en su identificación. Esto será encontrado en la etiqueta junto al nombre científico." ex="cf., aff." dwc="identificationQualifier" >}}

{{< dwc-term id="family" verbatim="Familia" descr="La familia a la cual pertenece el taxón. Este campo se rellena automáticamente al agregr el nombre científico." ex="Pinaceae" dwc="family" >}}

{{< dwc-term id="identifiedBy" verbatim="Identificado Por" descr="El nombre de la persona que identificó el espécimen. También llamado determinador." ex="L. R. Landrum" dwc="identifiedBy" >}}

{{< dwc-term id="dateIdentified" verbatim="Fecha de Identificación" descr="La fecha en la que fue realizada la identificación. La fecha puede ser ingresada en formato de texto libre y no necesita estar en formato estandarizado de fecha." ex="1992, May 1992, 2 May 1992" dwc="dateIdentified" >}}

{{< dwc-term id="identificationReferences" verbatim="Referencias de ID" descr="La referencia utilizada para realizar la identificación." ex="Nesom, Guy L. 2006. Flora of North America - Asteraceae. vol. 20" dwc="identificationReferences" >}}

{{< dwc-term id="identificationRemarks" verbatim="Comentarios de ID" descr="Cualquier comentario adicional relacionado con la identificación del espécimen." dwc="identificationRemarks" >}}

{{< dwc-term id="taxonRemarks" verbatim="Comentarios de Taxón" descr="Cualquier comentario adicional relacionado con el nombre científico bajo el cual el espécimen fue identificado." dwc="taxonRemarks" >}}

{{< dwc-term id="country" verbatim="País" descr="El nombre del país en el cual el espécimen fue colectado. Para asistir en la entrada de datos, un menú desplegable aparecerá al empezar a teclear las primeras letras, aunque nombres fuera del listado pueden ser incluidos." ex="USA, Canada, Mexico" dwc="country" >}}

{{< dwc-term id="stateProvince" verbatim="Estado/Provincia" descr="El nombre del estado o provincia en el que un espécimen fue colectado. Al empezar a teclear, un menú desplegable con una lista aparecerá para ciertos países." ex="New York, Arizona, Sonora" dwc="stateProvince" >}}

{{< dwc-term id="county" verbatim="Condado" descr="El nombre del condado en el cual el espécimen fue colectado. Elegir uno del menú desplegable si está en Estados Unidos. Para especímenes fuera de Estados Unidos, ingresar la siguiente región geográfica bajo estado/provincia." ex="Maricopa" dwc="county" >}}

{{< dwc-term id="municipality" verbatim="Municipalidad" descr="El nombre de la municipalidad en la cual el espécimen fue colectado. Para especímenes colectados fuera de Estados Unidos, introducir el cuarto nivel geográfico designado." ex="Paradise Valley" dwc="municipality" >}}

{{< dwc-term id="locality" verbatim="Localidad" descr="La localidad detallada en la cual el espécimen fue colectado." ex="9.5 miles NW of Sedona along Boynton Pass Rd." dwc="locality" >}}

{{< dwc-term id="locationID" verbatim="ID de Localidad" descr="Un identificador para la información de la localidad (datos asociados con dcterms:Location). Puede ser un identificador global único, o un identificador específico en el conjunto de datos." ex="https://opencontext.org/subjects/768A875F-E205-4D0B-DE55-BAB7598D0FD1" dwc="locationID" >}}

<a id="localitySecurity"><b>Seguridad de Localidad:</b></a> Al marcar la casilla de Seguridad de Localidad se ocultarán los detalles de localidad más abajo de condado para usuarios sin autorización. Esto es típicamente realizado para especies raras o amenazadas. Las imágenes también son ocultas para proteger detalles de localidad que pueden ser visibles en la etiqueta. Los usuarios que están conectados en el sistema y tienen los permisos necesarios para ver detalles de localidad (e.g. encargados de colecciones) continuarán teniendo acceso a los datos. Esta casilla será marcada automáticamente si el nombre de la especie está en un listado de especies raras &nbsp;(ver mapa del sitio). Si desea cambiar el estado de protección (activar o desactivar), haga click en la casilla Bloquear Seguridad (_Lock Security_) y/o introduzca una razón para sobreescribir la seguridad en el campo de texto. Dejar la seguridad de localidad desbloqueada permitirá aplicar la configuración programada por los administradores de especies sensibles, lo cual es la recomendación para la mayoría de registros. <br>
Para más información acerca de protección de especies sensibles, ver la página de <a href="https://biokic.github.io/symbiota-docs/user/redaction/">Protección de Especies Sensibles</a>. <br>
Este campo no está definido por el estándar Darwin Core.

{{< dwc-term id="decimalLatitude" verbatim="Latitud y Longitud (formato decimal)" descr="La latitud y longitud geográfica en grados decimales. La latitud del hemisferio sur y la longitud del hemisferio occidental (e.g. USA) deben ser ingresadas con valores negativos. Hacer click en el botón \"Herramientas\" para ingresar las coordenadas en grados, minutos, segundos (DMS) o en formatos UTM. Los grados decimales son el estandar preferido para las coordenadas según lo definido por  Darwin Core. Ver abajo para más información acerca del uso de esta herramienta." ex="34.874022, -111.75774" dwc="decimalLatitude" >}}

{{< dwc-term id="coordinateUncertaintyInMeters" verbatim="Incertidumbre (metros)" descr="La precisión de las coordenadas en metros (únicamente el valor numérico). Esto es medido como el radio del círculo en el cual el punto verdadero se encontraría de ser conocido. Si las coordenadas son obtenidas utilizando un GPS, entonces la presición sería el error encontrado en la unidad del GPS (usualmente cerca de 10m). Mientras que en los especímenes colectados previamente, los colectores usualmente no especifican la fuente de las coordenadas en la etiqueta (GPS, map, etc), es típicamente una buena suposición que las coordenadas tengan de uno a doscientos metros de presición. Si los detalles de la localidad son vagos como \"Gran Cañón\", entonces las coordenadas deberían ser el centroide entre una incertidumbre abarcando una mayor área donde el espécimen pudo ser colectado. Si la localidad es \"Cañón Boynton, Sedona\", la incertidumre sería alrededor de 1500 m. Este campo se auto rellena al utilizar GeoLocate para georreferenciar." ex="42000 para Phoenix, 20000 para Salt Lake City" dwc="coordinateUncertaintyInMeters" >}}

{{< dwc-term id="geodeticDatum" verbatim="Datum" descr="El sistema geográfico que fue utilizado para obtener las coordenadas. Este campo se auto rellena cuando se usa [http://www.museum.tulane.edu/geolocate/|GeoLocate] o la herramienta de Leaflet Maps para georreferenciar." ex="NAD27, NAD83, WGS84" dwc="geodeticDatum" >}}

<a id="verbatimCoordinates"><b>Coordenadas Literales:</b></a> Si las coordenadas registradas en la etiqueta del espécimen se encuentran un formato distinto a grados decimales, introducirlas aquí. Cuando los campos de lat/long decimal están en blanco y se introducen UTM o DMS usando uno de los formatos desplegados en el ejemplo de abajo, los valores de lat/long decimales serán generados automáticamente. Hacer click en el símbolo "&lt;&lt;" par reemplazar los valores decimales existentes. Este campo se auto rellena cuando se utilizan las herramientas de georreferenciación de DMS, UTM y TRS.<br>
Ex: 34° 13.940' N 112° 2.370' W, 34d 13m 12.940s N 112d 20m 46.370s W, 12 420944E 4064025N, TRS: T40N R32E S29 <br>
Ver Darwin Core en <a href="https://dwc.tdwg.org/terms/#dwc:verbatimCoordinates" target="_blank" rel="noopener noreferrer">verbatimCoordinates</a>.

{{< dwc-term id="minimumElevationInMeters" verbatim="Elevación en Metros" descr="La elevación en metros en la cual el espécimen fue colectado. También llamado altitud. Usar únicamente el campo de la izquierda, dejando el campo a la derecha en blanco cuando un sólo valor de elevación exista." ex="1400, 2000-2200" dwc="minimumElevationInMeters" >}}

<a id="verbatimElevation"><b>Elevación Literal:</b></a> La elevación literal a la cual el espécimen fue colectado. Esto es utilizado típicamente para registrar una medida de elevación que fue medida en pies o una designación de incertidumbre. Cuando el campo de elevación en metros es dejado en blanco, el valor será convertido automáticamente en metros. Haga click en el símbolo "&lt;&lt;" para reemplazar los valores en metros ingresados previamente.<br>
Ex: 4500ft, 4500 feet, ca 4500', ca 2000m, 4500' +-300'<br>
Ver Darwin Core <a href="https://dwc.tdwg.org/terms/#dwc:verbatimElevation" target="_blank" rel="noopener noreferrer">verbatimElevation</a>.

<a id="minimumDepthInMeters"><b>Profundidad en Metros:</b></a> El rango de profundidad bajo la superficie local, en metros.<br>
Ex: 100, 150-200<br>
Ver Darwin Core <a href="http://rs.tdwg.org/dwc/terms/minimumDepthInMeters" target="_blank" rel="noopener noreferrer">minimumDepthInMeters</a>, <a href="https://dwc.tdwg.org/terms/#dwc:maximumDepthInMeters" target="_blank" rel="noopener noreferrer">maximumDepthInMeters</a>.

{{< dwc-term id="verbatimDepth" verbatim="Profundidad Literal" descr="La descripción original de profundidad bajo la superficie local en la cual el espécimen fue colectado." ex="100ft, 100 feet, ca 100', ca 30m, 100' +-10'" dwc="verbatimDepth" >}}

{{< dwc-term id="georeferencedBy" verbatim="Georreferenciado Por" descr="El nombre de la persona que georreferenció el registro del espécimen. Este campo se rellena automáticamente cuando se utiliza GeoLocate para georreferenciar y la información ya ha sido ingresada." ex="A. Gonzales, emakings, acbarber" dwc="georeferencedBy" >}}

{{< dwc-term id="georeferenceProtocol" verbatim="Protocolo de Georreferenciación" descr="La fuente de los estándares utilizados para georreferenciar." ex="Georeferencing Quick Guide. Zermoglio et al. 2020" dwc="georeferenceProtocol" >}}

{{< dwc-term id="georeferenceSources" verbatim="Fuentes de Georreferenciación" descr="La herramienta o herramientas utilizadas para georreferenciar." ex="GeoLocate, Google Earth, USGS map" dwc="georeferenceSources" >}}

{{< dwc-term id="georeferenceVerificationStatus" verbatim="Estado de Verificación de Georreferenciación" descr="Indica si la georreferencia ha sido revisada o verificada." ex="revisada, no revisada" dwc="georeferenceVerificationStatus" >}}

{{< dwc-term id="georeferenceRemarks" verbatim="Comentarios de Georreferencia" descr="Cualquier comentario adicional relacionado a la georreferenciación del espécimen." dwc="georeferenceRemarks" >}}

{{< dwc-term id="habitat" verbatim="Hábitat" descr="La descripción del hábitat en el cual el espécimen fue colectado." ex="Humedales a lo largo de un pequeño arroyo en un chaparral." dwc="habitat" >}}

{{< dwc-term id="substrate" verbatim="Sustrato" descr="El sustrado en el cual el espécimen fue colectado. Mayormente utilizado en colecciones de líquenes y briofitas." ex="En basalto, tronco de encino" obs="Darwin Core lumps this information into habitat." >}}

{{< dwc-term id="associatedTaxa" verbatim="Taxa Asociados" descr="Una lista de los nombres de otras especies que ocurren con el espécimen colectado." ex="Quercus, Arctostaphylos, Ceanothus, Rhus, Eriogonum, Salvia" dwc="associatedTaxa" >}}
* En MycoPortal, también es el campo donde se almacena la información de "hospedero". See [this comment for instructions](https://github.com/BioKIC/symbiota-docs/issues/36#issuecomment-1015733243).

{{< dwc-term id="verbatimAttributes" verbatim="Descripción" descr="Una descripción física del espécimen en el tiempo de la colección. Este a menudo incluye información que puede ser perdida o es difícil de observar luego del proceso de colecta y preservación." ex="Arbusto de 3 m alto, corola amarilla" >}}

{{< dwc-term id="occurrenceRemarks" verbatim="Notas" descr="Cualquier comentario adicional relacionado con el espécimen." dwc="occurrenceRemarks" >}}

{{< dwc-term id="dynamicProperties" verbatim="Propiedades Dinámicas" descr="Una lista de medidas adicionales, hechos, características o aserciones acerca del espécimen en un formato que permite un análisis programático de los datos. Ver el enlace a Darwin Core de abajo para más detalles." ex="awnLengthInMeters=0.014, heightInMeters=1.5, relativeHumidity=28, airTemperatureInC=22" dwc="dynamicProperties" >}}

{{< dwc-term id="lifeStage" verbatim="Etapa de Vida" descr="La edad o etapa del organismo en el momento de la colecta/observación. Típicamente utilizado en colecciones zoológicas." ex="larva, juvenil" dwc="lifeStage" >}}

{{< dwc-term id="sex" verbatim="Sexo" descr="El sexo biológico de la ocurrencia." ex="hembra, macho" dwc="sex" >}}

{{< dwc-term id="individualCount" verbatim="Conteo Individual" descr="El número de individuos representados en la ocurrencia" ex="2, 15" dwc="individualCount" >}}

{{< dwc-term id="samplingProtocol" verbatim="Protocolo de Muestreo" descr="Los nombres y referencias de los métodos utilizados para colectar o muestrar una ocurrencia." ex="trampa de luz UV, red de niebla, Takats et al. 2001. Guidelines for Nocturnal Owl Monitoring in North America. Beaverhill Bird Observatory and Bird Studies Canada, Edmonton, Alberta. 32 pp., http://www.bsc-eoc.org/download/Owl.pdf" dwc="samplingProtocol" >}}

{{< dwc-term id="preparations" verbatim="Preparaciones" descr="Método de preparación o preservación para un espécimen." ex="en etanol, esqueleto" dwc="preparations" >}}

{{< dwc-term id="reproductiveCondition" verbatim="Fenología (Condición Reproductiva)" descr="La etapa reproductiva en la cual se encuentra el espécimen. Típicamente utilizado para colecciones botánicas y micológicas." ex="flor, fruto, estéril" dwc="reproductiveCondition" >}}

{{< dwc-term id="establishmentMeans" verbatim="Medio de Establecimiento" descr="El estado del establecimiento al tiempo de la colecta." ex="cultivado, invasivo, native" dwc="establishmentMeans" >}}

{{< dwc-term id="isCultivated" verbatim="Cultivado" descr="Marcar cuando el organismo haya sido establecido con ayuda de humanos y que no sea capaz de existir por su cuenta. Este es un campo de verdadero/falso que permite filtrar las especies no nativas o naturalizadas." obs="Not currently exported in DwC format.">}}

{{< dwc-term id="typeStatus" verbatim="Estado de Tipo" descr="La designación del tipo de un espécimen, si es un espécimen tipo" ex="HOLOTYPE, ISOTYPE, PARATYPE" dwc="typeStatus" >}}

{{< dwc-term id="disposition" verbatim="Disposición" descr="La ubicación o estado físico del espécimen." ex="missing, on loan, cone collection" dwc="disposition" >}}

{{< dwc-term id="occurrenceID" verbatim="ID de Ocurrencia" descr="Este es el Identificador Global Único (GUID) para el espécimen. Este identificaor debe ser estable e identificar de forma única al espécimen con respecto de todos los otros especímenes en el mundo." ex="000866d2-c177-4648-a200-ead4007051b9, urn:catalog:UWBM:Bird:89776" dwc="occurrenceID" >}}

{{< dwc-term id="fieldNumber" verbatim="Field Number" dwc="fieldNumber" >}}

{{< dwc-term id="ownerInstitutionCode" verbatim="Código de Propietario" descr="El acrónimo de la institución propietaria. Únicamente introducir un valor si la institución propietaria es dirferente a la que está ingresada en los metadatos de la colección añadida en el portal." ex="NPS, Forest Service" dwc="ownerInstitutionCode" >}}

{{< dwc-term id="basisOfRecord" verbatim="Base del Registro" descr="El tipo de registro en el cual está clasificado el espécimen. Para colecciones físicas, este campo es rellenado automáticamente como “PreservedSpecimen” y para proyectos de observación, el valor automático es “Observation”." ex="PreservedSpecimen, LivingSpecimen, Observation" dwc="basisOfRecord" >}}

{{< dwc-term id="language" verbatim="Idioma" descr="El idioma de la información en la etiqueta" ex="English, Spanish, Portuguese" dwc="language" >}}

{{< dwc-term id="processingStatus" verbatim="Estado de Procesamiento" descr="El estado del registro digital. Este campo es utilizado para manejo interno de datos y revisiones. Los valores utilizados son dictados por el flujo de trabajo específico de cada institución." >}}

{{< dwc-term id="labelProject" verbatim="Etiqueta de Proyecto" descr="Utilizado para imprimir etiquetas. Puede crear la etiqueta de un proyecto e imprimir un conjunto de etiquetas luego de haber ingresado los datos." ex="Plants of Sedona 2012" >}}

{{< dwc-term id="duplicateQuantity" verbatim="Duplicate Quantity" descr="El número de especímenes duplicados creados. Esto indicará el número de etiquetas a ser impresas por espécimen." ex="10" >}}


### Paleontology Fields

<a id="eon"><b>Eon:</b></a> El intervalo de tiempo geológico más grande.
Ex: Archean, Proterozoic, Phanerozoic
Ver Darwin Core <a href="https://dwc.tdwg.org/terms/#dwc:earliestEonOrLowestEonothem" target="_blank" rel="noopener noreferrer">earliestEonOrLowestEonothem</a>, <a href="https://dwc.tdwg.org/terms/#dwc:latestEonOrHighestEonothem" target="_blank" rel="noopener noreferrer">latestEonOrHighestEonothem</a>

<a id="era"><b>Era:</b></a> Una subdivisión de eon que representa un intervalo de tiempo geológico más corto.<br>
Ex: Paleozoic, Mesozoic, Cenozoic.<br>
Ver Darwin Core <a href="https://dwc.tdwg.org/terms/#dwc:earliestEraOrLowestErathem" target="_blank" rel="noopener noreferrer">earliestEraOrLowestErathem</a>, <a href="https://dwc.tdwg.org/terms/#dwc:latestEraOrHighestErathem" target="_blank" rel="noopener noreferrer">latestEraOrHighestErathem</a>

<a id="period"><b>Período:</b></a> Una subdivisión de era, que representa un intervalo de tiempo geológico más corto.<br>
Ex: Ordovician, Silurian, Devonian, Carboniferous, Mississippian, Pennsylvanian, Permian, Triassic, Jurassic, Cretaceous, Paleogene, Neogene, Quaternary.<br>
Ver Darwin Core <a href="https://dwc.tdwg.org/terms/#dwc:earliestPeriodOrLowestSystem" target="_blank" rel="noopener noreferrer">earliestPeriodOrLowestSystem</a>, <a href="https://dwc.tdwg.org/terms/#dwc:latestPeriodOrHighestSystem" target="_blank" rel="noopener noreferrer">latestPeriodOrHighestSystem</a>

<a id="epoch"><b>Época:</b></a> Una subdivisión de período que representa un intervalo de tiempo geológico más corto.<br>
Ex: Lower, Middle, Upper Ordovician; Wenlock; Pridoli; Lower, Middle, Upper Devonian; Lower, Middle, Upper Mississippian; Lower, Middle, Upper Pennsylvanian; Cisuralian; Lower, Middle, Upper Jurassic; Lower, Upper Cretaceous; Paleocene; Eocene; Oligocene; Miocene; Pliocene; Pleistocene; Holocene.<br>
El campo de Época está registrado actualmente utilizado Serie, las unidades cronoestratigráficas.<br>
Ver Darwin Core <a href="https://dwc.tdwg.org/terms/#dwc:earliestEpochOrLowestSeries" target="_blank" rel="noopener noreferrer">earliestEpochOrLowestSeries</a>, <a href="https://dwc.tdwg.org/terms/#dwc:latestEpochOrHighestSeries" target="_blank" rel="noopener noreferrer">latestEpochOrHighestSeries</a>

<a id="stage"><b>Etapa:</b></a> Término cronoestratigráfico dado a la sucesión de estratos de roca depositados en una sola edad geocronológica.<br>
Ex: Lochkovian, Emsian, Eifelian, Givetian, Frasnian, Tournaisian, Serpukhovian, Moscovian, Changhsingian, Norian, Oxfordian, Hauterivian, Albian, Maastrichtian, Thanetian, Messinian, etc.<br>
Ver Darwin Core <a href="https://dwc.tdwg.org/terms/#dwc:earliestAgeOrLowestStage" target="_blank" rel="noopener noreferrer">earliestAgeOrLowestStage</a>, <a href="https://dwc.tdwg.org/terms/#dwc:latestAgeOrHighestStage" target="_blank" rel="noopener noreferrer">latestAgeOrHighestStage</a>

{{< dwc-term id="localStage" verbatim="Local Stage" descr="A local name for a stage that was applied to this specimen." ex="Ulatsian, Helvetian." >}}

{{< dwc-term id="earlyInterval" verbatim="Intervalo Temprano" descr="Nombre del eon, era, período, época o edad geocronológica más temprano posible, o el eonotema, eratema, sistema, serie o etapa cronoestratigráfica más baja atribuible al horizonte estratigráfico del cual el espécimen catalogado fue colectado." ex="Aalenian, Aeronian, Albian, Anisian, Aptian, Aquitanian, Archean, Artinskian, Asselian, Bajocian, Barremian, Bartonian, etc." >}}

{{< dwc-term id="lateInterval" verbatim="Intervalo Tardío" descr="Nombre del eon, era, período, época o edad geocronológica más tardío posible, o el eonotema, eratema, sistema, serie o etapa cronoestratigráfica más alto atribuible al horizonte estratigráfico del cual el espécimen catalogado fue colectado." ex="Aalenian, Aeronian, Albian, Anisian, Aptian, Aquitanian, Archean, Artinskian, Asselian, Bajocian, Barremian, Bartonian, etc." >}}

{{< dwc-term id="absoluteAge" verbatim="Edad Absoluta" descr="Campo para registrar la edad del espécimen/roca en años determinados usando la pérdida de isótopos radioactivos (Carbon-14, argon-argon, potassium-argon, uranium-lead, etc.) y otros métodos cuantitativos de datación." ex="20 Ma, 75 ka, 10.5 – 12.7 +/- 0.5 Ma, etc." >}}

{{< dwc-term id="storageAge" verbatim="Edad de Almacenamiento" descr="Cammpo para instituciones que arreglan las colecciones por tiempo geológico o bioestratigrafía. La ubicación física del espécimen dentro del espacio de la colección." ex="Miocene, Wasatchian, Paleocene, Bridgerian, etc." >}}

{{< dwc-term id="biota" verbatim="Biota (Flora/Fauna)" descr="Nombre dado a las colecciones de fósiles de la misma edad de una sola localidad o múltiples localidad dentro de un área geográfica específica." ex="Chalk Bluffs, Stewart Valley, Bridge Creek, Mazon Creek, etc." >}}

<a id="biostratigraphy"><b>Bioestratigrafía (Biozona):</b></a> El nombre de la zona bioestratigráfica más baja posible del horizonte estratigráfico del cual el espécimen catalogado fue colectado.<br>
Ex: “Wa0”, “Uvigerinella sparsicostata Zone”, “Ogygiocaris”<br>
Ver Darwin Core <a href="https://dwc.tdwg.org/terms/#dwc:lowestBiostratigraphicZone" target="_blank" rel="noopener noreferrer">lowestBiostratigraphicZone</a>, <a href="https://dwc.tdwg.org/terms/#dwc:highestBiostratigraphicZone" target="_blank" rel="noopener noreferrer">highestBiostratigraphicZone</a>

<a id="group"><b>Grupo:</b></a> El nombre del grupo litoestratigráfico en el cual el espécimen catalogado fue colectado. La página <a href="https://ngmdb.usgs.gov/Geolex/search" target="_blank" rel="noopener noreferrer">National Geologic Map Database Geolex Search</a> es un gran recurso para los nombres de unidades litoestratigráficas aceptadas por USGS.<br>
Ex: Bathurst, Lower Wealden, Monte Cristo, Contra Costa, Panoche, etc.<br>
Ver Darwin Core <a href="https://dwc.tdwg.org/terms/#dwc:group" target="_blank" rel="noopener noreferrer">group</a>

<a id="formation"><b>Formación:</b></a> El nombre de la formación litoestratigráfica en la cual el espécimen catalogado fue colectado. La página <a href="https://ngmdb.usgs.gov/Geolex/search" target="_blank" rel="noopener noreferrer">National Geologic Map Database Geolex Search</a> es un gran recurso para los nombres de unidades litoestratigráficas aceptadas por USGS.<br>
Ex: Notch Peak, House Limestone, Fillmore, Chinle, etc.<br>
Ver Darwin Core <a href="https://dwc.tdwg.org/terms/#dwc:formation" target="_blank" rel="noopener noreferrer">formation</a>

<a id="member"><b>Miembro:</b></a> El nombre del miembro litoestratigráfico en la cual el espécimen catalogado fue colectado. La página <a href="https://ngmdb.usgs.gov/Geolex/search" target="_blank" rel="noopener noreferrer">National Geologic Map Database Geolex Search</a> es un gran recurso para los nombres de unidades litoestratigráficas aceptadas por USGS.<br>
Ex: Lava Dam, Hellnmaria, Brown Mountain Sandstone<br>
Ver Darwin Core <a href="https://dwc.tdwg.org/terms/#dwc:member" target="_blank" rel="noopener noreferrer">member</a>

<a id="bed"><b>Cama:</b></a> Elnombre de la cama litoestratigráfica en la cual el espécimen catalogado fue colectado. La página <a href="https://ngmdb.usgs.gov/Geolex/search" target="_blank" rel="noopener noreferrer">National Geologic Map Database Geolex Search</a> es un gran recurso para los nombres de unidades litoestratigráficas aceptadas por USGS.<br>
Ex: Harlem coal<br>
Ver Darwin Core <a href="https://dwc.tdwg.org/terms/#dwc:bed" target="_blank" rel="noopener noreferrer">bed</a>

{{< dwc-term id="taxonEnvironment" verbatim="Ambiente del Taxón" descr="El ambiente deposicional de la unidad de roca en la cual el espécimen catalogado fue colectado." ex="marine, lacustrine, non-marine, marine-non-marine" >}}

{{< dwc-term id="lithology" verbatim="Litología" descr="Campo para los términos que describen los tipos de roca/sedimento en el cual el espécimen catalogado fue colectado." ex="sandstone, mudstone, siltstone, shale, etc." dwc="lithostratigraphicTerms" >}}

{{< dwc-term id="stratRemarks" verbatim="Comentarios del Estrato" descr="Campo para registrar detalles adicionales acerca de la geología, estratigrafía, litología más detallada, información de muestreos palinológicos, etc." >}}

{{< dwc-term id="element" verbatim="Elemento" descr="Campo para registrar el tipo de órgano que representa un espécimen paleobotánico." ex="stem, strobilus, sterile leaf, fertile leaf, pinnule(s), rooting organ, rootlet, megasporangium, sporangium, spore, sterile axis, fertile axis, root, etc." >}}

{{< dwc-term id="slideProperties" verbatim="Propiedades de Lámina" descr="Campo para registrar los tipos de láminas preparadas de especímenes, para resaltar el tipo de preparación y medio de montaje, y para proveer coordenadas England Finder para láminas palinomorfas." ex="strewn, petrographic thin-section, mounted peel" >}}

{{< dwc-term id="geologicalContextID" verbatim="ID de Contexto Geológico" descr="Un identificador para el conjunto de información asociada con el GeologicalContext (la ubicación en un contexto geológico, como estratigrafía). Puede ser un identificador único global o un identificador específico del conjunto de datos." ex="https://opencontext.org/subjects/e54377f7-4452-4315-b676-40679b10c4d9" dwc="geologicalContextID" >}}
