---
title: "Obtener celdas fusionadas de una hoja de cálculo de Excel – Aspose.Cells Cloud API"
type: docs
url: /es/get-mergedcell-from-a-worksheet/
weight: 60
keywords: "Aspose.Cells Cloud, celdas fusionadas, hoja de cálculo de Excel, API REST, Aspose.Cells SDK, celdas fusionadas en Excel"
description: "Aprenda cómo recuperar rangos de celdas fusionadas de una hoja de cálculo de Excel utilizando la API de Aspose.Cells Cloud (v3.0). Incluye pasos de autenticación, solicitud completa con cURL, esquema de respuesta, manejo de errores y ejemplos de SDK en C#, Java, Python y más."
---

Esta API REST devuelve información sobre las **celdas fusionadas** en una hoja de cálculo de Excel.

> **Nota**: El objeto de la API se denomina **MergedCell** (singular). En el texto explicativo nos referimos al *concepto* de celdas fusionadas (plural).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/mergedCells
```

## Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en tokens JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                           |
|----------------------|--------|-----------|---------------------------------------|
| **name**             | string | path      | Nombre del archivo de Excel.          |
| **sheetName**        | string | path      | Nombre de la hoja de cálculo.         |
| **folder**           | string | query     | Carpeta que contiene el documento.    |
| **storageName**      | string | query     | Nombre del almacenamiento a utilizar. |

## **Respuesta**

Devuelve un objeto `MergedCellsResponse`.

```json
{
  "Status":"OK",
  "Code":200,
  "MergedCells":{
    "Count": 0,
    "MergedCellList":[
      {
        "Link":{
          "Href":"",
          "Rel":"",
          "Type":"",
          "Title":""
        }
      }
    ]
  }
}
```

**Códigos de estado HTTP**

| Código | Significado                | Descripción                                                    |
|--------|----------------------------|----------------------------------------------------------------|
| 200    | OK                         | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta       | Parámetros faltantes o no válidos (p. ej., tipo de archivo no admitido). |
| 401    | No autorizado              | Token JWT inválido o ausente.                                  |
| 413    | Payload demasiado grande   | El archivo cargado supera el límite de tamaño.                |
| 500    | Error interno del servidor | Error inesperado en el servidor.                               |

## Cómo usar la API GetWorksheetMergedCells con SDK

### Especificación de la API GetWorksheetMergedCells

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetMergedCells) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos `cURL` para acceder fácilmente a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo realizar una llamada a la API en la nube mediante `cURL`.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/mergedCells" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MergedCells": {
    "Count": 1,
    "MergedCells": [
      {
      "link": {
            "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/cells/mergedcells/0",
            "Rel": "self"
          }
      }
    ]    
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar contra la API. Un SDK maneja los detalles de bajo nivel, lo que le permite centrarse en la lógica de su negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetMergedCells.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetMergedCells.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetMergedCells.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetMergedCells.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetMergedCells.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetMergedCells.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetMergedCells.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetMergedCells.go" >}}

{{< /tab >}}

{{< /tabs >}}