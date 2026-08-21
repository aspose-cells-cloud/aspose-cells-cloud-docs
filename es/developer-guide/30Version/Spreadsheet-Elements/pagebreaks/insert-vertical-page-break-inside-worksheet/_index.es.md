---
title: "Agregar un salto de página vertical"
second_title: "Documento"
linktitle: "Agregar un salto de página vertical"
type: docs
url: /page-breaks/add-vertical-page-break/
aliases: [/insert-vertical-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud, salto de página vertical, API REST, Excel, SDK, cURL"
description: "Aprenda cómo insertar un salto de página vertical en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye sintaxis de solicitud, ejemplo con cURL, ejemplos de SDK, guía de autenticación y detalles sobre manejo de errores."
weight: 40
ArticleTitle: "Agregar un salto de página vertical – API de Aspose.Cells Cloud"
---

Esta API REST inserta un salto de página vertical en una hoja de cálculo.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                 |
|----------------------|---------|-----------|-----------------------------------------------------------------------------|
| name                 | string  | path      | El nombre del libro de Excel.                                               |
| sheetName            | string  | path      | El nombre de la hoja de cálculo donde se agregará el salto de página.       |
| cellname             | string  | query     | La referencia de celda (por ejemplo, **A1**) que define la ubicación del salto de página. |
| column               | integer | query     | El índice basado en cero de la columna donde comienza el salto de página.   |
| row                  | integer | query     | El índice basado en cero de la fila donde comienza el salto de página.      |
| startRow             | integer | query     | La primera fila del rango del salto de página.                              |
| endRow               | integer | query     | La última fila del rango del salto de página.                               |
| folder               | string  | query     | La ruta de la carpeta en el almacenamiento donde se encuentra el libro.     |
| storageName          | string  | query     | El nombre del servicio de almacenamiento.                                   |

**Parámetros obligatorios**: Se debe proporcionar **ya sea** `cellname` **o** `column`. Cuando se usa `column`, también puede proporcionar `row`, `startRow` y `endRow` para definir un rango. Todos los demás campos son opcionales.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Ejemplo con cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SampleBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Respuesta

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                             |
|--------|-----------------------------|-------------------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente.                                            |
| 413    | Payload demasiado grande     | El archivo cargado excede el límite de tamaño.                          |
| 500    | Error interno del servidor  | Error inesperado del servidor.                                          |

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}