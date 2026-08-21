---
title: "Ocultar columnas en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Ocultar"
type: docs
url: /es/columns/hide/
aliases:
  - /hide-columns-in-excel-worksheet/
  - /hide-columns-in-an-excel-worksheet/
keywords: "Aspose.Cells Cloud, API para ocultar columnas, ocultar columnas en Excel, API REST para ocultar columnas, SDK de Aspose.Cells, automatización de hojas de cálculo"
description: "Aprenda a ocultar una o más columnas en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye el punto de conexión, parámetros, ejemplo con cURL, ejemplos de código en SDK y manejo de errores."
weight: 40
---

Esta API REST oculta columnas en una hoja de cálculo.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/hide
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                 |
|----------------------|---------|-----------|-----------------------------------------------------------------------------|
| name                 | string  | path      | Nombre del archivo del libro de trabajo.                                   |
| sheetName            | string  | path      | Nombre de la hoja de cálculo en la que se ocultarán las columnas.          |
| startColumn          | integer | query     | Índice de base cero de la primera columna que se ocultará.                 |
| totalColumns         | integer | query     | Número de columnas consecutivas que se ocultarán, comenzando desde **startColumn**. |
| folder               | string  | query     | Ruta a la carpeta que contiene el libro de trabajo.                        |
| storageName          | string  | query     | Nombre del servicio de almacenamiento donde se encuentra el archivo.       |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetColumns) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para llamar fácilmente a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo ocultar una columna con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/hide?startColumn=1&totalColumns=1" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Códigos de respuesta posibles**

| Código HTTP | Significado                                 | Ejemplo JSON (error)                                     |
|-------------|---------------------------------------------|----------------------------------------------------------|
| 200         | Éxito                                       | `{ "Code": 200, "Status": "OK" }`                        |
| 400         | Solicitud incorrecta (por ejemplo, parámetros inválidos) | `{ "Code": 400, "Message": "Rango de columnas no válido." }` |
| 401         | No autorizado (token faltante o inválido)   | `{ "Code": 401, "Message": "Token de acceso inválido." }` |
| 404         | No encontrado (libro de trabajo o hoja de cálculo) | `{ "Code": 404, "Message": "Archivo no encontrado." }` |
| 500         | Error interno del servidor                  | `{ "Code": 500, "Message": "Error inesperado." }`        |

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel para que pueda concentrarse en la lógica de su negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostHideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostHideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostHideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostHideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostHideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostHideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostHideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostHideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}