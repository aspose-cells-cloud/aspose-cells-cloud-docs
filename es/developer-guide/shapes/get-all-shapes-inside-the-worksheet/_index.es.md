---
title: Obtenga todas las formas en una hoja de trabajo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Get-al
type: docs
url: /es/shapes/get-all/
aliases: [/get-all-shapes-inside-the-worksheet/]
keywords: Get all shapes on an Excel workshee
description: Aspose.Cells Cloud REST API admite la obtención de todas las formas en una hoja de trabajo Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 10
---
Este REST API indica Obtener formas de hoja de trabajo
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino| nombre del documento.|
| nombre de la hoja| cadena| camino| nombre de la hoja de trabajo.|
| carpeta| cadena| consulta| Carpeta del documento.|
| nombredealmacenamiento| cadena| consulta| nombre del almacenamiento.|
 
 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShapes) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash

{

  "Shapes" : {

    "ShapeList" : [

      {

        "link" : {

          "Href" : "/0",

          "Rel" : "self",

          "Type" : null,

          "Title" : null

        }

      },

      {

        "link" : {

          "Href" : "/1",

          "Rel" : "self",

          "Type" : null,

          "Title" : null

        }

      },

      {

        "link" : {

          "Href" : "/2",

          "Rel" : "self",

          "Type" : null,

          "Title" : null

        }

      },

      {

        "link" : {

          "Href" : "/3",

          "Rel" : "self",

          "Type" : null,

          "Title" : null

        }

      }

    ],

    "link" : {

      "Href" : "http://api.aspose.com/v1.1/cells/sampleShapes.xlsx/worksheets/Sheet1/shapes",

      "Rel" : "self",

      "Type" : null,

      "Title" : null

    }

  },

  "Code" : 200,

  "Status" : "OK"

}
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Familia de SDK en la nube
 
 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor revisa el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de nube.
 
Los siguientes ejemplos de código demuestran cómo realizar llamadas a servicios web Aspose.Cells utilizando varios SDK:
 
 
{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-GetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example-GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "2118580a8c2f08f37269d89ff9f57781" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-GetWorksheetShapes.swift" >}}

{{< /tab >}}

{{< /tabs >}}
