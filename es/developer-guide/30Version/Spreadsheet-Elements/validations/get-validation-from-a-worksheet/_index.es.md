---
title: "Obtener una validación de hoja de cálculo por índice desde una hoja de cálculo de Excel"
second_title: "Document"
linktype: "Get"
type: docs
url: /validations/get/
aliases: [/get-validation-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, API de validación de hoja de cálculo, obtener validación por índice, API REST de Excel, Aspose.Cells SDK"
description: "Recuperar una validación de hoja de cálculo mediante su índice basado en cero desde un libro de Excel usando la API de Aspose.Cells Cloud (v3.0). Incluye ejemplo de cURL, esquema de respuesta, códigos de error y fragmentos de SDK para C#, Java, Python y más."
weight: 10
---

Esta API REST recupera una validación de hoja de cálculo por su índice en una hoja de cálculo de Excel.  
Antes de llamar al punto de conexión, obtenga un token JWT mediante el punto de conexión `/connect/token` e inclúyalo en el encabezado `Authorization` como `Bearer <jwt token>`.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                |
| --------------------- | ------- | --------- | ---------------------------------------------------------- |
| name                  | string  | path      | Nombre del archivo del libro de trabajo.                  |
| sheetName             | string  | path      | Nombre de la hoja de cálculo.                             |
| validationIndex       | integer | path      | Índice basado en cero de la validación que se va a recuperar. |
| folder                | string  | query     | Carpeta que contiene el libro de trabajo.                 |
| storageName           | string  | query     | Nombre del servicio de almacenamiento.                    |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidation) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Validation": {
    "AlertStyle": "Stop",
    "AreaList": [
      {
        "EndColumn": 0,
        "EndRow": 0,
        "StartColumn": 0,
        "StartRow": 0
      },
      {
        "EndColumn": 27,
        "EndRow": 0,
        "StartColumn": 26,
        "StartRow": 0
      }
    ],
    "IgnoreBlank": false,
    "InCellDropDown": false,
    "Operator": "None",
    "ShowError": false,
    "ShowInput": false,
    "Type": "AnyValue",
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/Validations/0",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Esquema de respuesta**

| Campo          | Tipo    | Descripción                                                                   |
| -------------- | ------- | ----------------------------------------------------------------------------- |
| AlertStyle     | string  | Estilo de la alerta mostrada al usuario (Stop, Warning, Information).         |
| AreaList       | array   | Colección de rangos de celdas a los que se aplica la validación.              |
| IgnoreBlank    | boolean | Si es `true`, se ignoran las celdas en blanco durante la validación.          |
| InCellDropDown | boolean | Si es `true`, se muestra una lista desplegable en la celda.                   |
| Operator       | string  | Operador de comparación utilizado para la validación (por ejemplo, `None`, `Between`). |
| ShowError      | boolean | Determina si se muestra un mensaje de error cuando la validación falla.       |
| ShowInput      | boolean | Determina si se muestra un mensaje de entrada al seleccionar la celda.        |
| Type           | string  | Tipo de validación (por ejemplo, `AnyValue`, `WholeNumber`, `Decimal`, etc.). |
| link.Href      | string  | URL de autoreferencia al recurso de validación.                               |
| link.Rel       | string  | Tipo de relación (siempre `self`).                                            |

**Códigos de error posibles**

| Estado HTTP | Significado                                                              |
| ----------- | ------------------------------------------------------------------------ |
| 200         | Validación recuperada correctamente.                                     |
| 400         | Solicitud incorrecta: faltan o son inválidos los parámetros.             |
| 401         | No autorizado: token JWT inválido o ausente.                             |
| 404         | No encontrado: el libro de trabajo, la hoja de cálculo o el índice de validación no existen. |
| 500         | Error interno del servidor: condición inesperada.                        |

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar con Aspose.Cells Cloud. Un SDK abstracte los detalles de bajo nivel, permitiéndole centrarse en la lógica de su negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}