---
title: "Obtener reglas de formato condicional"
type: docs
url: /es/conditional-formattings/get-all/
aliases: [  /es/get-conditional-formattings-of-worksheet/ ]
keywords: "Aspose.Cells Cloud, REST API, Excel, Formato condicional, Hoja de cálculo, API de formato condicional"
description: "Recuperar todas las reglas de formato condicional aplicadas a una hoja de cálculo utilizando la API REST de Aspose.Cells Cloud. Incluye sintaxis de solicitud, pasos de autenticación, parámetros, ejemplos concisos de respuesta y manejo de errores."
weight: 20
---

Esta API REST recupera las reglas de formato condicional aplicadas a una hoja de cálculo.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                     |
| -------------------- | ------ | --------- | ----------------------------------------------- |
| name                 | string | path      | El nombre del archivo de Excel.                 |
| sheetName            | string | path      | El nombre de la hoja de cálculo.                |
| folder               | string | query     | La ruta de la carpeta donde se almacena el archivo. |
| storageName          | string | query     | El nombre del servicio de almacenamiento (opcional). |

### Respuestas de error

| Código HTTP | Razón                                                     | Cuerpo de ejemplo                                                  |
| ----------- | --------------------------------------------------------- | ------------------------------------------------------------------ |
| **400**     | Solicitud incorrecta – parámetros faltantes o inválidos. | `{ "Code":"400", "Message":"Invalid parameter value." }`          |
| **401**     | No autorizado – token JWT faltante o inválido.            | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | No encontrado – el libro de trabajo o la hoja de cálculo no existe. | `{ "Code":"404", "Message":"File not found." }`                    |
| **500**     | Error interno del servidor – fallo inesperado del servidor. | `{ "Code":"500", "Message":"An unexpected error occurred." }`      |

La <a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings" target="_blank">Especificación OpenAPI</a> define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "OK",
  "ConditionalFormattings": {
    "Count": 1,
    "ConditionalFormattingList": [
      {
        "sqref": "A1:B10",
        "FormatConditions": [
          {
            "Priority": 1,
            "Type": "CellValue",
            "Operator": "GreaterThan",
            "Formula1": "100",
            "Style": {
              "Font": {
                "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                "IsBold": true
              }
            }
          }
        ]
      }
    ]
  }
}
```

_El ejemplo anterior muestra únicamente los campos más relevantes para mantener la carga útil concisa._

**Parámetros de respuesta**

| Parámetro                               | Tipo   | Descripción                                                                 |
|-----------------------------------------|--------|-----------------------------------------------------------------------------|
| Status                                  | string | Estado del resultado de la solicitud (por ejemplo, **OK**).                |
| ConditionalFormattings                  | object | Contenedor para los datos de formato condicional.                          |
| ConditionalFormattings.Count            | integer| Número de reglas de formato condicional devueltas.                         |
| ConditionalFormattings.ConditionalFormattingList | array  | Lista de objetos de formato condicional.                                   |
| ConditionalFormattingList[].sqref       | string | Rango de celdas al que se aplica el formato (por ejemplo, **A1:B10**).      |
| ConditionalFormattingList[].FormatConditions | array  | Colección de objetos de condiciones de formato para el rango.              |
| FormatConditions[].Priority             | integer| Prioridad de evaluación de la condición.                                   |
| FormatConditions[].Type                 | string | Tipo de condición (por ejemplo, **CellValue**).                            |
| FormatConditions[].Operator             | string | Operador utilizado para la condición (por ejemplo, **GreaterThan**).       |
| FormatConditions[].Formula1             | string | Primera fórmula o valor para la condición.                                 |
| FormatConditions[].Style                | object | Estilo aplicado cuando se cumple la condición.                             |
| Style.Font.Color                        | object | Definición del color RGBA para la fuente.                                   |
| Style.Font.IsBold                       | boolean| Indica si la fuente está en negrita.                                        |

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                    |
|--------|-----------------------------|----------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                                 |
| 413    | Carga útil demasiado grande| El archivo subido excede el límite de tamaño.                  |
| 500    | Error interno del servidor  | Error inesperado del servidor.                                 |

{{< /tab >}}

{{< /tabs >}}

## Familia de SDKs en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que usted se enfoque en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank">repositorio de GitHub</a> para obtener una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-GetWorksheetConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-get-conditional-formatting-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-get_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-GetWorksheetConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-GetWorksheetConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b2a10009556f14d1f939a8433925c5f6" >}}

{{< /tab >}}

{{< /tabs >}}
---