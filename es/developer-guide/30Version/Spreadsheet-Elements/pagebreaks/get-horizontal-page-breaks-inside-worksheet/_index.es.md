---
title: "Obtener saltos de página horizontales"
second_title: "Documentos"
linktitle: "Obtener saltos de página horizontales"
type: docs
url: /page-breaks/get-horizontal-page-breaks/
aliases: [/get-horizontal-page-breaks-inside-worksheet/]
keywords: "saltos de página horizontales, Aspose.Cells Cloud, API REST, hoja de cálculo de Excel, SDK"
description: "Recuperar saltos de página horizontales desde una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud. Incluye el punto de conexión, parámetros, ejemplo de cURL, formato de respuesta y fragmentos de SDK para C#, Java, Python y más."
ArticleTitle: "Obtener saltos de página horizontales - Documentación de la API de Aspose.Cells Cloud"
weight: 10
---

**Salto de página horizontal**: una interrupción basada en filas que obliga a la hoja de cálculo a iniciar una nueva página impresa después de la fila especificada. Esta API REST recupera esos saltos de página horizontales.

## Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                       |
| --------------------- | ------ | --------- | ----------------------------------------------------------------- |
| name                  | string | path      | El nombre del archivo de Excel.                                   |
| sheetName             | string | path      | El nombre de la hoja de cálculo.                                  |
| folder                | string | query     | La ruta de la carpeta en el almacenamiento donde se encuentra el archivo. _(opcional)_ |
| storageName           | string | query     | El nombre del almacenamiento. _(opcional)_                       |

La <a href="https://apireference.aspose.cloud/cells/#/PageBreaks/GetHorizontalPageBreaks" rel="noopener" title="Especificación OpenAPI para GetHorizontalPageBreaks">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo invocar la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "HorizontalPageBreaks": {
    "HorizontalPageBreakList": [
      {
        "Row": 6,
        "EndColumn": 16383,
        "StartColumn": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/HorizontalPageBreaks",
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

## Manejo de errores

| Estado HTTP | Descripción                                                   | Ejemplo JSON                                        |
| ----------- | ------------------------------------------------------------- | --------------------------------------------------- |
| 400         | Solicitud incorrecta: parámetros faltantes o no válidos.     | `{ "Code": 400, "Message": "Parámetro no válido." }` |
| 401         | No autorizado: token JWT faltante o no válido.                | `{ "Code": 401, "Message": "Fallo en la autenticación." }` |
| 404         | No encontrado: el archivo o la hoja de cálculo especificados no existen. | `{ "Code": 404, "Message": "Recurso no encontrado." }` |
| 500         | Error interno del servidor: condición inesperada en el servidor. | `{ "Code": 500, "Message": "Error del servidor." }` |

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetHorizontalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetHorizontalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetHorizontalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetHorizontalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetHorizontalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetHorizontalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetHorizontalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetHorizontalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}