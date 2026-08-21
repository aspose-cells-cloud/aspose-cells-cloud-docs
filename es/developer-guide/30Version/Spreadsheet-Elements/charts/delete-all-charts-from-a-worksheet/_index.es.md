---
title: "Eliminar todos los gráficos de una hoja de cálculo"
type: docs
url: /es/charts/clear/
aliases: [  /es/delete-all-charts-from-a-worksheet/ ]
weight: 30
keywords: "Aspose.Cells, Cloud, eliminar, todos los gráficos, hoja de cálculo, REST API, DELETE, SDK"
description: "Aprenda cómo eliminar todos los gráficos de una hoja de cálculo utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye el endpoint, parámetros, ejemplo con cURL, fragmentos de código SDK, pasos de autenticación y manejo de errores."
ArticleTitle: "Eliminar todos los gráficos de una hoja de cálculo mediante la API de Aspose.Cells Cloud"
---

Esta API REST elimina todos los gráficos de la hoja de cálculo especificada.

**Antecedentes**: Eliminar todos los gráficos de una hoja de cálculo es útil cuando necesita restablecer el diseño visual de una hoja, reemplazar visualizaciones desactualizadas o preparar un libro para su reutilización sin conservar los datos de gráficos anteriores.

Antes de llamar a la API, asegúrese de cumplir con los siguientes requisitos previos:

- Disponga de un token JWT válido para la autenticación.  
- El archivo del libro exista en la ubicación y carpeta especificadas en el almacenamiento.  
- Esté utilizando la versión de la API **v3.0**.

## DeleteWorksheetClearCharts API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                  |
| --------------------- | ------ | --------- | -------------------------------------------- |
| name                  | string | path      | Nombre del archivo del libro.                |
| sheetName             | string | path      | Nombre de la hoja de cálculo.                |
| folder                | string | query     | Carpeta donde se almacena el libro.         |
| storageName           | string | query     | Nombre del almacenamiento.                   |

**Encabezados de solicitud**

| Encabezado      | Descripción                           |
|-----------------|---------------------------------------|
| Authorization   | Bearer `<jwt token>`                  |
| Accept          | `application/json`                    |
| Content-Type    | `application/json` (sin cuerpo)       |

**Cuerpo de la solicitud**

La operación DELETE **no requiere** un cuerpo de solicitud.

**Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                    |
|--------|-----------------------------|----------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (p. ej., tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                                 |
| 413    | Payload demasiado grande    | El archivo cargado excede el límite de tamaño.                |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                               |

*Ejemplos de respuestas de error*

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "Parámetro no válido: se requiere 'sheetName'."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "La autenticación falló. Token JWT inválido."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "La carga útil de la solicitud supera el tamaño máximo permitido."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "Se produjo un error inesperado en el servidor."
}
```

## Cómo usar la API DeleteWorksheetClearCharts con SDKs

### Especificación de la API DeleteWorksheetClearCharts

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetClearCharts) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts" \
-X DELETE \
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

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor manera de acelerar el desarrollo cuando necesita **eliminar todos los gráficos** de una hoja de cálculo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteAllCharts-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetClearCharts-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-clear_the_charts-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteAllChartsFromAWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteAllCharts-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteAllCharts-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1775c5a8985efa819486b7ede2c34bfc" >}}

{{< /tab >}}

{{< /tabs >}}