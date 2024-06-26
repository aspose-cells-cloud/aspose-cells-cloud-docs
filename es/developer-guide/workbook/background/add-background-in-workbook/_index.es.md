﻿---
title: Agregar fondo en Workboo
second_title: Aspose.Cells Cloud Documen
linktitle: Anuncio
type: docs
url: /es/workbook/background/add/
aliases: [/add-background-in-workbook/,/workbook/add-background/]
keywords: Add background on an Excel workbook
description: Aspose.Cells Cloud REST API admite agregar fondo en un libro de trabajo Excel en un archivo Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 160
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdwon, Agregar fondo en el libro de trabajo
---
Este REST API indica agregar `background` en un libro de trabajo Excel.


**Parámetro de consulta**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|picPath|cadena|posición de la imagen.|
|carpeta|cadena|Carpeta del libro de trabajo original.|
|nombredealmacenamiento|cadena|Nombre del almacenamiento.|

**Solicitar parámetro del cuerpo**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|archivo de datos| archivo de datos|El archivo de datos se guarda en el cuerpo de la solicitud.|

## DESCANSO API

|**API**|**Tipo**|**Descripción**|**Enlace de recursos**|
|:- |:- |:- |:- |
|/celdas/{nombre}/fondo|PONER|Agregar fondo en el archivo de Excel|[PonerLibro De TrabajoFondo](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground)|

 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

 Puedes usar**cURL**Herramienta de línea de comandos para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

	"Code": 200,

 	"Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}


## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor revisa el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Android" tabName5="Perl" tabName6="Ruby" tabName7="PHP" tabName8="Node.js" tabName9="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "4f5e06ec874b8b698dfa0e5359c85f96" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "b47350fc841e7c7e8889b1f57723ad94" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "bef09b36e0e7b769022bd810898dbd73" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "a984b922e2a7373755fb877e8754452b" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "7b9fa1a76c49c164d034342a2a59d4e0" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "a56d3fa3fff9c61191ee3e869ec51cdd" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "4a63cab36bb9f03e4e58bc30267b60b8" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "4009896954c23f8a1394b3757a30ee9d" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d3b449b5e5e2cdbb25da9e8de37bdccc" >}}

{{< /tab >}}

{{< /tabs >}}
