---
title: "Obtener MinColumn de una hoja de cálculo de Excel"
type: docs
url: /get-mincolumn-from-excel-worksheet/
weight: 100
keywords: Excel, Aspose.Cells Cloud, REST API, Obtener MinColumn, Hoja de cálculo, SDK, API en la nube
description: Recuperar el índice mínimo de columna que contiene datos en una hoja de cálculo de un archivo de Excel mediante la API REST de Aspose.Cells Cloud.
ArticleTitle: "Obtener MinColumn de una hoja de cálculo de Excel - Aspose.Cells Cloud API"
---

Esta API REST devuelve el índice mínimo de columna que contiene datos en una hoja de cálculo de Excel cuando el parámetro `cellOrMethodName` se establece en `mincolumn`.

- **Ejemplo de cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mincolumn" \
     -H "Authorization: Bearer <SU_TOKEN_DE_ACCESO>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**Detalles de la solicitud**

| Parámetro | Tipo | Obligatorio | Descripción |
|-----------|------|-------------|-------------|
| `cellOrMethodName` | string | Sí | Valor fijo `mincolumn` para indicar la operación. |
| `folder` | string | No | Ruta a la carpeta que contiene el libro de cálculo (si no es la carpeta raíz). |
| `storageName` | string | No | Nombre del almacenamiento en la nube de Aspose que se utilizará. |

**Detalles de la respuesta**

La API devuelve un objeto JSON con una única propiedad:

```json
{
  "MinColumn": integer   // Índice en base cero de la columna más a la izquierda que contiene datos.
}
```

Códigos de estado HTTP típicos:

- **200 OK** – Solicitud correcta, devuelve el valor de `MinColumn`.  
- **401 Unauthorized** – Token de autenticación ausente o no válido.  
- **404 Not Found** – El libro de cálculo, la hoja de cálculo o el rango de celdas especificados no existen.  
- **500 Internal Server Error** – Error inesperado en el servidor.

- **Uso de los SDK de Aspose.Cells Cloud**

Utilizar un SDK es la forma más eficiente de desarrollar. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en la lógica de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "108bf3803d41abd988a29cdbd39aee44" >}}

{{< /tab >}}

{{< /tabs >}}
---