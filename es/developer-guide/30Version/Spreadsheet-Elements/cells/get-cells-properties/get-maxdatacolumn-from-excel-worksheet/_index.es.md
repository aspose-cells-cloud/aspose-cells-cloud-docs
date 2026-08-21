---
title: "Aspose.Cells Cloud API – Obtener el MaxDataColumn de una hoja de cálculo de Excel (v3.0)"
type: docs
url: /get-maxdatacolumn-from-excel-worksheet/
weight: 70
keywords: "Aspose.Cells Cloud, Obtener MaxDataColumn, hoja de cálculo de Excel, API REST, v3.0, SDK"
description: "Recuperar el índice de columna más alto que contiene datos en una hoja de cálculo especificada mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye detalles de la solicitud, respuesta de ejemplo y ejemplos de SDK."
ArticleTitle: "Aspose.Cells Cloud API – Obtener el MaxDataColumn de una hoja de cálculo de Excel (v3.0)"
---

Esta API REST devuelve el índice máximo de columna de datos en una hoja de cálculo de Excel cuando el parámetro `cellOrMethodName` se establece en `maxdatacolumn`.

## **Ejemplo con cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxdatacolumn" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxDataColumn": 12
}
```

{{< /tab >}}

{{< /tabs >}}

**Detalles de la solicitud**  
- **Método HTTP:** `GET`  
- **Patrón de punto final:** `https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatacolumn`  
- **Parámetros de ruta:**  
  - `fileName` – Nombre del archivo de Excel (por ejemplo, `myWorkbook.xlsx`).  
  - `sheetName` – Nombre de la hoja de cálculo (por ejemplo, `Sheet1`).  
- **Encabezados:**  
  - `Authorization: Bearer <access_token>` (obligatorio)  
  - `Accept: application/json` (recomendado)  

**Parámetros**

| Parámetro | Ubicación | Tipo   | Obligatorio | Descripción |
|-----------|-----------|--------|-------------|-------------|
| `fileName` | Ruta      | string | Sí          | El nombre del archivo de Excel almacenado en el almacenamiento en la nube. |
| `sheetName` | Ruta    | string | Sí          | La hoja de cálculo de la que se desea obtener la columna de datos máxima. |
| `cellOrMethodName` | Ruta | string | Sí | Debe establecerse en `maxdatacolumn` para invocar esta operación. |

**Respuestas**

| Código de estado | Descripción                                      | Ejemplo de carga útil |
|------------------|--------------------------------------------------|------------------------|
| 200              | Correcto – devuelve el índice de la columna de datos máxima. | `{ "MaxDataColumn": 12 }` |
| 401              | No autorizado – token de acceso inválido o ausente. | `{ "error": "Invalid authentication." }` |
| 404              | No encontrado – el archivo o la hoja de cálculo no existen. | `{ "error": "Resource not found." }` |
| 500              | Error interno del servidor – condición inesperada. | `{ "error": "Server error." }` |

**Control de errores**  
Si la solicitud falla, revise el código de estado HTTP y el mensaje `error` en el cuerpo de la respuesta. Asegúrese de que el token de acceso sea válido y de que el archivo y la hoja de cálculo especificados existan en su almacenamiento de Aspose Cloud.

- **Utilizar los SDK de Aspose.Cells Cloud**

Utilizar un SDK es la forma más eficiente de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "126f68818f671a2f6087ee334726c454" >}}

{{< /tab >}}

{{< /tabs >}}