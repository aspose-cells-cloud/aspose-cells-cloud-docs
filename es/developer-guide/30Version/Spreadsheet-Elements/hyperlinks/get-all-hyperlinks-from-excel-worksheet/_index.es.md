---
title: "Obtener todos los hipervínculos – Aspose.Cells Cloud REST API"
type: docs
url: /hyperlinks/get-all/
aliases:
  [/get-hyperlink-from-excel-worksheet/, /get-hyperlinks-from-excel-worksheet/]
keywords: "Aspose.Cells, obtener todos los hipervínculos, API de Excel, API REST, SDK en la nube, ejemplo con cURL, hipervínculos en hojas de cálculo"
description: "Recupere todos los hipervínculos de una hoja de cálculo en un archivo de Excel mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye endpoint HTTPS, parámetros requeridos, ejemplo con cURL, esquema de respuesta y ejemplos de código con SDK."
weight: 10
ArticleTitle: "Obtener todos los hipervínculos – Documentación de Aspose.Cells Cloud REST API"
---

Esta API REST recupera **todos los hipervínculos** de una hoja de cálculo específica en un libro de Excel.

## Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio | Valor predeterminado | Descripción                                  |
| --------------------- | ------ | --------- | ----------- | -------------------- | -------------------------------------------- |
| name                  | string | path      | Sí          | –                    | Nombre del documento de Excel.              |
| sheetName             | string | path      | Sí          | –                    | Nombre de la hoja de cálculo.               |
| folder                | string | query     | No          | –                    | Carpeta que contiene el documento.          |
| storageName           | string | query     | No          | –                    | Nombre del servicio de almacenamiento a usar. |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlinks) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo invocar la API mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlinks": {
    "Count": 4,
    "HyperlinkList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": null
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

La respuesta JSON contiene un objeto `Hyperlinks`.

- **Count**: número total de hipervínculos en la hoja de cálculo.
- **HyperlinkList**: matriz donde cada elemento contiene un objeto `link`. La propiedad `Href` almacena la dirección del hipervínculo, mientras que `Rel`, `Title` y `Type` proporcionan metadatos adicionales (a menudo `null` para enlaces simples).

### Respuestas de error

| Código HTTP | Motivo                                                  | Cuerpo de ejemplo                                                    |
| ----------- | ------------------------------------------------------- | -------------------------------------------------------------------- |
| **400**     | Solicitud incorrecta – parámetros faltantes o no válidos. | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**     | No autorizado – token JWT faltante o no válido.         | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | No encontrado – el libro o la hoja de cálculo no existen. | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**     | Error interno del servidor – fallo inesperado en el servidor. | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de integrar esta funcionalidad. Los SDK gestionan los detalles de bajo nivel, permitiéndole centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante distintos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}