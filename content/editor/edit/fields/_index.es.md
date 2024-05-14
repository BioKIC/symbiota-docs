---
title: "Campos de Datos en Symbiota"
date: 2014-07-21
lastmod: 2024-05-14
draft: false
authors: ["Ed Gilbert","Katie Pearson","Lindsay Walker"]
editors: ["Laura Rocha Prado"]
translators: ["Samanta Orellana","Google Translate"]
keywords: ["editar","campos","campos de datos", "términos", "términos dwc"]
---

El esquema de datos Symbiota está fuertemente alineado con el del estándar de intecambio de datos <a href="https://www.tdwg.org/standards/dwc/" target="_blank" rel="noopener noreferrer">Darwin Core</a>. Para más detalles, enlaces a las definiciones Darwin Core definitions son proporcionadas para cada término. Aprenda más acerca de los términos Darwin Core en las siguientes páginas de TDWG:
- [TDWG - Guía de Referencia Rápida de Darwin Core](https://dwc.tdwg.org/terms/)
- [TDWG - Lista de Términos de Darwin Core](https://dwc.tdwg.org/list)

{{< notice note >}}
  Los campos enumerados aquí difieren de los campos visibles en las herramientas de carga de datos. Para obtener información de campo específica de las herramientas de carga de datos, consulte la [página de Campos de Importación de Datos](https://biokic.github.io/symbiota-docs/coll_manager/upload/fields/).
{{</ notice >}}

 ### Tabla de Contenido
 - [Campos Estándar](#campos-estándar)
 - [Campos de Muestra de Materiales](#campos-de-muestra-de-material)
 - [Campos Paleontología](#campos-de-paleontología)

 {{< button href="../../../documents/SymbiotaDataFields_202111.csv" text="Descargar contenido completo como un archivo CSV" >}}
{{< button href="https://github.com/BioKIC/symbiota-docs/blob/master/static/documents/SymbiotaDataFields_202111.csv" text="Ver contenido completo como un archivo CSV" >}}

{{< notice note >}}
   Dado que los portales tienen la capacidad de personalizar los nombres de los campos que se encuentran en su formulario de entrada de datos, los nombres de los campos pueden diferir de la definición del campo principal y de cómo se asigna a las herramientas de exportación de Darwin Core.
{{</ notice >}}

### Campos Estándar

{{< dwc-term id="catalogNumber" verbatim="Número de catálogo" descr="El identificador único (clave principal) para el registro de muestra. Este campo debe usarse para almacenar el código de barras o el número de acceso (solo herbarios). Se exige que este campo sea único por colección" ex="WIS-L-0123456, ASU0012345, 12345" dwc="catalogNumber" >}}

<a id="otherCatalogNumbers"><b>Valores de identificador adicionales:</b></a> Cualquier otro identificador para un registro de muestra que no sea el número de catálogo central. Este campo se utiliza normalmente para almacenar los números de catálogo antiguos, números de acceso, identificadores de parques nacionales, etc. A los identificadores se les puede asignar un nombre de etiqueta para distinguirlos de otros identificadores (por ejemplo, número de acceso antiguo, número de NPS, etc.). Estos identificadores se asignan mejor a la definición de dwc:otherCatalogNumbers y, por lo tanto, se incluyen en las exportaciones de este campo. Puede encontrar más información sobre este sistema en <a href="https://biokic.github.io/symbiota-docs/editor/edit/fields/catno/" target="_blank" rel="noopener noreferrer"> Página de documentación de números de catálogo</a>.<br>Ej: 12345, TUZI 3082, número de cuenta NPS: GUIS-M-00126.<br>Consulte <a href="https://dwc.tdwg.org/ de Darwin Core Terms/#dwc:otherCatalogNumbers" target="_blank" rel="noopener noreferrer">otherCatalogNumbers</a>

{{< dwc-term id="recordedBy" verbatim="Coleccionista" descr="El nombre de la persona que recolectó el espécimen o realizó la observación." ex="CG Pringle, Goodding, L.N." dwc="recordedBy" >}}

{{< dwc-term id="associatedCollectors" verbatim="Coleccionistas asociados" descr="Otros recolectores que estaban presentes en el momento de la recolección." ex="John R. Reeder, A. Nelson" obs="Este campo no está definido por el estándar Darwin Core, que coloca a los recopiladores primarios y secundarios concatenados en el campo grabadoPor." >}}

{{< dwc-term id="recordNumber" verbatim="Número" descr="El número de colección asignado al espécimen por el recolector." ex="1294, 12490b, 94-132" dwc="recordNumber" >}}

{{< dwc-term id="eventDate" verbatim="Fecha" descr="La fecha en que se recolectó el espécimen o, si se indica un rango de fechas, el primer día en el rango de fechas de recolección. Se pueden ingresar fechas mientras utilizando su formato preferido, el valor se convertirá y almacenará como formato numérico ISO-8601 (AAAA-MM-DD). Tenga en cuenta que los meses y días desconocidos se pueden ingresar como \"00\". la fecha de \"marzo de 1956\" se puede ingresar como \"1956-03-00\"." ex="1983-09-15, 1983-07-00, 1934-00-00" dwc="eventDate" >}}

<a id="endDate"><b>Fecha de finalización: </b></a>La última fecha de recopilación, en el caso de un rango de fechas de recopilación. Si bien las fechas se pueden ingresar usando su formato preferido, el valor se convertirá y almacenará en formato numérico ISO-8601 (AAAA-MM-DD). Tenga en cuenta que los meses y días desconocidos se pueden ingresar como \"00\". Por ejemplo, una colección con fecha de \"Marzo de 1956\" se puede ingresar como \"1956-03-00\".<br>Ej: 1983-09-15, 1983-07-00, 1934-00- 00 </br> Consulte <a href="https://dwc.tdwg.org/terms/#dwc:eventDate" target="_blank" rel="noopener noreferrer">eventDate</a> de Darwin Core.

{{< dwc-term id="verbatimEventDate" verbatim="Fecha literal" descr="Se puede utilizar para registrar la fecha exactamente como se ingresó en la etiqueta. Particularmente útil para formatos de fecha o rangos de fechas no estándar." ex="primavera de 1901, marzo-abril de 1952, finales de septiembre de 1909" dwc="verbatimEventDate" >}}

{{< dwc-term id="year" verbatim="Año" descr="El valor numérico del año en el momento de la recopilación. Este campo (junto con el mes y el día) se completa automáticamente cuando se ingresa la fecha." ex="1959" dwc="year" >}}

{{< dwc-term id="month" verbatim="Mes" descr="El valor numérico del mes en el momento de la recopilación. Este campo (junto con el año y el día) se completa automáticamente cuando se ingresa la fecha." ex="10" dwc="month" >}}

{{< dwc-term id="day" verbatim="Día" descr="El valor numérico del día en el momento de la recopilación. Este campo (junto con el año y el mes) se completa automáticamente cuando se ingresa la fecha." ex="28" dwc="day" >}}

<a id="dayRange"><b>Rango de días del año:</b></a> Aquí se puede representar un rango de fechas de recolección como valores numéricos del día del año. Estos valores se calcularán automáticamente si ingresa un rango de fechas en el campo de fecha textual (por ejemplo, del 12 de septiembre de 1968 al 19 de septiembre de 1968, del 12 de septiembre de 1968 al 19 de septiembre de 1968) <br>
Consulte <a href="https://dwc.tdwg.org/terms/#dwc:startDayOfYear" target="_blank" rel="noopener noreferrer">startDayOfYear</a>, <a href="http: //rs.tdwg.org/dwc/terms/index.htm#endDayOfYear" target="_blank" rel="noopener noreferrer">endDayOfYear</a>.

{{< dwc-term id="scientificName" verbatim="Nombre científico" descr="El nombre latino del espécimen sin el autor. Podría ser cualquier cosa, desde reino hasta subespecie o variedad, dependiendo del nivel de identificación." ex="Pinaceae, Pinus, Pinus edulis, Pinus edulis var. fallax" dwc="scientificName" >}}

{{< dwc-term id="scientificNameAuthorship" verbatim="Autor" descr="El nombre de la persona que nombró por primera vez los taxones. Este campo se completa automáticamente después de ingresar el nombre científico." ex="L., Asa A. Gray" dwc="scientificNameAuthorship" >}}

{{< dwc-term id="identificationQualifier" verbatim="Identification Qualifier" descr="Expresión de incertidumbre del determinante en su identificación. Esto aparecerá en la etiqueta junto con el nombre científico." ex="cf., aff." dwc="identificationQualifier" >}}

{{< dwc-term id="family" verbatim="Familia" descr="La familia a la que pertenece el taxón. Este campo se completa automáticamente después de ingresar el nombre científico." ex="Pinaceae" dwc="family" >}}

{{< dwc-term id="identifiedBy" verbatim="Identificado por" descr="El nombre de la persona que identificó el espécimen. También llamado determinante." ex="L. R. Landrum" dwc="identifiedBy" >}}

{{< dwc-term id="dateIdentified" verbatim="Fecha de identificación" descr="La fecha en que se realizó la identificación. La fecha se puede ingresar como texto libre y no es necesario que esté en un formato de fecha estándar." ex="1992, mayo de 1992, 2 de mayo de 1992" dwc="dateIdentified" >}}

{{< dwc-term id="identificationReferences" verbatim="Referencias de ID" descr="La fuente de referencia utilizada para realizar la identificación." ex="Nesom, Guy L. 2006. Flora de América del Norte - Asteraceae. vol. 20" dwc="identificationReferences" >}}

{{< dwc-term id="identificationRemarks" verbatim="ID Remarks" descr="Cualquier nota adicional relacionada con la identificación del espécimen." dwc="identificationRemarks" >}}

{{< dwc-term id="taxonRemarks" verbatim="Observaciones sobre el taxón" descr="Cualquier nota adicional sobre el nombre taxonómico con el que se identificó el espécimen." dwc="taxonRemarks" >}}

{{< dwc-term id="continent" verbatim="Continente" descr="El nombre del continente en el que se recolectó el espécimen." ex="América del Norte, África" dwc="continent" >}}

{{< dwc-term id="waterBody" verbatim="Cuerpo de agua" descr="El nombre del cuerpo de agua en el que se recolectó la muestra." ex="Océano Pacífico, Mar Negro" dwc="waterBody" >}}

{{< dwc-term id="islandGroup" verbatim="Grupo de islas" descr="El nombre del grupo de islas en el que se recolectó el espécimen." ex="Islas Hawaianas, Archipiélago Alejandro" dwc="islandGroup" >}}

{{< dwc-term id="island" verbatim="Isla" descr="El nombre de la isla en la que se recolectó el espécimen." ex="Cayo Coco, Maui" dwc="island" >}}

{{< dwc-term id="country" verbatim="Country" descr="El nombre del país en el que se recopiló el espécimen. Para facilitar la entrada de datos, aparecerá un menú desplegable en el que se escribe uno, aunque los nombres fuera de Todavía se puede entrar en la lista." ex="EE.UU., Canadá, México" dwc="country" >}}

{{< dwc-term id="stateProvince" verbatim="State/Province" descr="El nombre del estado o provincia en el que se recopiló el espécimen. Como uno de los tipos, aparecerá una lista de selección para el país determinado." ex="Nueva York, Arizona, Sonora" dwc="stateProvince" >}}

{{< dwc-term id="county" verbatim="County" descr="El nombre del condado en el que se recolectó el espécimen. Elija uno del menú desplegable. Para especímenes recolectados fuera de los Estados Unidos, ingrese el siguiente región geográfica debajo del estado/provincia." ex="Maricopa" dwc="county" >}}

{{< dwc-term id="municipality" verbatim="Municipalidad" descr="El nombre del municipio en el que se recolectó el espécimen. Para especímenes recolectados fuera de los Estados Unidos, ingrese la designación geográfica de cuarto nivel." ex="Valle Paraíso" dwc="municipality" >}}

{{< dwc-term id="locality" verbatim="Localidad" descr="La ubicación detallada en la que se recolectó el espécimen." ex="9,5 millas al NO de Sedona a lo largo de Boynton Pass Rd." dwc="locality" >}}

{{ dwc-term id="locationID" verbatim = "ID de Ubicación" desc="Un identificador para el conjunto de información de ubicación (datos asociados con dcterms:Location). Puede ser un identificador único global o un identificador específico del conjunto de datos." ex="https://opencontext.org/subjects/768A875F-E205-4D0B-DE55-BAB7598D0FD1" dwc="locationID" >}}

<a id="localitySecurity"><b>Seguridad de la localidad:</b></a> Al marcar la casilla de verificación Seguridad de la localidad se ocultarán los detalles de la localidad por debajo del nivel del condado a usuarios no autorizados. Por lo general, esto se hace porque la especie es rara o está amenazada. Las imágenes también están ocultas para proteger los detalles de la localidad que podrían verse en la etiqueta. Los usuarios que hayan iniciado sesión en el sistema y tengan el permiso necesario para ver los detalles de la localidad (por ejemplo, administradores de colecciones) seguirán teniendo acceso a todos los datos. Esta casilla se marcará automáticamente si el nombre de la especie aparece en alguna de las listas de especies raras (ver mapa del sitio). Si desea bloquear la protección (activada o desactivada), haga clic en la casilla de verificación Bloquear seguridad y/o ingrese un motivo para anular la seguridad en el campo de texto. Dejar la seguridad de la localidad desbloqueada permitirá que se apliquen las configuraciones predeterminadas según lo determinen los administradores de especies sensibles, que es la recomendación para la mayoría de los registros. <br>
Para obtener más información sobre la protección de especies sensibles, consulte la página <a href="https://biokic.github.io/symbiota-docs/user/redaction/">Protección de especies sensibles</a>. <br>
Este campo no está definido por el estándar Darwin Core.

{{< dwc-term id="locationRemarks" verbatim="Comentarios sobre la ubicación" descr="Comentarios o notas sobre la localidad" ex="Anteriormente conocida como Mt. Evans" dwc="locationRemarks" >}}

{{< dwc-term id="decimalLatitude" verbatim="Latitud y longitud (formato decimal)" descr="Latitud y longitud geográficas en grados decimales. Las latitudes del hemisferio sur y las longitudes en el hemisferio occidental (por ejemplo, EE. UU.) deben deben ingresarse como valores negativos. Haga clic en el botón \"Herramientas\" para ingresar las coordenadas en grados, minutos, segundos (DMS) o los formatos UTM. Los grados decimales son el estándar de coordenadas preferido según lo define Darwin Core. más información sobre el uso de esta herramienta." ex="34.874022, -111.75774" dwc="decimalLatitude" >}}

{{< dwc-term id="coordinateUncertaintyInMeters" verbatim="Incertidumbre (metros)" descr="La precisión de las coordenadas de georeferencia en metros (solo valor numérico). Esto se mide como el radio de un círculo donde estaría el punto verdadero. Si se conocen las coordenadas, la precisión sería el error encontrado dentro de la unidad GPS (generalmente alrededor de 10 m). Mientras que los especímenes recolectados previamente que tienen coordenadas en la etiqueta registrada por el recolector generalmente no indican el fuente de las coordenadas (GPS, mapa, etc.), normalmente es una buena suposición que las coordenadas son precisas entre uno y doscientos metros. Si los detalles de la localidad son vagos, como simplemente \"Gran Cañón\", entonces las coordenadas deberían. sea el centroide dentro de la incertidumbre que abarca el área mayor donde se pudo haber recolectado el espécimen. Si la localidad es \"Boynton Canyon, Sedona\", la incertidumbre sería de aproximadamente 1500 m. Este campo se completa automáticamente cuando se utiliza GeoLocate para georreferenciación." ex="42000 para Phoenix, 20000 para Salt Lake City" dwc="coordinateUncertaintyInMeters" >}}

{{< dwc-term id="geodeticDatum" verbatim="Datum" descr="El sistema geográfico que se usó para obtener las coordenadas. Este campo se completa automáticamente cuando se usa [http://www.museum.tulane.edu/geolocate/ |GeoLocate] o la herramienta de georreferenciación de Google Maps." ex="NAD27, NAD83, WGS84" dwc="geodeticDatum" >}}

<a id="verbatimCoordinates"><b>Coordenadas textuales:</b></a> Si las coordenadas registradas en la etiqueta de la muestra están en un formato que no sea grados decimales, ingréselo aquí. Cuando los campos de latitud y longitud decimales están en blanco y se ingresa UTM o DMS utilizando uno de los formatos que se muestran en el ejemplo siguiente, los valores de latitud y longitud decimales se generarán automáticamente. Haga clic en "&lt;&lt;" símbolo para reemplazar los valores decimales existentes. Este campo se completa automáticamente cuando se utilizan las herramientas de georreferenciación DMS, UTM y TRS.<br>
Ej: 34° 13,940' N 112° 2,370' W, 12 420944E 4064025N, TRS: T40N R32E S29 <br>
Consulte <a href="https://dwc.tdwg.org/terms/#dwc:verbatimCoordinates" target="_blank" rel="noopener noreferrer">verbatimCoordinates</a> de Darwin Core.

{{< dwc-term id="minimumElevationInMeters" verbatim="Elevación en metros" descr="La elevación en metros a la que se recolectó el espécimen. También llamada altitud. Use solo el campo izquierdo y el derecho en blanco cuando se trate de una sola elevación. existe." ex="1400, 2000-2200" dwc="minimumElevationInMeters" >}}

<a id="verbatimElevation"><b>Elevación textual:</b></a> La elevación textual a la que se recopiló la muestra. Normalmente se utiliza para registrar una medición de elevación que se registró en pies o una designación de incertidumbre. Cuando el campo de elevación en metros se deja en blanco, el valor se convertirá automáticamente a metros. Haga clic en "&lt;&lt;" símbolo para reemplazar los valores de medidores ingresados previamente.<br>
Ej: 4500 pies, 4500 pies, ca 4500', ca 2000 m, 4500' +-300'<br>
Consulte <a href="https://dwc.tdwg.org/terms/#dwc:verbatimElevation" target="_blank" rel="noopener noreferrer">verbatimElevation</a> de Darwin Core.

<a id="minimumDepthInMeters"><b>Profundidad en metros:</b></a> El rango de profundidad debajo de la superficie local, en metros.<br>
Ej: 100, 150-200<br>
Consulte los <a href="http://rs.tdwg.org/dwc/terms/minimumDepthInMeters" target="_blank" rel="noopener noreferrer">minimumDepthInMeters</a>, <a href="https:/ /dwc.tdwg.org/terms/#dwc:maximumDepthInMeters" target="_blank" rel="noopener noreferrer">maximumDepthInMeters</a>.

{{< dwc-term id="verbatimDepth" verbatim="Profundidad literal" descr="La descripción literal original de la profundidad debajo de la superficie local en la que se recolectó el espécimen." ex="100 pies, 100 pies, aproximadamente 100', aproximadamente 30 m, 100' +-10'" dwc="verbatimDepth" >}}

{{< dwc-term id="georeferencedBy" verbatim="Georeferenced By" descr="El nombre de la persona que georeferencia el registro de muestra. Este campo se completa automáticamente cuando se utiliza GeoLocate para georreferenciar." ex="A. Gonzales, emakings, acbarber" dwc="georeferencedBy" >}}

{{< dwc-term id="georeferenceProtocol" verbatim="Protocolo de georeferencia" descr="La fuente de los estándares utilizados para georreferenciar." ex="Guía rápida de georeferenciación. Zermoglio et al. 2020" dwc="georeferenceProtocol" >}}

{{< dwc-term id="georeferenceSources" verbatim="Fuentes de georreferenciación" descr="La herramienta o herramientas utilizadas para georreferenciar." ex="GeoLocate, Google Earth, mapa USGS" dwc="georeferenceSources" >}}

{{< dwc-term id="georeferenceVerificationStatus" verbatim="Estado de verificación de Georef" descr="Dice si la georeferencia ha sido revisada o verificada." ex="revisado, no revisado" dwc="georeferenceVerificationStatus" >}}

{{< dwc-term id="georeferenceRemarks" verbatim="Observaciones de georeferencia" descr="Cualquier nota adicional sobre la georreferenciación del espécimen." dwc="georeferenceRemarks" >}}

{{< dwc-term id="habitat" verbatim="Habitat" descr="La descripción del hábitat en el que se recolectó el espécimen." ex="Áreas húmedas a lo largo de un pequeño arroyo en chaparral." dwc="habitat" >}}

{{< dwc-term id="substrate" verbatim="Sustrato" descr="El sustrato sobre el cual se recolectó la muestra. Se utiliza principalmente para muestras de líquenes y briofitas." ex="Sobre basalto, tronco de roble" obs="Darwin Core agrupa esta información en el hábitat." >}}

{{< dwc-term id="associatedTaxa" verbatim="Taxones asociados" descr="Una lista de los nombres de otras especies que aparecen con el espécimen recolectado." ex="Quercus, Arctostaphylos, Ceanothus, Rhus, Eriogonum, Salvia" dwc="associatedTaxa" >}}
* En MycoPortal, este es también el campo donde se almacena la información del "host". Consulte [este comentario para obtener instrucciones] (https://github.com/BioKIC/symbiota-docs/issues/36#issuecomment-1015733243).

{{< dwc-term id="verbatimAttributes" verbatim="Description" descr="Una descripción física del espécimen en el momento de la recolección. Esto a menudo incluye información que puede perderse o ser difícil de observar después del proceso de recolección y preservación. " ex="Arbusto de 3 m de altura, corola amarilla" >}}

{{< dwc-term id="occurrenceRemarks" verbatim="Notas" descr="Cualquier nota adicional sobre la muestra." dwc="occurrenceRemarks" >}}

{{< dwc-term id="dynamicProperties" verbatim="Propiedades dinámicas" descr="Una lista de mediciones, hechos, características o afirmaciones adicionales sobre el espécimen en un formato que permite el análisis programático de los datos. Consulte Darwin Core enlace a continuación para obtener más detalles." ex="awnLengthInMeters=0.014, heightInMeters=1.5, relativaHumedad=28, airTemperatureInC=22" dwc="dynamicProperties" >}}

{{< dwc-term id="lifeStage" verbatim="Etapa de vida" descr="La edad o etapa del organismo en el momento de la recolección/observación. Normalmente se utiliza para colecciones zoológicas." ex="larva, juvenil" dwc="lifeStage" >}}

{{< dwc-term id="sex" verbatim="Sexo" descr="El sexo biológico del suceso." ex="mujer, hombre" dwc="sex" >}}

{{< dwc-term id="individualCount" verbatim="Recuento de individuos" descr="El número de individuos representados por la ocurrencia" ex="2, 15" dwc="individualCount" >}}

{{< dwc-term id="samplingProtocol" verbatim="Protocolo de muestreo" descr="Los nombres y referencias a los métodos utilizados para recolectar o tomar muestras de un suceso" ex="Trampa de luz ultravioleta, red de niebla, Takats et al. 2001. Directrices para el seguimiento de búhos nocturnos en América del Norte. Beaverhill Bird Observatory and Bird Studies Canada, Edmonton, Alberta 32 págs., http://www.bsc-eoc.org/download/Owl.pdf" dwc="samplingProtocol">}}

{{< dwc-term id="preparations" verbatim="Preparaciones" descr="Método de preparación o conservación de una muestra" ex="en etanol, esqueleto" dwc="preparations" >}}

{{< dwc-term id="reproductiveCondition" verbatim="Fenología (Condición reproductiva)" descr="La etapa reproductiva en la que se encuentra el espécimen. Normalmente se utiliza para colecciones de plantas y hongos." ex="flor, fruto, estéril" dwc="reproductiveCondition" >}}

{{< dwc-term id="behavior" verbatim="Behavior" descr="El comportamiento exhibido por el organismo/ocurrencia en el momento de la recolección/observación." ex="volar, sentarse sobre huevos" dwc="behavior" >}}

{{< dwc-term id="vitality" verbatim="Vitalidad" descr="Una indicación de si el organismo estaba vivo o muerto en el momento de la recolección u observación." ex="vivo, muerto" dwc="vitality" >}}

{{< dwc-term id="establishmentMeans" verbatim="Medios de establecimiento" descr="El estado del establecimiento en el momento de la recolección." ex="cultivados, invasivos, nativos" dwc="establishmentMeans" >}}

{{< dwc-term id="isCultivated" verbatim="Cultivated Checkbox" descr="Marque cuándo el organismo se estableció con la ayuda de humanos y no podría existir por sí solo. Este campo verdadero/falso habilita la capacidad para filtrar especies no nativas o naturalizadas." obs="Actualmente no exportado en formato DwC.">}}

{{< dwc-term id="typeStatus" verbatim="Tipo Estado" descr="La designación de tipo de un espécimen, si es un espécimen tipo" ex="HOLOTYPE, ISOTYPE, PARATYPE" dwc="typeStatus">}}

{{< dwc-term id="disposition" verbatim="Disposición" descr="La ubicación o estado de la muestra física." ex="desaparecido, en préstamo, en cobranza" dwc="disposition" >}}

{{< dwc-term id="occurrenceid" verbatim="Occurrence ID" descr="Esta es la identificación única global (GUID) del espécimen. Este código de identificación debe ser estable e identificar de manera única el espécimen en relación con todos los demás especímenes dentro Si su colección está configurada para tener ID de ocurrencia/GUID generados por el portal (esta es la configuración sugerida para todas las colecciones administradas en vivo), este campo aparecerá en blanco en el formulario del editor de ocurrencias para ver el valor de ID de ocurrencia asociado con su. muestra, haga clic en el enlace Exhibición pública en la parte superior de la página" ex="000866d2-c177-4648-a200-ead4007051b9, urn:catalog:UWBM:Bird:89776" dwc="occurrenceId">}}

{{< dwc-term id="fieldnumber" verbatim="Número de campo" descr="Un identificador dado al evento de recolección en el campo. Este número a menudo sirve como vínculo entre el evento indicado en las notas de campo y el registro del espécimen " ex="2024-04-05-00045, JOSHUATREE_35" dwc="fieldnumber" >}}

{{< dwc-term id="language" verbatim="Idioma" descr="El idioma de la información de la etiqueta" ex="Inglés, español, portugués" dwc="language" >}}

{{< dwc-term id="labelproject" verbatim="Proyecto de etiquetas" descr="Se utiliza para imprimir etiquetas. Puede crear un proyecto de etiquetas e imprimir ese conjunto de etiquetas después de haber ingresado los datos." ex="Plantas de Sedona 2012" >}}

{{< dwc-term id="duplicatequantity" verbatim="Cantidad duplicada" descr="El número de muestras duplicadas creadas. Esto determinará el número de etiquetas impresas para la muestra." ex="10" >}}

{{< dwc-term id="institutionCode" verbatim="Código de institución" descr="El acrónimo de la institución que administra este suceso. Introduzca un valor únicamente si la institución es diferente de lo que se ingresó cuando se crearon los metadatos de la institución. añadido al portal." ex="NMNH, FLMNH" dwc="institutionCode" >}}

{{< dwc-term id="collectionCode" verbatim="Código de colección" descr="El acrónimo de la colección que administra este suceso. Ingrese solo un valor si la colección es diferente de lo que se ingresó cuando se crearon los metadatos de la colección. añadido al portal." ex="Herps, F" dwc="collectionCode" >}}

{{< dwc-term id="ownerInstitutionCode" verbatim="Código de propietario" descr="El nombre (o acrónimo) utilizado por la institución propietaria de los objetos o la información a que se hace referencia en el registro." ex="NPS" dwc="ownerInstitutionCode" >}}

{{< dwc-term id="basisOfRecord" verbatim="Base del registro" descr="El tipo de registro en el que se clasifica el espécimen. Para colecciones físicas, este campo por defecto es \"PreservedSpecimen\" (también conocido como espécimen de herbario) y para observación proyectos, el valor predeterminado es \"Observación\"." ex="Espécimen preservado, espécimen vivo, observación" dwc="basisOfRecord" >}}

{{< dwc-term id="processingStatus" verbatim="Estado de procesamiento" descr="El estado del registro digital. Este campo se utiliza para la gestión y revisión interna de datos. Los valores utilizados están dictados por el flujo de trabajo específico de cada institución." >}}

{{< dwc-term id="dataGeneralizations" verbatim="Generalizaciones de datos" descr="Notas internas asociadas con el registro de ocurrencia. Los datos ingresados en este campo no son visibles para el público y no se descargan en un Archivo Darwin Core." >}}

### Campos de Muestra de Material

| ![Módulo de muestra de material](/symbiota-docs/images/materialsampleblank.png) |
|:--:|
| Pestaña Muestra de material |

{{< notice note >}}
   Los vocabularios controlados para los campos de datos de Muestras de materiales se administran por portal, y los ejemplos sugeridos que se proporcionan a continuación se derivan de los vocabularios utilizados para el [NEON Biorepository](https://biorepo.neonscience.org/portal/). Estos vocabularios varían según el portal y las modificaciones pueden requerir la opinión de la comunidad. Comuníquese con el administrador de su portal para obtener más información.
{{</ notice >}}

{{< dwc-term id="sampleType" verbatim="Tipo de muestra" descr="Vocabulario controlado que define el tipo de muestra, que a menudo es de naturaleza anatómica." ex="cráneo, hígado, tracto gastrointestinal, ectoparásito" dwc="" >}}

{{< dwc-term id="catalogNumber" verbatim="Número de catálogo/código de barras" descr="Un identificador único para la muestra de material, análogo a _catalogNumber_ para apariciones de muestras." ex="WIS-L-0123456, ASU0012345" dwc="número de catálogo" >}}

{{< dwc-term id="matSampleID" verbatim="ID de muestra de material (GUID)" descr="Un identificador único global para la muestra de material. En ausencia de un identificador único global persistente, construya uno a partir de una combinación de identificadores en el registro que hará que este identificador sea globalmente único." ex="06809dc5-f143-459a-be1a-6f03e63fc083" dwc="materialSampleID" >}}

{{< dwc-term id="sampleCondition" verbatim="Condition" descr="Campo de texto libre para describir la condición física de la muestra. Se recomienda el uso de un vocabulario controlado, pero no es obligatorio." ex="muy pobre, pobre, regular, bueno, desconocido" dwc="" >}}

{{< dwc-term id="disposition" verbatim="Disposición" descr="Vocabulario controlado que describe el estado actual de una muestra con respecto a su colección." ex="en cobranza, en proceso, consumido, en préstamo" dwc="disposition" >}}

{{< dwc-term id="preservationType" verbatim="Tipo de conservación" descr="Vocabulario controlado que define el método de conservación/almacenamiento físico de una muestra." ex="seco, etanol, congelado, fijado" dwc="" >}}

{{< dwc-term id="preparationDate" verbatim="Fecha de preparación" descr="La fecha de preparación física de una muestra. Las fechas en este campo se ajustan visualmente al formato MM/DD/AAAA. La entrada manual de datos en este campo está validada usando un formulario de calendario." ex="01/08/2022" dwc="" >}}

{{< dwc-term id="preparedByUid" verbatim="Preparado por" descr="Nombre de la persona que preparó una muestra. La persona debe tener una cuenta de usuario en el portal para ser registrado en este campo." ex="Liao, Rosie; Johnston, Andrew" dwc="" >}}

{{< dwc-term id="preparationDetails" verbatim="Detalles de preparación" descr="Campo de texto libre para registrar notas que brindan más contexto sobre la preparación física y el estado de la muestra." ex="tracto gastrointestinal superior e inferior; riñón, izquierdo, entero; preparado con bórax" dwc="" >}}

{{< dwc-term id="individualCount" verbatim="Recuento individual" descr="El número de objetos prestables asociados con la muestra, es decir, todas las piezas de la muestra asignadas al mismo material únicoSampleID (ver arriba)." ex="0, 1, 100" dwc="individualCount" >}}

{{< dwc-term id="sampleSize" verbatim="Tamaño de la muestra" descr="Campo de texto libre para cuantificar la muestra más allá del número de objetos contados, por ejemplo, peso seco." ex="200 uL" dwc="" >}}

{{< dwc-term id="storageLocation" verbatim="Ubicación de almacenamiento" descr="Campo de texto libre para describir la ubicación de almacenamiento físico permanente de una muestra." ex="Congelador 3; Almacenamiento de gran tamaño; Cab011, Dwr002" dwc="" >}}

{{< dwc-term id="remarks" verbatim="Observaciones" descr="Campo de texto libre para proporcionar notas adicionales, comentarios y contexto exclusivo de una muestra que no puede ser capturado por otros campos de datos existentes. Limitado a 250 caracteres. " ex="muestreo de genotipo; mandíbula izquierda consumida en investigación; con esqueleto postcraneal" dwc="" >}}

### Campos de Paleontología

| ![Módulo Paleo](/symbiota-docs/images/paleo_module.png) |
|:--:|
| Módulo Paleo en la pestaña Datos de ocurrencia |

{{< notice note >}}
   Los vocabularios controlados para los siguientes campos de datos se gestionan por portal. Las modificaciones a estos valores pueden requerir discusión comunitaria. Comuníquese con el administrador de su portal para obtener más información.
{{</ notice >}}

<a id="eon"><b>Eón:</b></a> Los intervalos de tiempo geológicos más largos.
Ej: Arcaico, Proterozoico, Fanerozoico
Consulte <a href="https://dwc.tdwg.org/terms/#dwc:earliestEonOrLowestEonothem" target="_blank" rel="noopener noreferrer">earliestEonOrLowestEonothem</a>, <a href="https: //dwc.tdwg.org/terms/#dwc:latestEonOrHighestEonothem" target="_blank" rel="noopener noreferrer">latestEonOrHighestEonothem</a>

<a id="era"><b>Era:</b></a> Una subdivisión de un eón que es un intervalo más corto de tiempo geológico.<br>
Ej: Paleozoico, Mesozoico, Cenozoico.<br>
Consulte <a href="https://dwc.tdwg.org/terms/#dwc:earliestEraOrLowestErathem" target="_blank" rel="noopener noreferrer">earliestEraOrLowestErathem</a>, <a href="https: //dwc.tdwg.org/terms/#dwc:latestEraOrHighestErathem" target="_blank" rel="noopener noreferrer">latestEraOrHighestErathem</a>

<a id="period"><b>Período:</b></a> Subdivisión de una era que es un intervalo más corto de tiempo geológico.<br>
Ej: Ordovícico, Silúrico, Devónico, Carbonífero, Misisipi, Pensilvania, Pérmico, Triásico, Jurásico, Cretácico, Paleógeno, Neógeno, Cuaternario.<br>
Consulte <a href="https://dwc.tdwg.org/terms/#dwc:earliestPeriodOrLowestSystem" target="_blank" rel="noopener noreferrer">earliestPeriodOrLowestSystem</a>, <a href="https: //dwc.tdwg.org/terms/#dwc:latestPeriodOrHighestSystem" target="_blank" rel="noopener noreferrer">latestPeriodOrHighestSystem</a>

<a id="epoch"><b>Época:</b></a> Una subdivisión de un período que es un intervalo más corto de tiempo geológico.<br>
Ej: Ordovícico Inferior, Medio y Superior; Wenlock; Pridoli; Devónico inferior, medio y superior; Misisipio inferior, medio y superior; Pensilvania inferior, media y superior; cisuraliano; Jurásico Inferior, Medio y Superior; Cretácico inferior y superior; Paleoceno; Eoceno; oligoceno; Mioceno; Plioceno; Pleistoceno; Holoceno.<br>
El campo Época se está registrando actualmente utilizando Series, las unidades cronoestratigráficas.<br>
Consulte <a href="https://dwc.tdwg.org/terms/#dwc:earliestEpochOrLowestSeries" target="_blank" rel="noopener noreferrer">earliestEpochOrLowestSeries</a>, <a href="https: //dwc.tdwg.org/terms/#dwc:latestEpochOrHighestSeries" target="_blank" rel="noopener noreferrer">latestEpochOrHighestSeries</a>

<a id="stage"><b>Etapa:</b></a> Término cronoestratigráfico dado a la sucesión de estratos rocosos depositados en una única edad geocronológica.<br>
Ej: Lochkoviano, Emsiano, Eifeliano, Givetiano, Frasniano, Tournaisiano, Serpujoviano, Moscoviano, Changhsingiano, Noriano, Oxfordiano, Hauteriviano, Albiano, Maastrichtiano, Thanetiano, Messiniense, etc.<br>
Consulte <a href="https://dwc.tdwg.org/terms/#dwc:earliestAgeOrLowestStage" target="_blank" rel="noopener noreferrer">earliestAgeOrLowestStage</a>, <a href="https: //dwc.tdwg.org/terms/#dwc:latestAgeOrHighestStage" target="_blank" rel="noopener noreferrer">latestAgeOrHighestStage</a>

{{< dwc-term id="localStage" verbatim="Etapa local" descr="Un nombre local para una etapa que se aplicó a este espécimen." ex="Ulatsiano, Helvético." >}}

{{< dwc-term id="earlyInterval" verbatim="Intervalo Temprano" descr="Nombre del eón, era, período, época o edad geocronológica más antigua posible, o del eonotema, eratema, sistema, serie o etapa cronoestratigráfico más bajo posible atribuible al horizonte estratigráfico del cual se recolectó el espécimen catalogado." ex="Aaleniano, Aeroniano, Albiano, Anisiano, Aptiense, Aquitano, Arcaico, Artinskiano, Asseliano, Bajociano, Barremiano, Bartoniano, etc." >}}

{{< dwc-term id="lateInterval" verbatim="Late Interval" descr="Nombre del último eón, era, período, época o edad geocronológica posible, o del más alto eónotema, eratema, sistema, serie o etapa cronoestratigráfico atribuible al horizonte estratigráfico del cual se recolectó el espécimen catalogado." ex="Aaleniano, Aeroniano, Albiano, Anisiano, Aptiense, Aquitano, Arcaico, Artinskiano, Asseliano, Bajociano, Barremiano, Bartoniano, etc." >}}

{{< dwc-term id="absoluteAge" verbatim="Absolute Age" descr="Campo para registrar la edad del espécimen/roca en años determinada mediante desintegración radiactiva de isótopos (Carbono-14, argón-argón, potasio-argón, uranio-plomo, etc.) y otros métodos de datación cuantitativa." ex="20 Ma, 75 ka, 10,5 – 12,7 +/- 0,5 Ma, etc." >}}

{{< dwc-term id="storageAge" verbatim="Storage Age" descr="Campo para instituciones que organizan colecciones por tiempo geológico o bioestratigrafía. La ubicación física de un espécimen dentro del espacio de colección." ex="Mioceno, Wasatchiano, Paleoceno, Bridgeriano, etc." >}}

{{< dwc-term id="biota" verbatim="Biota (Flora/Fauna)" descr="Nombre que se da a las colecciones de fósiles de la misma edad de una sola localidad o de múltiples localidades dentro de un área geográfica específica." ex="Chalk Bluffs, Stewart Valley, Bridge Creek, Mazon Creek, etc." >}}

<a id="biostratigraphy"><b>Bioestratigrafía (Biozona):</b></a> El nombre de la zona bioestratigráfica geológica más baja posible del horizonte estratigráfico del cual se recolectó el elemento catalogado.<br>
Ej: "Wa0", "Zona Uvigerinella sparsicostata", "Ogygiocaris"<br>
Consulte <a href="https://dwc.tdwg.org/terms/#dwc:lowestBiostratigraphicZone" target="_blank" rel="noopener noreferrer">lowestBiostratigraphicZone</a>, <a href="https: //dwc.tdwg.org/terms/#dwc:highestBiostratigraphicZone" target="_blank" rel="noopener noreferrer">highestBiostratigraphicZone</a>

<a id="group"><b>Grupo:</b></a> El nombre del grupo litoestratigráfico del que se recolectó el espécimen catalogado. La <a href="https://ngmdb.usgs.gov/Geolex/search" target="_blank" rel="noopener noreferrer">Búsqueda Geolex de la base de datos de mapas geológicos nacionales</a> es un gran recurso para las áreas litoestratigráficas nombradas. unidades aceptadas por el USGS.<br>
Ej: Bathurst, Lower Wealden, Monte Cristo, Contra Costa, Panoche, etc.<br>
Consulte el <a href="https://dwc.tdwg.org/terms/#dwc:group" target="_blank" rel="noopener noreferrer">grupo</a> de Darwin Core.

<a id="formation"><b>Formación:</b></a> El nombre de la formación litoestratigráfica de la que se recolectó el espécimen catalogado. La <a href="https://ngmdb.usgs.gov/Geolex/search" target="_blank" rel="noopener noreferrer">Búsqueda Geolex de la base de datos de mapas geológicos nacionales</a> es un gran recurso para las áreas litoestratigráficas nombradas. unidades aceptadas por el USGS.<br>
Ej: Notch Peak, House Limestone, Fillmore, Chinle, etc.<br>
Consulte la <a href="https://dwc.tdwg.org/terms/#dwc:formation" target="_blank" rel="noopener noreferrer">formación</a> de Darwin Core.

<a id="member"><b>Miembro:</b></a> El nombre del miembro litoestratigráfico del que se recopiló el elemento catalogado. La <a href="https://ngmdb.usgs.gov/Geolex/search" target="_blank" rel="noopener noreferrer">Búsqueda Geolex de la base de datos de mapas geológicos nacionales</a> es un gran recurso para las áreas litoestratigráficas nombradas. unidades aceptadas por el USGS.<br>
Ej: presa de lava, Hellnmaria, arenisca de montaña marrón<br>
Consulte el <a href="https://dwc.tdwg.org/terms/#dwc:member" target="_blank" rel="noopener noreferrer">miembro</a> de Darwin Core.

<a id="bed"><b>Lecho:</b></a> El nombre del lecho litoestratigráfico del que se recolectó el elemento catalogado. La <a href="https://ngmdb.usgs.gov/Geolex/search" target="_blank" rel="noopener noreferrer">Búsqueda Geolex de la base de datos de mapas geológicos nacionales</a> es un gran recurso para las áreas litoestratigráficas nombradas. unidades aceptadas por el USGS.<br>
Ej: carbón de Harlem<br>
Vea la <a href="https://dwc.tdwg.org/terms/#dwc:bed" target="_blank" rel="noopener noreferrer">cama</a> de Darwin Core.

{{< dwc-term id="taxonEnvironment" verbatim="Taxon Environment" descr="El ambiente de depósito de la unidad de roca de la cual se recolectó el espécimen catalogado." ex="marino, lacustre, no marino, marino-no-marino" >}}

{{< dwc-term id="lithology" verbatim="Lithology" descr="Campo para términos que describen los tipos de roca/sedimento de los cuales se recolectó el espécimen catalogado." ex="arenisca, lutita, limolita, esquisto, etc." dwc="Términos litoestratigráficos" >}}

{{< dwc-term id="stratRemarks" verbatim="Strat Remarks" descr="Campo para registrar detalles adicionales sobre geología, estratigrafía, descripción litología más detallada, información de muestreo palinológico, datos de núcleos, etc." >}}

{{< dwc-term id="elemento" verbatim="Elemento" descr="Campo para registrar el tipo de órgano vegetal que representa el espécimen catalogado." ex="tallo, estróbilo, hoja estéril, hoja fértil, pínula(s), órgano radicular, raicilla, megasporangio, esporangio, espora, eje estéril, eje fértil, raíz, etc." >}}

{{< dwc-term id="slideProperties" verbatim="Propiedades de diapositiva" descr="Campo para registrar tipos de portaobjetos preparados de especímenes, indicando el tipo de preparación y medio de montaje, y para proporcionar las coordenadas del England Finder para portaobjetos palinomorfos." ex="pelado montado, de sección delgada petrográfica, esparcido" >}}

{{< dwc-term id="geologicalContextID" verbatim="ID de contexto geológico" descr="Un identificador para el conjunto de información asociada con un contexto geológico (la ubicación dentro de un contexto geológico, como la estratigrafía). Puede ser un único global identificador o un identificador específico del conjunto de datos." ex="https://opencontext.org/subjects/e54377f7-4452-4315-b676-40679b10c4d9" dwc="geologicalContextID" >}}