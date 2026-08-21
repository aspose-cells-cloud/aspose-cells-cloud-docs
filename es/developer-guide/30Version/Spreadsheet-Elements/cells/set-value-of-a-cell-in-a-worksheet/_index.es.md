---
title: "Establecer el valor de una celda – Referencia de la API de Aspose.Cells Cloud (v3.0)"  
type: docs  
url: /es/set-value-of-a-cell-in-a-worksheet/  
weight: 70  
keywords: "API de Aspose Cells establecer valor de celda, actualización de celda de Excel mediante REST, ejemplo de cURL de Aspose.Cells Cloud"  
description: "Aprenda cómo establecer el valor de una celda específica en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye sintaxis de solicitud, parámetros, ejemplo HTTPS con cURL y fragmentos de código SDK."  
---  

Esta API REST establece el **valor de la celda** en un archivo de Excel.

## API REST  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```  

## Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


**Parámetros de la solicitud**

| Nombre          | Tipo   | Ubicación | Descripción                                   |
|-----------------|--------|-----------|-----------------------------------------------|
| name            | string | path      | Nombre del documento de Excel (incluyendo la extensión). |
| sheetName       | string | path      | Nombre de la hoja de cálculo (distingue mayúsculas y minúsculas). |
| cellName        | string | path      | Dirección estilo A1 de la celda objetivo (por ejemplo, `A1`). |
| value           | string | query     | Valor que se asignará a la celda. |
| type            | string | query     | Tipo de datos del valor (`int`, `string`, `float`, etc.). |
| formula         | string | query     | Fórmula que se aplicará a la celda (opcional). |
| folder          | string | query     | Carpeta que contiene el documento (opcional). |
| storageName     | string | query     | Nombre del almacenamiento donde reside el archivo (opcional). |

## **Respuesta**

Devuelve un objeto `CellResponse`.

- **Resumen de campos de respuesta**

| Campo           | Tipo    | Descripción                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Name`          | string  | Dirección de la celda (por ejemplo, `F341`).         |
| `Row`           | integer | Índice de fila (base cero).                           |
| `Column`        | integer | Índice de columna (base cero).                        |
| `Value`         | string  | Valor mostrado por la celda.                          |
| `Type`          | string  | Tipo de datos de la celda (por ejemplo, `IsString`).  |
| `Formula`       | string  | Texto de la fórmula si la celda contiene una.         |
| `IsFormula`     | bool    | Indica si la celda contiene una fórmula.              |
| `IsMerged`      | bool    | Indica si la celda forma parte de un rango fusionado. |
| `IsArrayHeader` | bool    | Indica si la celda es una cabecera de matriz.         |
| `IsInArray`     | bool    | Indica si la celda pertenece a una matriz.            |
| `IsErrorValue`  | bool    | Indica si la celda contiene un valor de error.        |
| `IsInTable`     | bool    | Indica si la celda está dentro de una tabla.          |
| `IsStyleSet`    | bool    | Indica si se ha aplicado un estilo a la celda.        |
| `HtmlString`    | string  | Representación codificada en HTML del valor de la celda. |
| `Style.link`    | object  | Hipervínculo al recurso de estilo.                    |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**Códigos de estado HTTP**

| Código | Significado                  | Descripción                                           |
|--------|------------------------------|-------------------------------------------------------|
| 200    | OK                           | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta         | Parámetros ausentes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado                | Token JWT inválido o ausente.                         |
| 413    | Payload demasiado grande      | El archivo cargado supera el límite de tamaño.      |
| 500    | Error interno del servidor   | Error inesperado en el servidor.                     |

## Cómo utilizar la API PostWorksheetCellSetValue con SDK

### Especificación de la API PostWorksheetCellSetValue

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) define una interfaz de programación accesible públicamente, lo que permite a los desarrolladores invocar los puntos finales REST directamente desde un navegador o cualquier cliente HTTP.

Puede utilizar la herramienta de línea de comandos **cURL** para llamar a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo establecer el valor de una celda con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A3",
    "Row": 2,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

El uso de un SDK acelera el desarrollo al manejar detalles de bajo nivel, permitiéndole centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells con distintos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellSetValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellSetValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellSetValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellSetValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellSetValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellSetValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellSetValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellSetValue.go" >}}

{{< /tab >}}

{{< /tabs >}}
---