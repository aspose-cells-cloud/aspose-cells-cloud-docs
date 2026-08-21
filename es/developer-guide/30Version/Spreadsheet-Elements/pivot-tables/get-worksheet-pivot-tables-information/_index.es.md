---
title: "Obtener todas las tablas dinámicas en una hoja de cálculo de Excel"
second_title: "Document"
linktitle: Obtener todas
type: docs
url: /es/pivot-tables/get-all/
aliases: [  /es/get-worksheet-pivot-tables-information/ ]
keywords: "obtener todas las tablas dinámicas, API de Aspose.Cells Cloud, Excel PivotTable, API REST"
description: "Recuperar todas las tablas dinámicas de una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud. Incluye el punto final, los parámetros, los pasos de autenticación, ejemplos con cURL y con SDK para la API de tablas dinámicas."
weight: 20
ArticleTitle: "Obtener todas las tablas dinámicas en una hoja de cálculo de Excel – API de Aspose.Cells Cloud"
---

Una **tabla dinámica (PivotTable)** es una herramienta de resumen de datos en Excel que le permite reorganizar y analizar grandes conjuntos de datos. Esta API REST recupera información sobre **todas** las tablas dinámicas en una hoja de cálculo especificada.

## Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                      |
| -------------------- | ------ | --------- | ------------------------------------------------ |
| name                 | string | path      | Nombre del documento de Excel.                  |
| sheetName            | string | path      | Nombre de la hoja de cálculo.                   |
| folder               | string | query     | Carpeta donde se almacena el documento.         |
| storageName          | string | query     | Nombre del servicio de almacenamiento.          |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTables) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

### Solicitud

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

### Respuesta

{{< tab tabNum="2" >}}

```json
{
  "PivotTables": {
    "PivotTableList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Respuestas de error

| Código HTTP | Descripción                                                      | Ejemplo de carga JSON                                         |
| ----------- | ---------------------------------------------------------------- | ------------------------------------------------------------- |
| 400         | Solicitud incorrecta: falta un parámetro obligatorio.           | `{ "Code": "400", "Message": "Missing required parameter." }` |
| 401         | No autorizado: token inválido o ausente.                         | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404         | No encontrado: el libro, la hoja o la tabla dinámica no existen. | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500         | Error interno del servidor: condición inesperada en el servidor.| `{ "Code": "500", "Message": "Server error." }`               |

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK gestiona los detalles de bajo nivel para que usted se enfoque en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTables-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformation.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTables-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTables-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "6b30a17927feeb2899283e4dbe566c42" >}}
{{< /tab >}}

{{< /tabs >}}