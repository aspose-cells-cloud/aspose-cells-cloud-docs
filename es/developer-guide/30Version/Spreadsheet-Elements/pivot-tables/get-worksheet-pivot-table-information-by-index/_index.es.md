---
title: "Obtener una tabla dinámica en una hoja de cálculo de Excel"
second_title: "Document"
linktype: Get
type: docs
url: /es/pivot-tables/get/
aliases: [  /es/get-worksheet-pivot-table-information-by-index/ ]
keywords: "Aspose.Cells, tabla dinámica, Excel, API REST, obtener tabla dinámica de hoja de cálculo"
description: "Recuperar una tabla dinámica desde una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye sintaxis de solicitud, parámetros, autenticación, esquema de respuesta, manejo de errores y ejemplos de SDK."
weight: 10
ArticleTitle: "Obtener una tabla dinámica en una hoja de cálculo de Excel"
---

Esta API REST recupera la información de la **tabla dinámica** de una hoja de cálculo mediante su índice.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivottableIndex}
```

### Parámetros de solicitud

| Nombre del parámetro  | Tipo    | Ubicación | Descripción                                                |
| --------------------- | ------- | --------- | ---------------------------------------------------------- |
| **name**              | string  | path      | El nombre del archivo de Excel.                            |
| **sheetName**         | string  | path      | El nombre de la hoja de cálculo que contiene la tabla dinámica. |
| **pivottableIndex**   | integer | path      | Índice de base cero de la tabla dinámica en la hoja de cálculo. |
| **folder**            | string  | query     | La carpeta donde se almacena el documento.                 |
| **storageName**       | string  | query     | El nombre del almacenamiento de Aspose Cloud.              |

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "PivotFilters": [
    {
      "AutoFilter": {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "FilterColumns": [
          {
            "FieldIndex": 0,
            "FilterType": "string",
            "MultipleFilters": {
              "MatchBlank": true,
              "MultipleFilterList": [{}]
            },
            "ColorFilter": {
              "FilterByFillColor": "string",
              "Pattern": "string",
              "Color": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "ForegroundColorColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "BackgroundColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              }
            },
            "CustomFilters": [
              {
                "FilterOperatorType": "string"
              }
            ],
            "DynamicFilter": {
              "DynamicFilterType": "string"
            },
            "IconFilter": {
              "IconId": 0,
              "IconSetType": "string"
            },
            "Top10Filter": {
              "Criteria": "string",
              "IsPercent": true,
              "IsTop": true,
              "Items": 0
            },
            "VisibleDropdown": "string"
          }
        ],
        "Range": "string",
        "Sorter": {
          "CaseSensitive": true,
          "HasHeaders": true,
          "KeyList": [
            {
              "Key": 0,
              "SortOrder": "string",
              "CustomList": "string"
            }
          ],
          "SortLeftToRight": true
        }
      },
      "EvaluationOrder": 0,
      "FieldIndex": 0,
      "FilterType": "string",
      "MeasureFldIndex": 0,
      "MemberPropertyFieldIndex": 0,
      "Name": "string",
      "Value1": "string",
      "Value2": "string"
    }
  ]
}
```

**Esquema de respuesta**

| Campo           | Tipo    | Descripción                                          |
|-----------------|---------|------------------------------------------------------|
| Status          | string  | Texto con el estado de la operación (por ejemplo, “OK”). |
| PivotFilters    | array   | Colección de definiciones de filtros dinámicos.     |
| └─ AutoFilter   | object  | Detalles del filtro automático aplicado a la tabla dinámica. |
|    └─ link      | object  | Información del hipervínculo del filtro.            |
|    └─ FilterColumns | array | Configuraciones individuales de filtro por columna. |
|    └─ Range     | string  | Rango de celdas al que se aplica el filtro.         |
|    └─ Sorter    | object  | Configuración de ordenación para los datos filtrados. |
| (los demás campos anidados siguen la misma estructura que se muestra en el ejemplo JSON) |

{{< /tab >}}

{{< /tabs >}}

### Manejo de errores

La API sigue los códigos de estado HTTP estándar. Las respuestas típicas incluyen:

| Código de estado | Significado                                                      | Ejemplo JSON (error)                              |
| ---------------- | ---------------------------------------------------------------- | ------------------------------------------------- |
| 200              | Correcto: se devuelve la tabla dinámica                         | —                                                 |
| 401              | No autorizado: token inválido o ausente                          | `{"code":401,"message":"Invalid access token."}`  |
| 404              | No encontrado: el archivo, la hoja de cálculo o el índice de la tabla dinámica no existen | `{"code":404,"message":"Pivot table not found."}` |
| 500              | Error del servidor: condición inesperada                        | `{"code":500,"message":"Internal server error."}` |

**Notas:** La API admite archivos de Excel de hasta 150 MB y funciona con formatos de Excel 2007–2021. Asegúrese de que el nombre de la hoja de cálculo distinga entre mayúsculas y minúsculas.

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que usted se enfoque en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTableByIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetWorksheetPivotInfoByIndex-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformationByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTableByIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-pivottables-GetPivotTableIndexWorksheet-get-pivottable-index-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTableByIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3ff21d138764aa6b6fd51fbaab8cdb95" >}}

{{< /tab >}}

{{< /tabs >}}