---
title: "Cambiar el estilo de celda en una hoja de cálculo de Excel"
type: docs
url: /es/change-cell-style-in-excel-worksheet/
weight: 30
keywords:
  - Aspose.Cells
  - Aspose.Cells Cloud
  - Excel
  - Estilo de celda
  - API REST
  - SDK en la nube
  - cURL
  - actualización de estilo de celda
  - API de Excel
description: "Aprenda cómo actualizar el estilo de una celda específica en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud, incluyendo ejemplos de solicitudes, respuestas y fragmentos de código SDK."
ArticleTitle: "Cambiar el estilo de celda en una hoja de cálculo de Excel – Guía de la API de Aspose.Cells Cloud"
---

Esta API REST actualiza el **estilo de celda** de un archivo de Excel.

## API PostUpdateWorksheetCellStyle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                           |
|----------------------|--------|-----------|-------------------------------------------------------|
| name                 | string | path      | Nombre del archivo del libro de trabajo.             |
| sheetName            | string | path      | Nombre de la hoja de cálculo.                        |
| cellName             | string | path      | Celda de destino (por ejemplo, **A1**).              |
| style                | object | body      | Objeto JSON que define la configuración de estilo que se aplicará a la celda. |
| folder               | string | query     | Carpeta que contiene el libro de trabajo.            |
| storageName          | string | query     | Nombre del almacenamiento donde se guarda el libro de trabajo. |

### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                              |
|--------|-----------------------------|----------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                           |
| 413    | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño.         |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                         |

## Cómo utilizar la API PostUpdateWorksheetCellStyle con SDK

### Especificación de la API PostUpdateWorksheetCellStyle

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetCellStyle) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. Reemplace `<jwt token>` por un token de acceso OAuth 2.0 válido obtenido desde el punto de autenticación de Aspose Cloud.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test_cells.xlsx/worksheets/Sheet3/cells/A1/style" \
-d '{ "BackgroundThemeColor": { "ColorType": "Text2", "Tint": 1 } }' \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "None"
    },
    "Name": null,
    "CultureCustom": null,
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "BottomBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "DiagonalDown" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "DiagonalUp" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "Horizontal" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "LeftBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "RightBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "TopBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "Vertical" }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/test_cells.xlsx/worksheets/Sheet3/cells/A1/style",
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

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar contra la API. Un SDK abstracte los detalles de bajo nivel para que pueda centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo llamar a los servicios web de Aspose.Cells mediante varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Consulte también:**  
- [Obtener el estilo de celda](https://docs.aspose.cloud/cells/get-cell-style/) – Recuperar el estilo actual de una celda.  
- [Actualizar el estilo de varias celdas](https://docs.aspose.cloud/cells/update-multiple-cells-style/) – Aplicar un estilo a un rango de celdas en una sola solicitud.  
---