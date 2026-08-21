---
title: "Obtener la última celda de una hoja de cálculo de Excel – Aspose.Cells Cloud API (v4.0)"
type: docs
url: /get-last-cell-of-excel-worksheet/
weight: 30
keywords: "Aspose.Cells, API de Excel, obtener última celda, hoja de cálculo, nube"
description: "Recuperar la dirección de la celda final de una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud v4.0. Incluye detalles de la solicitud, ejemplo de cURL, respuesta JSON y ejemplos de SDK."
ArticleTitle: "Obtener la celda final de una hoja de cálculo de Excel – Aspose.Cells Cloud API v4.0"
---

Esta API REST devuelve la **endcell** (celda final) de una hoja de cálculo de Excel cuando el parámetro `cellOrMethodName` se establece en `endcell`.

**Resumen**  
La operación **Get Last Cell** (Obtener última celda) devuelve la dirección de la última celda utilizada en una hoja de cálculo especificada. Es útil para determinar el rango efectivo de datos de una hoja sin necesidad de escanear todo el libro.

- **Ejemplo con cURL.**

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/endcell" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "F341",
    "Row": 340,
    "Column": 5,
    "Value": "<Más información>",
    "Type": "IsString",
    "Formula": "=HYPERLINK(SUBSTITUTE(HelpURLTemplate,\"xxxxxxxxxx\",[Help Topic]),\"<Más información>\")",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"TEXT-DECORATION: underline;FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">&lt;Más información&gt;</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Parámetros
| Parámetro            | Tipo   | Obligatorio | Descripción |
|----------------------|--------|-------------|-------------|
| `fileName`           | string | Sí          | Nombre del archivo de Excel almacenado en la nube. |
| `worksheetName`      | string | Sí          | Nombre de la hoja de cálculo desde la cual recuperar la última celda. |
| `cellOrMethodName`   | string | Sí          | Debe establecerse en **`endcell`** para invocar esta operación. |
| `folder` *(opcional)*| string | No          | Ruta de carpeta en la nube donde se encuentra el libro. |
| `storageName` *(opcional)*| string | No      | Nombre del almacenamiento. Si se omite, se utiliza el almacenamiento predeterminado. |

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o faltante. |
| 413    | Carga demasiado grande       | El archivo cargado excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

- **Utilizar los SDK de Aspose.Cells Cloud**

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetLastCellWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetLastCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_last_cell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetLastCellOfExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetLastCellWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

_Proximamente._

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetLastCellWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3cf3e145c223fd6f6f3d9f6377092db5" >}}

{{< /tab >}}

{{< /tabs >}}

Para otras operaciones relacionadas con la navegación de celdas, consulte los temas **[Obtener primera celda](/get-first-cell-of-excel-worksheet/)** y **[Obtener fila máxima](/get-max-row-of-worksheet/)**.