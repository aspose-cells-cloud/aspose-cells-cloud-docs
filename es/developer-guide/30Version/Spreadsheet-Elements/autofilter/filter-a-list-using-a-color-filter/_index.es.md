---
title: "Agregar un filtro de color en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Agregar filtro de color"
type: docs
url: /autofilter/add-color-filter/
aliases: [/filter-a-list-using-a-color-filter/,/autofilter/add-a-color-filter/]
keywords: "Excel, filtro de color, Aspose.Cells Cloud, API REST, filtro automático, autenticación JWT"
description: "Aprenda cómo aplicar un filtro de color en una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud. Incluye el endpoint, parámetros, ejemplo de cURL, manejo de errores y ejemplos de SDK."
weight: 65
ArticleTitle: "Agregar un filtro de color en una hoja de cálculo de Excel usando la API de Aspose.Cells Cloud"
---

Aprenda cómo agregar un filtro de color en una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud. Esta guía cubre el endpoint necesario, los parámetros, los requisitos previos de autenticación, la solicitud de ejemplo con cURL, ejemplos de SDK y el manejo de respuestas.

Esta API REST agrega un **filtro de color** a una hoja de cálculo de Excel.

## PutWorksheetColorFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud:


| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                 |
|----------------------|---------|-----------|-----------------------------------------------------------------------------|
| name                 | string  | path      | El nombre del archivo de Excel.                                             |
| sheetName            | string  | path      | El nombre de la hoja de cálculo que contiene los datos que se van a filtrar. |
| range                | string  | query     | El rango de celdas al que se aplica el filtro (por ejemplo, `A1:B10`).      |
| fieldIndex           | integer | query     | Índice de base cero de la columna a la que se aplica el filtro de color.    |
| colorFilter          | object  | body      | Objeto JSON que define los colores de primer plano y de fondo para filtrar. |
| matchBlanks          | boolean | query     | Si se deben incluir en los resultados del filtro las filas con celdas en blanco. |
| refresh              | boolean | query     | Si es `true`, se actualiza la hoja de cálculo tras aplicar el filtro.       |
| folder               | string  | query     | La carpeta en el almacenamiento donde se encuentra el archivo de Excel.     |
| storageName          | string  | query     | El nombre del servicio de almacenamiento (por ejemplo, Aspose Cloud Storage). |

**Esquema JSON de `colorFilter`**

| Propiedad         | Tipo   | Descripción                                                                     | Obligatorio |
|-------------------|--------|---------------------------------------------------------------------------------|-------------|
| Pattern           | string | Patrón de filtro (por ejemplo, `"Solid"`).                                     | Sí          |
| ForegroundColor   | object | Define el color de primer plano. Contiene subpropiedades como `Color`, `ColorIndex`, `IsShapeColor`, `ThemeColor` y `Type`. | No |
| BackgroundColor   | object | Define el color de fondo. Tiene las mismas subpropiedades que `ForegroundColor`. | No |

### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                | Descripción                                         |
|--------|----------------------------|-----------------------------------------------------|
| 200    | OK                         | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta       | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado              | Token JWT inválido o faltante.                      |
| 413    | Carga útil demasiado grande | El archivo subido supera el límite de tamaño.     |
| 500    | Error interno del servidor | Error inesperado en el servidor.                   |

## Cómo usar la API PutWorksheetColorFilter con SDK

### Especificación de la API PutWorksheetColorFilter

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetColorFilter) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/colorFilter?range=A1%3AB1&fieldIndex=0" \
-X PUT \
-d "{ \"Pattern\": \"Solid\", \"ForegroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 1 }, \"Type\": \"Automatic\" }, \"BackgroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 0 }, \"Type\": \"Automatic\" }}" \
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

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetColorFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetColorFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetColorFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetColorFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetColorFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetColorFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetColorFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetColorFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Consulte también:** [Agregar un filtro personalizado](https://docs.aspose.cloud/cells/autofilter/add-custom-filter/), [Agregar un filtro de fecha](https://docs.aspose.cloud/cells/autofilter/add-date-filter/), [Eliminar un filtro automático](https://docs.aspose.cloud/cells/autofilter/remove-auto-filter/).
---