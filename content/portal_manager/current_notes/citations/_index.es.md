---
title: "Citando portales Symbiota y ocurrencias"
date: 2022-09-01
lastmod: 2022-09-01
authors: ["Laura Rocha Prado"]
translators: ["Samanta Orellana"]
draft: false
weight: 10
keywords: ["citando","citas","descargas"]
---

## De agosto 2022-a la fecha: Formatos de citas e introducción a CITEME.txt

Los formatos de citas y la creación de un archivo `CITEME.txt` ha sido introducido recientemente en Symbiota ([Pull Request #261](https://github.com/BioKIC/Symbiota/pull/261)).

### Formatos predeterminados
Los portales Symbiota ahora cuentan con un formato estandarizado para que los usuarios puedan citarlos, junto con sus datos. Estos formatos predeterminados y dinámicos han sido incorporados en los portales (y pueden ser personalizados de ser necesario), y pueden ser encontrados en el [directorio `[root]/includes`](https://github.com/BioKIC/Symbiota/tree/master/includes):
- Portal en general: se encuentra en [`citationportal_template.php`](https://github.com/BioKIC/Symbiota/blob/master/includes/citationportal_template.php);
- Colecciones (para colecciones no publicadas en GBIF): [`citationcollection_template.php`](https://github.com/BioKIC/Symbiota/blob/master/includes/citationcollection_template.php);
- Colección publicada en GBIF: [`citationgbif_template.php`](https://github.com/BioKIC/Symbiota/blob/master/includes/citationgbif_template.php);
- Conjunto de Datos: [`citationdataset_template.php`](https://github.com/BioKIC/Symbiota/blob/master/includes/citationdataset_template.php);

Adicionalmente, la plantilla para la página de Políticas de Uso ([`[root]/includes/usagepolicy_template.php`](https://github.com/BioKIC/Symbiota/blob/master/includes/usagepolicy_template.php)) ha sido actualizada para incluir los formatos dinámicos. Esto significa que los administradores de los portales que deseen personalizar los formatos de cita, pueden hacerlo por si mismos. 

### ¿En dónde en Symbiota son utilizados los formatos?
Los formatos de citas son insertados en ciertas páginas con contexto específico, y en las descargas.

El formato para el portal en general, será visible de manera predeterminada en la [página de Política de Uso](https://github.com/BioKIC/Symbiota/blob/master/includes/usagepolicy_template.php).

Los formatos para la colección serán insertados en cada [página de Perfil de Colección](https://github.com/BioKIC/Symbiota/blob/master/collections/misc/collprofiles.php), dependiendo si la colección está publicada en GBIF o no. 

![neon-biorepo-coll-citation.jpg](/symbiota-docs/images/neon-biorepo-coll-citation.jpg)
*Ejemplo de una página de perfil de una colección que no ha sido publicada en GBIF en [el Portal de Datos del Biorrepositorio NEON](https://biorepo.neonscience.org/portal/collections/misc/collprofiles.php?collid=50).*

![neon-biorepo-coll-gbif-citation.jpg](/symbiota-docs/images/neon-biorepo-coll-gbif-citation.jpg)
*Ejemplo de una página de perfil de una colección que está publicada en GBIF en el [Portal de Datos del Biorrepositorio NEON](https://biorepo.neonscience.org/portal/collections/misc/collprofiles.php?collid=39).*

El formato de cita para conjuntos de datos será insertado en cada [página de Conjunto de Datos](https://github.com/BioKIC/Symbiota/blob/master/collections/datasets/public.php).

Todos los formatos pueden ser incluidos, uno a la vez, en el archivo [`CITEME.txt`](https://github.com/BioKIC/Symbiota/blob/master/classes/DwcArchiverCore.php) incluido con el paquete descargado de un portal Symbiota, dependiendo del contexto en el cual el paquete fue solicitado. Por ejemplo, descargar los resultados de una búsqueda incluiráun archivo `CITEME.txt` que contendrá el formato `citationportal.php`. Por otro lado, al descargar un DwCA de la página de una colección que está publicada en GBIF, incluirá el formato `citationgbif.php`. Este comportamiento fue diseñado para informar a los usuarios de una mejor manera acerca del origen de sus datos. 

![neon-biorepo-citeme.jpg](/symbiota-docs/images/neon-biorepo-citeme.jpg)
*Ejemplo de un archivo `CITEME.txt` incluido en un DwCA descargado desde el [Portal de Datos del Biorrepositorio NEON](https://biorepo.neonscience.org/).*


### Activar el formato de uso
Para asegurarse que su portal use los formatos de cita, todo lo que debe hacer es tener una copia de cada plantilla de citas, y remover la ruta `_template` del nombre del archivo.

### Personalizando formatos
{{< notice note >}}
  Por favor notar que los formatos de cita deberían incluir únicamente formato de texto plano y/o PHP. No debe incluirse formato HTML en los formatos porque este es usado en distinto contexto.
{{</ notice >}}

Para personalizar cada formato, abra las copias de las plantillas y haga los cambios deseados. Guárdelos. Como las copias de las plantillas (sin la ruta `_template` en el nombre del archivo) no serán rastreadas por Git, no serán sobreescritas por futuras versiones.

### Widget de GBIF 
La página del Perfil de la Colección (`[root]/collections/misc/collprofiles.php`) ha sido actualizada para incluir cada formato apropiado de cita (si no está publicada en GBIF, se incluirá el formato `citationcollection.php` de forma predeterminada; si está publicada en GBIF, se incluirá el formato `citationgbif.php`). 

Si una colección ha sido publicada en GBIF, la página incluirá el [widget de citas de GBIF](https://www.gbif.org/article/1E6v02SFQyhupvB7JqDXPN/citation-widget#:~:text=GBIF%20maintains%20an%20ongoing%20literature,citation%20feed%20into%20external%20websites.) usando la clave específica de GBIF para la colección.

![neon-biorepo-coll-gbif-widget.jpg](/symbiota-docs/images/neon-biorepo-coll-gbif-widget.jpg)
*Ejemplo de un widget de GBIF widget añadido al [perfil de una colección en el Portal de Datos del Biorrepositorio NEON](https://biorepo.neonscience.org/portal/collections/misc/collprofiles.php?collid=39).*


### Dependencias
Para colecciones que publican en GBIF, instrucciones para el formato específico de GBIF para citar datos, pueden ser buscadas con [uses GBIF's API v1](https://www.gbif.org/developer/summary) para encontrar información de la colección (como `gbiftitle` and `DOI`).]
