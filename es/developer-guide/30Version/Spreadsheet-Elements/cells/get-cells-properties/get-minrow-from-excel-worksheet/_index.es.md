---
title: "Obtener MinRow de una hoja de cálculo de Excel – Referencia de la API de Aspose.Cells Cloud"
type: docs
url: /es/get-minrow-from-excel-worksheet/
weight: 80
keywords: "Aspose.Cells, GetMinRow, hoja de cálculo de Excel, API REST, índice de fila mínima, SDK en la nube"
description: "Aprenda cómo recuperar el índice de fila mínima de una hoja de cálculo mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye la solicitud completa con cURL con autenticación, esquema de respuesta y ejemplos de SDK para múltiples lenguajes."
ArticleTitle: "Obtener MinRow de una hoja de cálculo de Excel – Referencia de la API de Aspose.Cells Cloud"
---

Esta API REST devuelve el índice de fila mínima en una hoja de cálculo de Excel cuando el parámetro `cellOrMethodName` se establece en `minrow`. Este punto final puede utilizarse para determinar la primera fila no vacía (basada en índice cero) en una hoja de cálculo determinada.

- **Ejemplo con cURL:**

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/minrow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "MinRow": 0
}
```

{{< /tab >}}

{{< /tabs >}}

**Solicitud**

```
GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/minrow
```

| Propiedad         | Tipo   | Obligatorio | Descripción                                           |
|-------------------|--------|-------------|-------------------------------------------------------|
| `fileName`        | string | Sí          | Nombre del libro (por ejemplo, `myWorkbook.xlsx`).  |
| `sheetName`       | string | Sí          | Hoja de cálculo objetivo (por ejemplo, `Sheet1`).    |
| `cellOrMethodName`| string | Sí          | Valor fijo `minrow`.                                  |
| `folder`          | string | No          | Ruta de la carpeta en el almacenamiento en la nube.  |
| `storageName`     | string | No          | Nombre del almacenamiento si se usa uno no predeterminado. |

**Respuesta**

El servicio devuelve un objeto JSON que contiene la propiedad `MinRow`, que indica el índice de la primera fila no vacía (basado en índice cero).

| Estado HTTP | Significado                                     |
|-------------|-------------------------------------------------|
| 200         | Éxito – carga útil JSON con `MinRow`.          |
| 401         | No autorizado – token no válido o ausente.     |
| 404         | Libro o hoja de cálculo no encontrados.        |
| 500         | Error interno del servidor.                    |

El valor `MinRow` resulta útil cuando se necesita localizar rápidamente el punto de inicio de los datos en una hoja.

- **Utilizar los SDK de Aspose.Cells Cloud**

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9497c39cde5cecb6709ff5feb2ab2b8" >}}

{{< /tab >}}

{{< /tabs >}}