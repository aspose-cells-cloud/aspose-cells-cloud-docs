---
title: "Obtener MinDataRow de una hoja de cálculo de Excel"
type: docs
url: /get-mindatarow-from-excel-worksheet/
weight: 90
keywords: "Aspose Cells, MinDataRow, API de Excel, SDK en la nube"
description: "Recuperar el índice de la fila de datos mínima de una hoja de cálculo utilizando la API de Aspose.Cells Cloud v3.0. Incluye el patrón de solicitud, parámetros, ejemplo de cURL, ejemplo de respuesta, códigos de estado y fragmentos de SDK."
ArticleTitle: "Obtener MinDataRow de una hoja de cálculo de Excel – Aspose.Cells Cloud API"
---

El endpoint **Get MinDataRow** de la **API de Aspose.Cells Cloud v3.0** devuelve el índice de la primera fila que contiene datos en una hoja de cálculo especificada. Esta operación requiere un token de acceso válido (autenticación Bearer) y el parámetro de consulta `cellOrMethodName` establecido en `mindatarow`.

**Versión de la API: 3.0**

### Ejemplo de cURL

La solicitud utiliza el método HTTP GET. Reemplace los marcadores de posición `{fileName}` y `{sheetName}` con los nombres reales del libro y la hoja de cálculo.

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/mindatarow?cellOrMethodName=mindatarow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Parámetros de la solicitud**

| Parámetro          | Ubicación | Tipo   | Obligatorio | Descripción                                                   |
|--------------------|-----------|--------|-------------|---------------------------------------------------------------|
| `fileName`         | Ruta      | string | Sí          | Nombre del libro de Excel (incluyendo la extensión).         |
| `sheetName`        | Ruta      | string | Sí          | Nombre de la hoja de cálculo dentro del libro.               |
| `cellOrMethodName` | Consulta  | string | Sí          | Debe establecerse en `mindatarow` para invocar esta operación. |

**Ejemplo de respuesta**

```json
{
  "MinDataRow": 5
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                       |
|--------|-----------------------------|---------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante. |
| 413    | Payload demasiado grande    | El archivo cargado excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

### Ejemplos de SDK

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK gestiona los detalles de bajo nivel, lo que le permite centrarse en la lógica de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante varios SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "85f2a886ba296b8abf640c0638b4eec1" >}}

{{< /tab >}}

{{< /tabs >}}

**Consulte también**

- [Obtener MaxDataRow](https://docs.aspose.cloud/cells/get-maxdatarow-from-excel-worksheet/)
- [Obtener MinColumn](https://docs.aspose.cloud/cells/get-mincolumn-from-excel-worksheet/)
- [Obtener MaxColumn](https://docs.aspose.cloud/cells/get-maxcolumn-from-excel-worksheet/)