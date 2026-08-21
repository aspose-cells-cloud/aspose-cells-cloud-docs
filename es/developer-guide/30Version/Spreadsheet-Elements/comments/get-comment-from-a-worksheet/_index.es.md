---
title: "Obtener comentario de hoja de cálculo – Documentación de la API de Aspose.Cells Cloud"
type: docs
url: /es/comments/get/
aliases: [  /es/get-comment-from-a-worksheet/ ]
keywords: "Aspose.Cells, comentario de hoja de cálculo, API, GET, Excel"
description: "Aprenda cómo recuperar un comentario de hoja de cálculo por nombre de celda utilizando la API de Aspose.Cells Cloud (v3.0). Incluye URL de solicitud, parámetros, ejemplo con cURL, detalles de respuesta y fragmentos de código de SDK."
weight: 10
ArticleTitle: "Obtener comentario de hoja de cálculo – Documentación de la API de Aspose.Cells Cloud"
---

Esta REST API recupera un comentario de hoja de cálculo por nombre de celda utilizando **Aspose.Cells Cloud**.

**Requisitos previos:** Para llamar a esta operación, debe incluir un token de acceso JWT válido en el encabezado `Authorization` (`Bearer <jwt token>`). Los tokens se pueden obtener mediante el flujo de autenticación de Aspose.Cells Cloud descrito en la [guía de autenticación](/cells/authentication/).

## API GetWorksheetComment

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación (ruta URL / cadena de consulta) | Descripción                                                                 |
| -------------------- | ------ | ----------------------------------------- | --------------------------------------------------------------------------- |
| name                 | string | Ruta URL                                  | Nombre del archivo de Excel.                                                |
| sheetName            | string | Ruta URL                                  | Nombre de la hoja de cálculo que contiene el comentario.                   |
| cellName             | string | Ruta URL                                  | Dirección de la celda (por ejemplo, **A1**) cuyo comentario se está recuperando. |
| folder               | string | Cadena de consulta                        | Ruta de la carpeta donde se almacena el documento.                         |
| storageName          | string | Cadena de consulta                        | Nombre del servicio de almacenamiento.                                     |

La <a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "roy.wang",
    "HtmlNote": "",
    "Note": "Aspose.Cells Cloud.",
    "AutoSize": "True",
    "IsVisible": "True",
    "Width": 30,
    "Height": 10,
    "TextHorizontalAlignment": "Bottom",
    "TextOrientationType": "TopToBottom",
    "TextVerticalAlignment": "Bottom"
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Respuesta:** La API devuelve un objeto JSON que contiene un objeto `Comment` con los siguientes campos:

| Campo                      | Tipo    | Descripción                                             |
| -------------------------- | ------- | ------------------------------------------------------- |
| `CellName`                 | string  | Dirección de la celda (por ejemplo, **A1**).           |
| `Author`                   | string  | Nombre del autor del comentario.                        |
| `HtmlNote`                 | string  | Contenido del comentario en formato HTML (si existe).  |
| `Note`                     | string  | Versión en texto plano del comentario.                  |
| `AutoSize`                 | boolean | Indica si el cuadro del comentario se redimensiona automáticamente. |
| `IsVisible`                | boolean | Determina si el comentario es visible.                 |
| `Width`                    | integer | Ancho del cuadro del comentario (en caracteres).        |
| `Height`                   | integer | Alto del cuadro del comentario (en caracteres).         |
| `TextHorizontalAlignment` | string  | Alineación horizontal del texto (por ejemplo, **Bottom**). |
| `TextOrientationType`      | string  | Orientación del texto (por ejemplo, **TopToBottom**).  |
| `TextVerticalAlignment`    | string  | Alineación vertical del texto (por ejemplo, **Bottom**). |

## Errores comunes

- **401 No autorizado** – Verifique que el token JWT sea válido, no haya expirado y esté correctamente colocado en el encabezado `Authorization`.
- **404 No encontrado** – Asegúrese de que el nombre del archivo, el nombre de la hoja de cálculo y la dirección de la celda sean correctos y que el archivo exista en la carpeta/almacenamiento especificados.
- **500 Error interno del servidor** – Compruebe que la carga útil de la solicitud no contenga datos mal formados y confirme que el servicio esté operativo.

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                  |
| ------ | --------------------------- | ------------------------------------------------------------ |
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente.                                |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño.               |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                             |

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetComments.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetComments.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetComments.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetComments.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetComments.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetComments.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetComments.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetComments.go" >}}

{{< /tab >}}

{{< /tabs >}}