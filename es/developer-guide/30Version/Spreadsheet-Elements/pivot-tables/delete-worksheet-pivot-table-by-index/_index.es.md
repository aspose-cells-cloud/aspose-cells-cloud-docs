---
title: "Eliminar una tabla dinámica en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: Eliminar
type: docs
url: /es/pivot-tables/delete/
aliases: [/delete-worksheet-pivot-table-by-index/]
keywords: "Aspose.Cells, tabla dinámica, eliminar, Excel, API REST"
description: "Eliminar una tabla dinámica de una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye el formato de solicitud, un ejemplo con cURL, códigos de error y fragmentos de SDK para C#, Java, Python y Node.js."
weight: 70
ArticleTitle: "Cómo eliminar una tabla dinámica en una hoja de cálculo de Excel con Aspose.Cells Cloud"
---

Esta API REST elimina una tabla dinámica de una hoja de cálculo por su índice.

**Requisitos previos**: debe disponer de un token de acceso JWT válido para Aspose.Cells Cloud y el archivo de Excel de destino debe estar almacenado en una ubicación compatible con el almacenamiento. Asegúrese de especificar correctamente el nombre del archivo, el nombre de la hoja de cálculo y los detalles del almacenamiento antes de invocar la API.

Las tablas dinámicas son una forma potente de resumir datos en una **hoja de cálculo de Excel**. Con Aspose.Cells Cloud, puede eliminar programáticamente una tabla dinámica no deseada mediante una única solicitud HTTP DELETE. Esta operación resulta ideal cuando necesita limpiar hojas de cálculo, automatizar la generación de informes o integrar la manipulación de Excel en sus aplicaciones.

## API DeleteWorksheetPivotTable

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                           |
| --------------------- | ------- | --------- | ----------------------------------------------------- |
| name                  | string  | path      | Nombre del documento de Excel.                       |
| sheetName             | string  | path      | Nombre de la hoja de cálculo que contiene la tabla dinámica. |
| pivotTableIndex       | integer | path      | Índice de base cero de la tabla dinámica que se va a eliminar. |
| folder                | string  | query     | Ruta a la carpeta donde se almacena el documento.    |
| storageName           | string  | query     | Nombre del servicio de almacenamiento.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTable) define una interfaz de programación pública accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Ejemplo de respuesta**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

La respuesta sigue un esquema JSON simple:

```json
{
  "Code": integer,   // Código de estado tipo HTTP de la operación
  "Status": string   // Descripción textual, por ejemplo, "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Manejo de errores

A continuación se muestran los códigos de estado de respuesta comunes:

| Estado HTTP | Descripción                                                         |
| ----------- | ------------------------------------------------------------------- |
| 400         | Solicitud incorrecta: parámetros faltantes o no válidos.           |
| 401         | No autorizado: token JWT no válido o ausente.                       |
| 404         | No encontrado: el archivo, la hoja de cálculo o la tabla dinámica no existen. |
| 500         | Error interno del servidor: se produjo una condición inesperada.   |

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-DeleteWorksheetPivotTableIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteWorksheetPivotTablesByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-DeleteWorksheetPivotTableIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-DeleteWorksheetPivotTableIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8798eca5f30bf41a4675b83583a72ec3" >}}

{{< /tab >}}

{{< /tabs >}}
---