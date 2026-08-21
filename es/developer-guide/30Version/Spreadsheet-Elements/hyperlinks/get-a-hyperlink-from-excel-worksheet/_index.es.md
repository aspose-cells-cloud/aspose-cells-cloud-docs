---
title: "Obtener hipervínculo de hoja de cálculo"
type: docs
url: /hyperlinks/get/
keywords: "Aspose.Cells Cloud, Obtener hipervínculo de hoja de cálculo, API de hipervínculos de Excel, REST, Autenticación JWT, Hoja de cálculo de Excel, Punto final de la API"
description: "Recuperar un hipervínculo específico de una hoja de cálculo de Excel utilizando la API de Aspose.Cells Cloud (v3.0). Incluye punto final, parámetros, ejemplo de cURL, detalles de autenticación, manejo de errores y fragmentos de SDK."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – Obtener hipervínculo de hoja de cálculo"
---

Esta API REST recupera un **hipervínculo** de hoja de cálculo mediante la **API de Obtener Hipervínculo de Aspose.Cells**.

## Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
Antes de llamar al punto final, obtenga un token de acceso JWT utilizando su ID de cliente y secreto, e inclúyalo en el encabezado `Authorization: Bearer <jwt token>`.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                          |
| --------------------- | ------- | --------- | ---------------------------------------------------- |
| name                  | string  | path      | Nombre del archivo de Excel.                        |
| sheetName             | string  | path      | Nombre de la hoja de cálculo que contiene el enlace. |
| hyperlinkIndex        | integer | path      | Índice de base cero del hipervínculo a recuperar.    |
| folder                | string  | query     | Carpeta donde se guarda el documento.               |
| storageName           | string  | query     | Nombre del servicio de almacenamiento.              |

### Respuestas de error

| Código HTTP | Razón                                                          | Cuerpo de ejemplo                                                   |
| ----------- | -------------------------------------------------------------- | ------------------------------------------------------------------- |
| **400**     | Solicitud incorrecta: parámetros faltantes o no válidos.      | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**     | No autorizado: token JWT faltante o no válido.                 | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | No encontrado: el libro o la hoja de cálculo no existen.      | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**     | Error interno del servidor: fallo inesperado del servidor.    | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlink) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlink": {
    "Address": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "Area": {
      "EndColumn": 0,
      "EndRow": 1,
      "StartColumn": 0,
      "StartRow": 1
    },
    "ScreenTip": null,
    "TextToDisplay": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/hyperlinks/1",
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

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}