---
title: "Obtener propiedades de celdas"
type: docs
url: /get-cells-properties/
weight: 130
keywords: "Aspose Cells Cloud, REST API, Excel, hoja de cálculo, propiedades de celdas, obtener propiedades de celdas"
description: "Aprenda a usar la API REST de Aspose.Cells Cloud para recuperar las propiedades de una celda específica o de métodos predefinidos de celdas en una hoja de cálculo de Excel."
---

Esta API REST demuestra cómo recuperar una celda específica en un archivo de Excel.

## API REST

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
```

## Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en tokens JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parámetros de solicitud


| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                                                                                                           |
| -------------------- | ------ | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**             | string | path     | El nombre del documento de Excel.                                                                                                                                                       |
| **sheetName**        | string | path     | El nombre de la hoja de cálculo que contiene la celda.                                                                                                                                        |
| **cellOrMethodName** | string | path     | El nombre de la celda o el nombre de un método predefinido (por ejemplo, `firstcell`, `endcell`, `maxrow`, `maxdatarow`, `maxcolumn`, `maxdatacolumn`, `minrow`, `mindatarow`, `mincolumn`, `mindatacolumn`). |
| **folder**           | string | query    | La carpeta donde se almacena el documento.                                                                                                                                              |
| **storageName**      | string | query    | El nombre del servicio de almacenamiento.                                                                                                                                                      |

## **Respuesta**

Devuelve un objeto CellResponse.

- **Resumen de campos de respuesta**

| Campo           | Tipo    | Descripción                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Name`          | string  | Dirección de la celda (por ejemplo, `F341`).                   |
| `Row`           | integer | Índice de fila (base cero).                                 |
| `Column`        | integer | Índice de columna (base cero).                              |
| `Value`         | string  | Valor mostrado por la celda.                           |
| `Type`          | string  | Tipo de datos de la celda (por ejemplo, `IsString`).             |
| `Formula`       | string  | Texto de la fórmula si la celda contiene una.          |
| `IsFormula`     | bool    | Indica si la celda contiene una fórmula.        |
| `IsMerged`      | bool    | Indica si la celda forma parte de un rango fusionado. |
| `IsArrayHeader` | bool    | Indica si la celda es un encabezado de matriz.        |
| `IsInArray`     | bool    | Indica si la celda pertenece a una matriz.       |
| `IsErrorValue`  | bool    | Indica si la celda contiene un valor de error.   |
| `IsInTable`     | bool    | Indica si la celda está dentro de una tabla.         |
| `IsStyleSet`    | bool    | Indica si se aplica un estilo a la celda.     |
| `HtmlString`    | string  | Representación codificada en HTML del valor de la celda.      |
| `Style.link`    | object  | Hipervínculo al recurso de estilo.                      |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "Hello Aspose.Cells",
    "Type":"String",
    "Formula" : "",
    ...
  }
}
```

**Códigos de estado HTTP**

| Código | Significado                     | Descripción                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400  | Solicitud incorrecta                 | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401  | No autorizado                | Token JWT inválido o ausente. |
| 413  | Carga útil demasiado grande           | El archivo subido excede el límite de tamaño. |
| 500  | Error interno del servidor       | Error inesperado en el servidor. |
## Cómo usar la API GetWorksheetCell con SDK

### Especificación de la API GetWorksheetCell


La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.
{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Statistical",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más eficiente de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

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

### Cómo recuperar una celda específica

- [Obtener datos de celda desde una hoja de cálculo](/cells/get-cell-data-from-a-worksheet/)
- [Obtener la primera celda de una hoja de cálculo de Excel](/cells/get-first-cell-from-excel-worksheet/)
- [Obtener la última celda de una hoja de cálculo de Excel](/cells/get-last-cell-of-excel-worksheet/)
- [Obtener MaxRow de una hoja de cálculo de Excel](/cells/get-maxrow-from-excel-worksheet/)
- [Obtener MaxDataRow de una hoja de cálculo de Excel](/cells/get-maxdatarow-from-excel-worksheet/)
- [Obtener MaxColumn de una hoja de cálculo de Excel](/cells/get-maxcolumn-from-excel-worksheet/)
- [Obtener MaxDataColumn de una hoja de cálculo de Excel](/cells/get-maxdatacolumn-from-excel-worksheet/)
- [Obtener MinRow de una hoja de cálculo de Excel](/cells/get-minrow-from-excel-worksheet/)
- [Obtener MinDataRow de una hoja de cálculo de Excel](/cells/get-mindatarow-from-excel-worksheet/)
- [Obtener MinColumn de una hoja de cálculo de Excel](/cells/get-mincolumn-from-excel-worksheet/)
- [Obtener MinDataColumn de una hoja de cálculo de Excel](/cells/get-mindatacolumn-from-excel-worksheet/)