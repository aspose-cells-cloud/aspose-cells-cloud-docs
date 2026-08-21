---
title: "Obtener saltos de página verticales"
second_title: "Documento"
linktitle: "Obtener saltos de página verticales"
type: docs
url: /page-breaks/get-vertical-page-breaks/
aliases: [/get-vertical-page-breaks-inside-worksheet/]
keywords: "Aspose.Cells, saltos de página verticales, API de Excel, hoja de cálculo en la nube, API REST"
description: "Recuperar saltos de página verticales desde una hoja de cálculo de Excel usando la API REST de Aspose.Cells Cloud (v3.0). Incluye el endpoint HTTPS, parámetros necesarios, ejemplo con cURL, detalles de la respuesta, manejo de errores y ejemplos de SDK."
weight: 20
---

Esta API REST recupera los **saltos de página verticales** de una hoja de cálculo.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                              | Obligatorio |
| -------------------- | ------ | --------- | -------------------------------------------------------- | ----------- |
| `name`               | string | path      | El nombre del archivo de Excel.                          | Sí          |
| `sheetName`          | string | path      | El nombre de la hoja de cálculo desde la cual leer los saltos. | Sí          |
| `folder`             | string | query     | La carpeta en el almacenamiento que contiene el archivo. | No          |
| `storageName`        | string | query     | El nombre del almacenamiento de Aspose Cloud a utilizar. | No          |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "VerticalPageBreaks": {
    "VerticalPageBreakList": [
      {
        "Column": 3,
        "EndRow": 1048575,
        "StartRow": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",
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

### Detalles de la respuesta

| Campo                   | Tipo  | Descripción                                                                          |
| ----------------------- | ----- | ------------------------------------------------------------------------------------ |
| `VerticalPageBreakList` | array | Colección de objetos de salto de página vertical.                                   |
| `Column`                | int   | Índice de columna (basado en cero) donde ocurre el salto.                            |
| `StartRow`              | int   | Primera fila del rango de salto (basado en cero).                                    |
| `EndRow`                | int   | Última fila del rango de salto (basado en cero; típicamente `1048575` para la última fila). |
| `link.Href`             | string | URL de autorreferencia del recurso (HTTPS).                                          |
| `Code`                  | int   | Código de estado HTTP devuelto por el servicio.                                      |
| `Status`                | string | Descripción textual del estado HTTP.                                                 |

### Manejo de errores

| Código HTTP | Significado           | Causa típica                              |
| ----------- | --------------------- | ------------------------------------------ |
| 401         | No autorizado         | Token JWT ausente o inválido.              |
| 404         | No encontrado         | El archivo o la hoja de cálculo especificados no existen. |
| 400         | Solicitud incorrecta  | Parámetros de consulta inválidos o mal formados. |
| 500         | Error interno del servidor | Condición inesperada del lado del servidor. |

Compruebe los campos `Code` y `Status` en la respuesta JSON para obtener más detalles.

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar con Aspose.Cells Cloud. Un SDK abstracta los detalles de bajo nivel para que pueda centrarse en la lógica de su negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetVerticalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetVerticalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetVerticalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetVerticalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetVerticalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetVerticalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetVerticalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetVerticalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}