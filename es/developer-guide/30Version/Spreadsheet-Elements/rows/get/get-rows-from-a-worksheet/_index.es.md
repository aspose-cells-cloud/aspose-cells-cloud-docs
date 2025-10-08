---
title: Obtener información de filas de una hoja de cálculo Excel
second_title: Documen
linktitle: Fila
type: docs
url: /es/rows/get/rows/
aliases: [/get-row-from-a-worksheet/]
keywords: Get rows info on an Excel workshee
description: Aspose.Cells Cloud REST API admite la obtención de filas en una hoja de cálculo Excel. El SDK admite varios lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 10
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Obtener información de filas de una hoja de cálculo Excel
---
Este REST API indica obtener información de filas en una hoja de cálculo Excel.

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
 
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino| El nombre del libro de trabajo.|
| nombreHoja| cadena| camino| El nombre de la hoja de trabajo.|
| carpeta| cadena| consulta| La carpeta workdook.|
| nombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRows) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{

  "Rows": {

    "MaxRow": 20,

    "RowsCount": 17,

    "RowsList": [

      {

        "link": {

          "Href": "/0",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/1",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/2",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/3",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/4",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/5",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/6",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/7",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/8",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/9",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/10",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/11",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/12",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/13",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/14",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/15",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/16",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/17",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/18",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/19",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/20",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/21",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/22",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/23",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/24",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      }

    ],

    "link": {

      "Href": "/test.xlsx/worksheets/Sheet1/cells/rows",

      "Rel": "self",

      "Title": null,

      "Type": null

    }

  },

  "Code": 200,

  "Status": "OK"

}
 
```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows" -H "accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Rows": {

    "MaxRow": 20,

    "RowsCount": 17,

    "RowsList": [

      {

        "link": {

          "Href": "/0",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/1",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/2",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/3",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/4",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/5",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/6",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/7",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/8",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/9",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/10",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/11",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/12",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/13",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/14",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/15",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/16",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/17",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/18",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/19",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/20",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/21",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/22",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/23",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/24",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      }

    ],

    "link": {

      "Href": "/test.xlsx/worksheets/Sheet1/cells/rows",

      "Rel": "self",

      "Title": null,

      "Type": null

    }

  },

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
