---
title: "Actualizar el estilo de varias celdas – Referencia de la API de Aspose.Cells Cloud (v3.0)"
type: docs
url: /es/update-multiple-cells-style/
weight: 20
keywords: ["Aspose.Cells", "actualizar estilo de varias celdas", "API de estilo de celdas Excel", "SDK en la nube", "API REST", "ejemplo cURL", "solicitud JSON", "autenticación JWT"]
description: "Aprenda cómo actualizar el estilo de un rango de celdas en un libro de Excel usando la API REST de Aspose.Cells Cloud v3.0. Incluye el endpoint, el método HTTP, los parámetros, ejemplos con cURL y SDK, autenticación, manejo de errores e información de versión."
ArticleTitle: "Actualizar el estilo de varias celdas – Referencia de la API de Aspose.Cells Cloud (v3.0)"
---

## API REST

Esta API REST establece el **estilo** para un rango de celdas en un libro de Excel.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
```

## Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción |
|----------------------|--------|-----------|-------------|
| **name**             | string | path      | Nombre del libro. |
| **sheetName**        | string | path      | Nombre de la hoja de cálculo. |
| **range**            | string | query     | Rango de celdas (por ejemplo, `A1:A10`). |
| **style**            | object | body      | Objeto JSON que define el estilo que se aplicará. |
| **folder**           | string | query     | Carpeta que contiene el libro. |
| **storageName**      | string | query     | Nombre del almacenamiento. |

#### Objeto style
El objeto JSON `style` representa el formato de celda. Puede contener cualquiera de las siguientes propiedades opcionales:

- **Font** – Configuración de fuente (`Name`, `Size`, `IsBold`, `IsItalic`, `Color`, etc.).  
- **BackgroundColor** – Color de fondo en formato ARGB.  
- **ForegroundColor** – Color de primer plano en formato ARGB.  
- **Name**, **CultureCustom**, **Custom** – Metadatos adicionales del estilo.

## **Respuesta**

Devuelve un `CellCloudResponse`.

- **Descripción general de los campos de respuesta**

| Campo             | Tipo    | Descripción                                           |
| ----------------- | ------- | ----------------------------------------------------- |
| `Status`          | string  |                                                       |
| `Code`            | integer | 200, 400, 401, 500, ...                               |


```json
{
  "Status":"OK",
  "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                          |
|--------|-----------------------------|------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante. |
| 413    | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo usar la API PostUpdateWorksheetRangeStyle con SDK

### Especificación de la API PostUpdateWorksheetRangeStyle

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle) proporciona el esquema completo.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
cURL -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
  -X POST \
  -d '{
        "Font": {
          "Color": { "A":255, "R":255, "G":255, "B":0 },
          "Size": 22,
          "IsBold": true,
          "IsItalic": true,
          "IsStrikeout": true,
          "IsSubscript": true,
          "IsSuperscript": true,
          "Name": "Arial"
        },
        "Name": "string",
        "CultureCustom": "string",
        "Custom": "string",
        "BackgroundColor": { "A":10, "R":10, "G":10, "B":10 },
        "ForegroundColor": { "A":255, "R":255, "G":255, "B":0 }
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Uso de los SDK de Aspose.Cells Cloud

Usar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells usando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}
---