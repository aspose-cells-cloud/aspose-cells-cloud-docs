---
title: "Obtener la primera celda (A1) de una hoja de cálculo de Excel"
type: docs
url: /get-first-cell-from-excel-worksheet/
weight: 20
keywords: "Aspose.Cells Cloud, Excel, REST API, Obtener primera celda, Hoja de cálculo, A1, API v3"
description: "Aprenda cómo recuperar la primera celda (A1) de una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud v3.0. Incluye solicitud cURL, respuesta JSON, ejemplos de error y muestras de SDK para C#, Java, PHP, Python y más."
ArticleTitle: "Obtener la primera celda (A1) de una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud"
---

Esta API REST muestra cómo recuperar la **primera celda** en un archivo de Excel cuando el parámetro `cellOrMethodName` se establece en `firstcell`.

**Punto de conexión**  
`GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{worksheet}/cells/firstcell`

- **Ejemplo con cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```shell
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/firstcell" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Parámetros**

| Parámetro          | Tipo   | Descripción                                                | Obligatorio |
|--------------------|--------|------------------------------------------------------------|-------------|
| `cellOrMethodName` | string | Debe establecerse en `firstcell` para recuperar la primera celda. | Sí          |
| `fileName`         | string | Nombre del archivo del libro (por ejemplo, `myWorkbook.xlsx`). | Sí          |
| `worksheet`        | string | Nombre de la hoja de cálculo (por ejemplo, `Sheet1`).     | Sí          |
| `Authorization`    | header | Token Bearer para la autenticación.                        | Sí          |

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A1",
    "Row": 0,
    "Column": 0,
    "Value": "Category",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #ffffff;\">Category</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

**Respuestas de error**

- **401 No autorizado**

```json
{
  "Code": "401",
  "Message": "Token de acceso inválido."
}
```

- **404 No encontrado**

```json
{
  "Code": "404",
  "Message": "El libro, la hoja de cálculo o la celda especificados no existen."
}
```

- **500 Error interno del servidor**

```json
{
  "Code": "500",
  "Message": "Se produjo un error inesperado en el servidor."
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                |
|--------|-----------------------------|------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente.                              |
| 413    | Carga demasiado grande       | El archivo cargado supera el límite de tamaño.            |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                           |

{{< /tab >}}

{{< /tabs >}}

- **Familia de SDK en la nube**

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}