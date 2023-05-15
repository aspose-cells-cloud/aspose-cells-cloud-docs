---
title: Importar imagen a la hoja de trabajo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importar imagen
type: docs
url: /es/import/picture/
aliases: [/import-picture-into-excel-worksheet/,/import-picture-into-worksheet/,/import-data/picture/]
keywords: Import picture into Excel files
description: Aspose.Cells Cloud REST API admite la importación de imágenes en archivos Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift
weight: 19
---
Este REST API `import picture data` en Excel hoja de trabajo.

La solicitud es una solicitud HTTP con contenido de varias partes (ver[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)o[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del contenido de varias partes contiene los datos de ImportPictureOption y la segunda contiene un archivo de datos.

## RESET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```


Los parámetros importantes se describen en la siguiente tabla:


**Opción de imagen de importación**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| fila superior izquierda| En t||
|Columna superior izquierda| En t||
| FilaInferiorDerecha| En t||
| Columna inferior derecha| En t||
| Nombre del archivo| cadena||
| Datos| Cadena||
| DestinationWorksheet| cadena| nombre de la hoja de trabajo de destino.|
| EsInsertar| cadena| verdadero Falso.|
| Tipo de datos de importación| cadena|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture.|
| Fuente| Origen del archivo| Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.|


**Ejemplo**


## Familia SDK de la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se ocupa de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor, echa un vistazo a la[repositorio GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de Cloud.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}


{{< /tab >}}

{{< /tabs >}}

