---
title: "Agregar condición de formato"
type: docs
url: /es/conditional-formattings/add-format-condition/
aliases: [  /es/add-a-format-condition/ ]
keywords: "Aspose.Cells Cloud, API de formato condicional, Agregar condición de formato, API REST de Excel, API de celdas"
description: "Aprenda cómo agregar una condición de formato a una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye sintaxis de solicitud, parámetros, ejemplo de cURL seguro y fragmentos de SDK."
ArticleTitle: "Agregar condición de formato – Documentación de la API de Aspose.Cells Cloud"
weight: 50
---

Esta API REST agrega una condición de formato a una hoja de cálculo.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                 |
| -------------------- | ------- | --------- | --------------------------------------------------------------------------- |
| name                 | string  | path      | El nombre del libro de Excel.                                               |
| sheetName            | string  | path      | El nombre de la hoja de cálculo que contiene el rango que se va a formatear.|
| index                | integer | path      | El índice base cero de la condición de formato que se va a agregar o reemplazar. |
| cellArea             | string  | query     | El rango de celdas (por ejemplo, `A1:C3`) al que se aplica la condición.    |
| type                 | string  | query     | El tipo de condición (por ejemplo, `Expression`, `CellValue`).              |
| operatorType         | string  | query     | El operador para la condición (por ejemplo, `Between`, `Equal`).            |
| formula1             | string  | query     | La primera fórmula o valor utilizado por la condición.                      |
| formula2             | string  | query     | La segunda fórmula o valor (requerido para algunos operadores como `Between`). |
| folder               | string  | query     | La carpeta en el almacenamiento donde se encuentra el libro.                |
| storageName          | string  | query     | El nombre del servicio de almacenamiento (por ejemplo, `Default`).          |

### Respuestas de error

| Código HTTP | Motivo                                           | Cuerpo de ejemplo                                                   |
| ----------- | ------------------------------------------------ | ------------------------------------------------------------------- |
| **400**     | Solicitud incorrecta – parámetros faltantes o no válidos. | `{ "Code":"400", "Message":"Valor de parámetro no válido." }`      |
| **401**     | No autorizado – token JWT faltante o no válido. | `{ "Code":"401", "Message":"El token de acceso falta o no es válido." }` |
| **404**     | No encontrado – el libro o la hoja de cálculo no existe. | `{ "Code":"404", "Message":"Archivo no encontrado." }`            |
| **500**     | Error interno del servidor – fallo inesperado del servidor. | `{ "Code":"500", "Message":"Se produjo un error inesperado." }`   |

### Respuesta correcta

| Código HTTP | Motivo                                         | Cuerpo de ejemplo                         |
| ----------- | ---------------------------------------------- | ------------------------------------------ |
| **200**     | Correcto – condición agregada o actualizada correctamente. | `{ "Code": "200", "Status": "OK" }` |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatCondition) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar **cURL** para llamar a la API de Aspose.Cells. El ejemplo siguiente muestra una solicitud completa, incluyendo un cuerpo JSON vacío.

### Ejemplo con cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0?cellArea=A1:C3&type=Expression&operatorType=Between&formula1=v1&formula2=v2" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'
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

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-AddFormatCondition-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-AddFormatCondition-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-AddFormatCondition-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "caa13d019b3c7c3b5c14110ccd217e99" >}}

{{< /tab >}}

{{< /tabs >}}