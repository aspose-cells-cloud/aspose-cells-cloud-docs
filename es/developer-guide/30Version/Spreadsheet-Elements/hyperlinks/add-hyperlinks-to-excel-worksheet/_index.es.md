---
title: "Agregar hipervínculo a una hoja de cálculo"
type: docs
url: /hyperlinks/add/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells, agregar hipervínculo, API REST de Excel, SDK en la nube"
description: "Aprenda cómo agregar un hipervínculo a una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud v3.0. Incluye el endpoint, una guía completa de parámetros, un ejemplo con cURL y fragmentos de código para SDK en C#, Java, Python y más."
weight: 20
---

Esta API REST agrega un hipervínculo a una hoja de cálculo de Excel.

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                                     |
| -------------------- | ------- | --------- | ----------------------------------------------------------------------------------------------- |
| name                 | string  | path      | Nombre del documento.                                                                           |
| sheetName            | string  | path      | Nombre de la hoja de cálculo.                                                                   |
| firstRow             | integer | query     | Índice de fila (basado en cero) de la primera fila del rango al que se aplicará el hipervínculo. |
| firstColumn          | integer | query     | Índice de columna (basado en cero) de la primera columna del rango al que se aplicará el hipervínculo. |
| totalRows            | integer | query     | Número de filas que abarca el rango del hipervínculo.                                           |
| totalColumns         | integer | query     | Número de columnas que abarca el rango del hipervínculo.                                        |
| address              | string  | query     | La URL de destino a la que apunta el hipervínculo (codificada en URL).                          |
| folder               | string  | query     | Carpeta del documento.                                                                          |
| storageName          | string  | query     | Nombre del almacenamiento.                                                                      |

La solicitud también puede incluir un cuerpo JSON que contenga los mismos campos (`Address`, `FirstRow`, `FirstColumn`, `TotalRows`, `TotalColumns`). Proporcionar el cuerpo es útil cuando prefiere una carga útil en lugar de parámetros en la cadena de consulta.

### Respuestas de error

| Código HTTP | Razón                                                | Cuerpo de ejemplo                                                    |
| ----------- | ---------------------------------------------------- | -------------------------------------------------------------------- |
| **400**     | Solicitud incorrecta: parámetros faltantes o no válidos. | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**     | No autorizado: token JWT faltante o no válido.         | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | No encontrado: el libro de trabajo o la hoja de cálculo no existe. | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**     | Error interno del servidor: fallo inesperado.          | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Hypelinks/PutWorksheetHyperlink) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks?firstRow=1&firstColumn=6&totalRows=1&totalColumns=1&address=https%3A%2F%2Fwww.msnbc.com%2F" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Si la solicitud falla, la API devuelve los códigos de error HTTP estándar (por ejemplo, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error) junto con una carga útil en JSON que contiene un mensaje y código de error.

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK gestiona los detalles de bajo nivel, para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}