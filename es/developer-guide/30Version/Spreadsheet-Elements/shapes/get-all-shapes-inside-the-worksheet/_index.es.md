---
title: "Obtener todas las formas en una hoja de cálculo de Excel"
second_title: "Document"
linktype: "get-all"
type: docs
url: /es/shapes/get-all/
aliases: [  /es/get-all-shapes-inside-the-worksheet/ ]
keywords: "Aspose.Cells, API en la nube, formas de Excel, obtener formas, REST, SDK"
description: "Recuperar todas las formas (gráficos, imágenes, cuadros de texto) de una hoja de cálculo mediante la API REST de Aspose.Cells Cloud. Incluye ejemplo de cURL, fragmentos de SDK, pasos de autenticación y manejo de errores."
ArticleTitle: "Obtener todas las formas en una hoja de cálculo de Excel"
weight: 10
---

Esta API REST permite recuperar todas las formas en una hoja de cálculo de Excel.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                              |
| --------------------- | ------ | --------- | -------------------------------------------------------------------------------------------------------- |
| **name**              | string | path      | El nombre del archivo de Excel.                                                                          |
| **sheetName**         | string | path      | El nombre de la hoja de cálculo.                                                                         |
| **folder**            | string | query     | La carpeta que contiene el documento.                                                                    |
| **storageName**       | string | query     | El nombre del servicio de almacenamiento a utilizar.                                                     |
| **include**           | string | query     | Establecer en `details` para devolver las propiedades completas de la forma; de lo contrario, solo se devuelven los objetos `link`. |

> **Opcional**: `folder`, `storageName` y `include` pueden omitirse si el archivo reside en el almacenamiento raíz.

Puede utilizar la herramienta de línea de comandos cURL para acceder a los servicios web de Aspose.Cells. El siguiente ejemplo muestra una solicitud que incluye los parámetros de consulta opcionales.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?folder=Samples&storageName=MyStorage" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Shapes": {
    "ShapeList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes",
      "Rel": "self",
      "Type": null,
      "Title": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Campos de respuesta

El objeto `Shapes` contiene una lista de elementos `Shape`. Cada forma incluye las siguientes propiedades (cuando se utiliza la bandera `include=details`; de lo contrario solo se devuelve el objeto `link`).

| Propiedad  | Tipo   | Descripción                                                                |
| ---------- | ------ | -------------------------------------------------------------------------- |
| **Name**   | string | El nombre asignado a la forma (por ejemplo, “Gráfico 1”).                  |
| **Type**   | string | El tipo de forma (por ejemplo, `Chart`, `Picture`, `TextBox`).             |
| **Top**    | number | La distancia, en puntos, desde el borde superior de la hoja de cálculo hasta la forma. |
| **Left**   | number | La distancia, en puntos, desde el borde izquierdo de la hoja de cálculo hasta la forma. |
| **Width**  | number | El ancho de la forma en puntos.                                            |
| **Height** | number | El alto de la forma en puntos.                                             |
| **Link**   | object | Información del hipervínculo (`Href`, `Rel`, `Type`, `Title`).             |

## Manejo de errores

| Estado HTTP | Descripción                                           | Cuerpo de error de ejemplo                                          |
| ----------- | ----------------------------------------------------- | ------------------------------------------------------------------- |
| **400**     | Solicitud incorrecta – parámetros mal formados.       | `{ "Code": 400, "Message": "Invalid parameter value." }`            |
| **401**     | No autorizado – token ausente o no válido.           | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| **404**     | No encontrado – el libro de trabajo o la hoja de cálculo no existen. | `{ "Code": 404, "Message": "File or worksheet not found." }`        |
| **500**     | Error interno del servidor – condición inesperada.    | `{ "Code": 500, "Message": "An unexpected error occurred." }`       |

Una solicitud correcta devuelve **HTTP 200** con un objeto `Shapes` que contiene la lista de formas, tal como se ilustra en el ejemplo de respuesta anterior.

La API impone un límite de **150 solicitudes por minuto por token JWT**. Superar este límite devuelve **HTTP 429** con un encabezado `Retry-After` que indica cuándo volver a intentar.

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}