---
title: "Obtener datos de celdas según un rango con nombre"
second_title: "Document"
linktype: "Values"
type: docs
url: /ranges/get/values/
aliases: [/get-cells-data-based-on-named-range/]
keywords: "Aspose.Cells, Cloud, REST API, Excel, rango con nombre, valores de celda, hoja de cálculo"
description: "Recuperar valores de celda desde un rango con nombre en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. El servicio está disponible a través de múltiples SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) y funciona en una amplia gama de plataformas de desarrollo."
weight: 20
ArticleTitle: "Obtener datos de celdas según un rango con nombre – Aspose.Cells Cloud API"
---

**Prerrequisitos**

- Un token de acceso JWT válido con el alcance adecuado.  
- El libro debe estar cargado en el almacenamiento en la nube de Aspose (o en una carpeta especificada).  
- Asegúrese de proporcionar el nombre del almacenamiento objetivo si utiliza un almacenamiento no predeterminado.

Esta API REST devuelve una lista de celdas dentro de un rango identificado por un rango con nombre o por índices de fila y columna.

Esta operación permite a los desarrolladores recuperar programáticamente los valores de las celdas que pertenecen a un rango con nombre específico en una hoja de cálculo de Excel. Al proporcionar el identificador `namedRange` o los índices explícitos de fila y columna, la API devuelve una lista detallada de celdas, incluyendo su dirección, fila, columna, valor, tipo de datos e información de formato. La respuesta puede utilizarse para impulsar aplicaciones basadas en datos, generar informes o realizar cálculos adicionales del lado del servidor. El servicio Aspose.Cells Cloud admite múltiples lenguajes de programación mediante sus SDK, garantizando una integración fluida independientemente de la plataforma de desarrollo. El uso de HTTPS garantiza la transmisión segura de los datos, y la API sigue los principios REST, devolviendo códigos de estado HTTP estándar para condiciones de éxito y error.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                                      |
|----------------------|---------|-----------|--------------------------------------------------------------------------------------------------|
| name                 | string  | path      | Nombre del archivo del libro.                                                                   |
| sheetName            | string  | path      | Nombre de la hoja de cálculo dentro del libro.                                                  |
| namedRange           | string  | query     | Rango con nombre a recuperar, por ejemplo, `A1:B2` o `range_name1`.                            |
| firstRow             | integer | query     | Índice de fila (basado en cero) de la primera fila del rango (se utiliza cuando no se proporciona `namedRange`). |
| firstColumn          | integer | query     | Índice de columna (basado en cero) de la primera columna del rango (se utiliza cuando no se proporciona `namedRange`). |
| rowCount             | integer | query     | Número de filas incluidas en el rango.                                                          |
| columnCount          | integer | query     | Número de columnas incluidas en el rango.                                                       |
| folder               | string  | query     | Carpeta que contiene el libro.                                                                  |
| storageName          | string  | query     | Nombre del almacenamiento en la nube donde reside el libro.                                    |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para llamar fácilmente a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo solicitar valores de celda desde un rango con nombre.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?namerange=data" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "CellsList": [
    {
      "Name": "B10",
      "Row": 9,
      "Column": 1,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "C10",
      "Row": 9,
      "Column": 2,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "D10",
      "Row": 9,
      "Column": 3,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "E10",
      "Row": 9,
      "Column": 4,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "F10",
      "Row": 9,
      "Column": 5,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "G10",
      "Row": 9,
      "Column": 6,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "H10",
      "Row": 9,
      "Column": 7,
      "Value": "a8",
      "Type": "IsString",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">a8</Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Nota de seguridad:** Utilice siempre HTTPS al llamar a la API. El servicio no admite HTTP sin cifrar; el uso de HTTPS garantiza que la solicitud esté cifrada y cumpla con las mejores prácticas de seguridad.

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                      |
|--------|-----------------------------|------------------------------------------------------------------|
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente.                                   |
| 413    | Payload demasiado grande     | El archivo cargado excede el límite de tamaño.                  |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                                 |

**Ejemplo de respuesta de error (400 Bad Request)**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "El parámetro 'namedRange' está ausente o no es válido."
}
```

> **Consejo:** La API utiliza índices basados en cero para `firstRow` y `firstColumn`. Por ejemplo, la primera fila de la hoja de cálculo es `0`.

## Familia de SDK en la nube

Utilizar un SDK es la forma más eficiente de acelerar el desarrollo. Un SDK abstrae los detalles de bajo nivel, permitiéndole centrarse en la lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellsRangeValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellsRangeValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellsRangeValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellsRangeValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellsRangeValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellsRangeValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellsRangeValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellsRangeValue.go" >}}

{{< /tab >}}

{{< /tabs >}}