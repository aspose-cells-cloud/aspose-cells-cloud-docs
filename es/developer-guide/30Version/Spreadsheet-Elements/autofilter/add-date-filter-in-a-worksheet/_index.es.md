---
title: "Agregar filtro de fecha a una hoja de cálculo de Excel"
second_title: "Document"
linktype: "add-date-filter"
type: docs
url: /es/autofilter/add-date-filter/
aliases:
  - /add-date-filter-in-a-worksheet/
  - /autofilter/add-a-date-filter/
description: "Aprenda cómo agregar un filtro de fecha a una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye un ejemplo con cURL, fragmentos de código para SDK (C#, Java, Python, etc.), parámetros y manejo de errores."
weight: 65
ArticleTitle: "Agregar filtro de fecha a una hoja de cálculo de Excel | Aspose.Cells Cloud API"
keywords: "Aspose.Cells, filtro de fecha en Excel, API de AutoFilter, API REST, SDK en la nube, cURL, automatización de hojas de cálculo"
---

Esta API REST agrega un **filtro de fecha** a una hoja de cálculo de Excel.

**Requisitos previos:** Debe tener un token JWT válido y el libro de trabajo de destino ya debe existir en la ubicación de almacenamiento especificada. La solicitud no requiere un cuerpo JSON.

## API PutWorksheetDateFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud


| Nombre del parámetro       | Tipo    | Ubicación | Descripción                                                                                                                                                     |
| -------------------------- | ------- | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                   | string  | Ruta      | Nombre del libro de trabajo.                                                                                                                                   |
| **sheetName**              | string  | Ruta      | Nombre de la hoja de cálculo.                                                                                                                                  |
| **range**                  | string  | Consulta  | Rango de Excel al que se aplica el filtro (por ejemplo, `A1:B1`).                                                                                              |
| **fieldIndex**             | integer | Consulta  | Índice de base cero de la columna que se va a filtrar.                                                                                                         |
| **dateTimeGroupingType**   | string  | Consulta  | Tipo de agrupación para el filtro de fecha/hora. Los valores permitidos son `Day`, `Hour`, `Minute`, `Month`, `Second`, `Year`. Los valores distinguen mayúsculas y minúsculas; el valor predeterminado es `Day`. |
| **year**                   | integer | Consulta  | Componente de año del valor del filtro.                                                                                                                        |
| **month**                  | integer | Consulta  | Componente de mes del valor del filtro.                                                                                                                        |
| **day**                    | integer | Consulta  | Componente de día del valor del filtro.                                                                                                                        |
| **hour**                   | integer | Consulta  | Componente de hora del valor del filtro.                                                                                                                       |
| **minute**                 | integer | Consulta  | Componente de minuto del valor del filtro.                                                                                                                     |
| **second**                 | integer | Consulta  | Componente de segundo del valor del filtro.                                                                                                                    |
| **matchBlanks**            | boolean | Consulta  | Incluir celdas en blanco (`true` o `false`).                                                                                                                  |
| **refresh**                | boolean | Consulta  | Actualizar el filtro tras aplicarlo (`true` o `false`).                                                                                                        |
| **folder**                 | string  | Consulta  | Ruta de la carpeta del libro de trabajo original.                                                                                                              |
| **storageName**            | string  | Consulta  | Nombre del servicio de almacenamiento.                                                                                                                         |

*La solicitud PUT no requiere un cuerpo de solicitud; todos los parámetros se suministran a través de la cadena de consulta.*

### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Bad Request                 | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | Unauthorized                | Token JWT no válido o faltante.                                             |
| 413    | Payload Too Large           | El archivo cargado excede el límite de tamaño.                             |
| 500    | Internal Server Error       | Error inesperado del servidor.                                              |

## Cómo usar la API PutWorksheetDateFilter con SDK

### Especificación de la API PutWorksheetDateFilter

La <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación pública accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
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



### Utilizar los SDK de Aspose.Cells Cloud

Usar un SDK es la forma más rápida de desarrollar. Un SDK maneja los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}