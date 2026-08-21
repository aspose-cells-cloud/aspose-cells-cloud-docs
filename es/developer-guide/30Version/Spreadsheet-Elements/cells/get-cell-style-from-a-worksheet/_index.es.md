---
title: "Obtener el estilo de una celda en una hoja de cálculo – Aspose.Cells Cloud API"
type: docs
url: /es/get-cell-style-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells, Excel, API REST, estilo de celda, hoja de cálculo, SDK en la nube, documentación de API"
description: "Aprenda cómo recuperar el estilo de una celda específica en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud v3. Incluye ejemplo con cURL, esquema de respuesta, códigos de estado y fragmentos de SDK."
ArticleTitle: "Obtener el estilo de una celda en una hoja de cálculo con la API de Aspose.Cells Cloud – Guía detallada"
---

Utilice esta API REST para recuperar el **estilo** de una celda en una hoja de cálculo de Excel.

## API GetWorksheetCellStyle

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud


| Nombre del parámetro | Tipo   | Ubicación | Descripción                                    |
| --------------------- | ------ | --------- | ---------------------------------------------- |
| name                  | string | path      | Nombre del documento de Excel.                |
| sheetName             | string | path      | Nombre de la hoja de cálculo.                 |
| cellName              | string | path      | Dirección de la celda (por ejemplo, A1).      |
| folder                | string | query     | Carpeta que contiene el archivo.              |
| storageName           | string | query     | Nombre del almacenamiento a utilizar.         |


### **Respuesta**

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
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
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                                              |
| 413    | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño.                             |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                                            |

**Respuestas de error**  
Las cargas útiles típicas de error para este endpoint siguen el formato estándar de errores de Aspose.Cells. Por ejemplo, un error 400 (Solicitud incorrecta) devuelve:

```json
{
  "Code": 400,
  "Message": "Parámetro no válido 'cellName'.",
  "Description": "El nombre de celda proporcionado no tiene un formato A1 válido."
}
```

Del mismo modo, un error 401 (No autorizado) devuelve:

```json
{
  "Code": 401,
  "Message": "Fallo en la autenticación.",
  "Description": "El token JWT falta o no es válido."
}
```

## Cómo utilizar la API GetWorksheetCellStyle con SDK

### Especificación de la API GetWorksheetCellStyle


La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle) define una interfaz de programación públicamente accesible y permite llevar a cabo interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/a1/style" \
  -X GET \
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
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
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
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
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

## Esquema de respuesta

| Campo                    | Tipo    | Descripción                                                               |
| ------------------------ | ------- | ------------------------------------------------------------------------- |
| **Style**                | object  | Contenedor de todas las propiedades relacionadas con el estilo de la celda. |
| Style.Font               | object  | Configuración de fuente (nombre, tamaño, color, indicadores de estilo).   |
| Style.Font.Color         | object  | Valores de color RGBA para la fuente.                                     |
| Style.Font.IsBold        | boolean | `true` si la fuente está en negrita.                                      |
| Style.Font.IsItalic      | boolean | `true` si la fuente está en cursiva.                                      |
| Style.Font.IsStrikeout   | boolean | `true` si la fuente tiene tachado.                                        |
| Style.Font.IsSubscript   | boolean | `true` si la fuente es subíndice.                                         |
| Style.Font.IsSuperscript | boolean | `true` si la fuente es superíndice.                                       |
| Style.Font.Name          | string  | Nombre de la familia de fuentes (por ejemplo, **Calibri**).               |
| Style.Font.Size          | number  | Tamaño de fuente en puntos.                                               |
| Style.Font.Underline     | string  | Estilo de subrayado (por ejemplo, **Single**).                            |
| Style.IsLocked           | boolean | Indica si la celda está protegida contra edición.                         |
| Style.IsTextWrapped      | boolean | `true` si el ajuste de texto está habilitado.                             |
| Style.IsGradient         | boolean | `true` si se ha aplicado un relleno con degradado.                        |
| Style.Pattern            | string  | Nombre del patrón de relleno (por ejemplo, **None**).                     |
| Style.BorderCollection   | array   | Lista de objetos de borde que definen estilo de línea, color y tipo de borde. |
| Style.BackgroundColor    | object  | Valores RGBA para el fondo de la celda.                                   |
| Style.ForegroundColor    | object  | Valores RGBA para el primer plano de la celda.                            |
| …                        | …       | _(Otros campos siguen el mismo patrón definido en la referencia de la API.)_ |

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante distintos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Consulte también**  
- [Establecer el estilo de celda](https://apireference.aspose.cloud/cells/#/Cells/SetWorksheetCellStyle)  
- [Obtener el valor de celda](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)
---