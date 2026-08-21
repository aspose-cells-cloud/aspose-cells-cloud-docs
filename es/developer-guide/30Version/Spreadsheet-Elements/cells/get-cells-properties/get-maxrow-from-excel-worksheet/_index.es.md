---
title: "Obtener MaxRow de una hoja de cálculo de Excel"
type: docs
url: /get-maxrow-from-excel-worksheet/
weight: 40
ArticleTitle: "Recuperar el número máximo de fila en una hoja de cálculo de Excel – API de Aspose.Cells Cloud"
keywords: "Aspose.Cells, Excel, MaxRow, API REST, SDK en la nube, hoja de cálculo, hoja de trabajo, GetMaxRow"
description: "Aprenda cómo recuperar el número máximo de fila en una hoja de cálculo de un archivo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye la sintaxis de la solicitud, el esquema de respuesta, ejemplos de SDK y notas de uso."
---

Esta API REST devuelve el **número máximo de fila** en una hoja de cálculo de Excel cuando el parámetro `cellOrMethodName` se establece en `maxrow`.

- **Ejemplo con cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxrow" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxRow": 1048576
}
```

{{< /tab >}}

{{< /tabs >}}

- **Uso de los SDK de Aspose.Cells Cloud**

Utilizar un SDK es la forma más eficiente de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel, permitiéndole centrarse en la lógica de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante varios SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "afcfd72b172e9c3e2d283a9ac059c8c7" >}}

{{< /tab >}}

{{< /tabs >}}

**Referencia de la API**

| Elemento | Detalles |
|--------|----------|
| **Método** | `GET` |
| **Punto final** | `/cells/{fileName}/worksheets/{sheetName}/cells/maxrow` |
| **Parámetros de ruta** | `fileName` – nombre del archivo de Excel (obligatorio) <br> `sheetName` – nombre de la hoja de cálculo (obligatorio) |
| **Parámetros de consulta** | `folder` – ruta de la carpeta en el almacenamiento (opcional) <br> `storageName` – nombre del almacenamiento (opcional) |
| **Respuesta correcta** | `200 OK` <br> ```json { "MaxRow": integer } ``` |
| **Respuestas de error** | `400 Bad Request` – parámetros inválidos <br> `401 Unauthorized` – error de autenticación <br> `404 Not Found` – archivo o hoja de cálculo no encontrado |

**Requisitos previos**

- Un token de autenticación válido de Aspose Cloud.  
- El libro de trabajo objetivo debe estar cargado en el almacenamiento de Aspose Cloud o ser accesible mediante una URL pública.  

**Notas**

- Esta operación está disponible en la versión **v3.0** de la API y posteriores.  
- El valor devuelto de `MaxRow` corresponde al índice más alto de fila utilizado (basado en 1). Para una hoja de cálculo en blanco, el valor suele ser `1`.  

Los siguientes ejemplos de SDK ilustran cómo invocar esta operación en distintos lenguajes de programación.  
---