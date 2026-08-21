---
title: "Borrar formato condicional"
type: docs
url: /conditional-formattings/clear/
aliases: [/clear-all-condition-formattings/]
keywords: "Aspose.Cells Cloud, REST API, borrar formato condicional, Excel, hojas de cálculo, JWT, v3.2"
description: "Eliminar todas las reglas de formato condicional de una hoja de cálculo mediante la API de Aspose.Cells Cloud (v3.2). Aprenda la sintaxis de la solicitud, los parámetros requeridos, los pasos de autenticación y consulte el código de ejemplo en múltiples SDK."
weight: 80
---

Esta API REST borra todas las reglas de formato condicional de una hoja de cálculo.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.2/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                           |
|----------------------|--------|-----------|-----------------------------------------------------------------------|
| **name**             | string | path      | El nombre del archivo del libro (por ejemplo, `Book1.xlsx`).         |
| **sheetName**        | string | path      | El nombre de la hoja de cálculo desde la cual eliminar el formato condicional. |
| **folder**           | string | query     | _(Opcional)_ Ruta de la carpeta en el almacenamiento donde se encuentra el libro. |
| **storageName**      | string | query     | _(Opcional)_ Nombre del servicio de almacenamiento.                  |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattings) define una interfaz de programación públicamente accesible y **la Especificación OpenAPI** le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.2/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Respuestas de error

| Código HTTP | Razón                                              | Cuerpo de ejemplo                                                  |
|-------------|----------------------------------------------------|--------------------------------------------------------------------|
| **400**     | Solicitud incorrecta – parámetros faltantes o no válidos. | `{ "Code":"400", "Message":"Valor de parámetro no válido." }`     |
| **401**     | No autorizado – token JWT faltante o no válido.   | `{ "Code":"401", "Message":"El token de acceso es faltante o no válido." }` |
| **404**     | No encontrado – el libro o la hoja de cálculo no existen. | `{ "Code":"404", "Message":"Archivo no encontrado." }`           |
| **500**     | Error interno del servidor – fallo inesperado del servidor. | `{ "Code":"500", "Message":"Ocurrió un error inesperado." }`     |

## Ejemplos de SDK

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-ClearConditionFormattings-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-clear-all-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-ClearConditionFormattings-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-ClearConditionFormattings-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "63fda1be9e5149f83edca47ce58dac87" >}}

{{< /tab >}}

{{< /tabs >}}