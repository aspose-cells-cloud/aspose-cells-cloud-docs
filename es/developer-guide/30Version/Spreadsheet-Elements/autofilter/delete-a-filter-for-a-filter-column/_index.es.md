---
title: "Eliminar un filtro de una hoja de cálculo de Excel – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Eliminar filtro"
type: docs
url: /es/delete-filter/
aliases: [/delete-a-filter-for-a-filter-column/, /delete-auto-filter/]
keywords: "Aspose.Cells Cloud, eliminar filtro, Excel, REST API, SDK"
description: "Aprenda cómo eliminar un filtro automático de una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud, cURL y SDKs (C#, Java, Python, etc.). Incluye endpoint, parámetros, autenticación y código de ejemplo."
weight: 100
---

## API REST

Esta API REST elimina un **filtro automático** en una hoja de cálculo de Excel.

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro       | Tipo    | Ubicación | ¿Obligatorio? | Descripción                                                                                      |
| -------------------------- | ------- | --------- | ------------- | ------------------------------------------------------------------------------------------------ |
| **name**                   | string  | Ruta      | Sí            | Nombre del libro.                                                                                |
| **sheetName**              | string  | Ruta      | Sí            | Nombre de la hoja de cálculo.                                                                    |
| **range**                  | string  | Consulta  | No            | Rango de celdas al que se aplica el filtro (por ejemplo, `A1:C10`).                              |
| **fieldIndex**             | integer | Consulta  | Sí            | Índice de base cero de la columna a la que se aplica el filtro.                                  |
| **dateTimeGroupingType**   | string  | Consulta  | No            | Cómo se agrupan los valores de fecha/hora: `Day`, `Hour`, `Minute`, `Month`, `Second` o `Year`. |
| **year**                   | integer | Consulta  | No            | Componente de año para la agrupación de fechas.                                                  |
| **month**                  | integer | Consulta  | No            | Componente de mes para la agrupación de fechas.                                                  |
| **day**                    | integer | Consulta  | No            | Componente de día para la agrupación de fechas.                                                  |
| **hour**                   | integer | Consulta  | No            | Componente de hora para la agrupación de fechas.                                                 |
| **minute**                 | integer | Consulta  | No            | Componente de minuto para la agrupación de fechas.                                               |
| **second**                 | integer | Consulta  | No            | Componente de segundo para la agrupación de fechas.                                              |
| **matchBlanks**            | boolean | Consulta  | No            | `true` / `false` – si se incluyen celdas en blanco en el filtro.                                |
| **refresh**                | boolean | Consulta  | No            | `true` / `false` – si se debe actualizar la hoja de cálculo tras la eliminación.                |
| **folder**                 | string  | Consulta  | No            | Carpeta original del libro.                                                                      |
| **storageName**            | string  | Consulta  | No            | Nombre del almacenamiento.                                                                       |

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
| 200    | OK                          | Filtro eliminado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                                              |
| 413    | Payload demasiado grande     | El archivo subido excede el límite de tamaño.                              |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                                            |

## Cómo usar la API DeleteWorksheetFilter con SDKs

### Especificación de la API DeleteWorksheetFilter

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&dateTimeGroupingType=Year" \
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

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDKs de Aspose.Cells Cloud

Utilizar un SDK es la forma más eficiente de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}