---
title: "Eliminar un filtro de fecha – Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Eliminar filtro de fecha"
type: docs
url: /autofilter/delete-date-filter/
aliases:
  - /remove-a-date-filter/
  - /autofilter/delete-a-date-filter/
weight: 100
keywords: "Aspose.Cells, eliminar filtro de fecha, filtro automático de Excel, API REST, SDK"
description: "Aprenda cómo eliminar un filtro de fecha de una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye el punto de conexión, parámetros, ejemplo de cURL con HTTPS, carga útil de respuesta y ejemplos de código del SDK."
ArticleTitle: "Eliminar un filtro de fecha – Documentación de la API Aspose.Cells Cloud"
---

Esta API REST elimina un filtro de fecha en una hoja de cálculo de Excel.

**Prerrequisitos:** Asegúrese de tener un token JWT válido, el libro esté almacenado en el almacenamiento de Aspose Cloud y tenga los permisos adecuados para modificar la hoja de cálculo.

## API DeleteWorksheetDateFilter

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro   | Tipo    | Ubicación | Descripción                                                                                     |
|------------------------|---------|-----------|-------------------------------------------------------------------------------------------------|
| name                   | string  | path      | Nombre del archivo de Excel.                                                                    |
| sheetName              | string  | path      | Nombre de la hoja de cálculo.                                                                   |
| fieldIndex             | integer | query     | Índice de base cero de la columna a la que se aplica el filtro.                                 |
| dateTimeGroupingType   | string  | query     | Tipo de agrupación para el filtro de fecha (por ejemplo, Year, Month, Day).                    |
| year                   | integer | query     | Componente de año del filtro (valor predeterminado: 0).                                         |
| month                  | integer | query     | Componente de mes del filtro (valor predeterminado: 0).                                         |
| day                    | integer | query     | Componente de día del filtro (valor predeterminado: 0).                                         |
| hour                   | integer | query     | Componente de hora del filtro (valor predeterminado: 0).                                        |
| minute                 | integer | query     | Componente de minuto del filtro (valor predeterminado: 0).                                      |
| second                 | integer | query     | Componente de segundo del filtro (valor predeterminado: 0).                                     |
| folder                 | string  | query     | Ruta de carpeta en el almacenamiento donde se encuentra el archivo.                             |
| storageName            | string  | query     | Nombre del almacenamiento de Aspose Cloud.                                                      |

### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente. |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

La API devuelve códigos de estado HTTP estándar que indican el resultado de la operación de eliminación.

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200    | OK          | El filtro de fecha se eliminó correctamente; la respuesta contiene el estado de la operación. |
| 400    | Solicitud incorrecta | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado | Token JWT no válido o ausente. |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño. |
| 500    | Error interno del servidor | Error inesperado en el servidor. |

## Cómo usar la API DeleteWorksheetDateFilter con SDK

### Especificación de la API DeleteWorksheetDateFilter

La <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetDateFilter" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?fieldIndex=0&dateTimeGroupingType=Year&year=1920" \
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

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel, para que usted pueda centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}