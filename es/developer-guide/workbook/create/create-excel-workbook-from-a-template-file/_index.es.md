---
title: Cómo crear un libro de trabajo Excel con un archivo de plantilla
second_title: Aspose.Cells Cloud Documen
linktitle: plantilla
type: docs
url: /es/workbook/create/template-file/
aliases: [/create-excel-workbook-from-a-template-file/,/workbook/new-from-a-template-file/]
keywords: How to create an Excel workbook with a smart marker template
description: Aspose.Cells Cloud REST API cómo crear un libro de trabajo Excel a partir de una plantilla de marcador inteligente. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift
weight: 30
---
Este REST API indica crear `workbook` a partir de un `template file`.

**Parámetro de consulta**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|archivo de plantilla|cadena||
|archivo de datos|cadena||
|esEscribirOver|cadena| verdadero Falso|
|carpeta|cadena|Carpeta original del libro de trabajo.|
|NombreDeAlmacenamiento|cadena|Nombre de almacenamiento.|

**Parámetro del cuerpo de la solicitud**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|datos|archivo||


## DESCANSO API

|**API**|**Tipo**|**Descripción**|**Enlace arrogante**|
|:- |:- |:- |:- |
|/celdas/{nombre}|PONER|Cree un nuevo libro de trabajo Excel a partir de un archivo de plantilla|[PutWorkbookCreate](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate)|

 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

 Puedes usar**cURL** herramienta de línea de comandos para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo hacer llamadas a Cloud API con cURL.


{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&dataFile=Sample_Data.xml&isWriteOver=true" -H "accept: application/json" -H "x-aspose-client: Containerize.Swagger"


```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{
  "Status": "string",
  "Workbook": {
    "FileName": "string",
    "Links": [
      {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Names": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Settings": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "IsWriteProtected": "string",
    "IsProtected": "string",
    "IsEncryption": "string",
    "Password": "string"
  }
}

```

{{< /tab >}}

{{< /tabs >}}


## Familia SDK de la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se ocupa de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor, echa un vistazo a la[repositorio GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de Cloud.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:


{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "1ba81e1c8c3b8ffe85019434a1cbb5e8" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "3e47ddd0f0cb006c4311790d67c21a74" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PutWorkbookCreate-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-create_new_workbook-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "CreateExcelWorkbookFromTempateFile.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-CreateWorkbookFromTemplate-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-CreateWorkbookFromTemplate-create-empty-workbook-from-template.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-CreateWorkbookFromTemplate-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "0828352a30b729404dd415c5ceed5615" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "046b2a6af4e89e88b75a417ca3862e41" >}}

{{< /tab >}}

{{< /tabs >}}
