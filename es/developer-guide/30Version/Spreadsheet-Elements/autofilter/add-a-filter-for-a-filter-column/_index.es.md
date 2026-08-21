---
title: "Agregar un filtro en una hoja de cálculo de Excel"
second_title: "Documentos"
linktype: "docs"
url: /autofilter/add-filter/
aliases: [/add-a-filter-for-a-filter-column/]
keywords: "Aspose.Cells, Cloud, Excel, AutoFiltro, Agregar filtro, API REST, SDK"
description: "Aprenda cómo agregar un autofiltro a una columna en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye ejemplos en cURL, SDK y una guía de parámetros."
weight: 60
ArticleTitle: "Agregar un filtro en una hoja de cálculo de Excel mediante Aspose.Cells Cloud"
---

**Prerrequisitos:** Antes de llamar a esta API, debe obtener un token JWT válido, asegurarse de que el libro de trabajo objetivo esté subido al almacenamiento especificado y contar con los permisos necesarios para acceder al archivo. Se recomienda utilizar una versión reciente de cURL (7.68 o posterior) para los ejemplos de línea de comandos.

Esta API REST agrega un filtro para una columna específica en una hoja de cálculo de Excel.

## API PutWorksheetFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción |
|----------------------|---------|-----------|-------------|
| name                 | string  | Path      | Nombre del libro de trabajo. |
| sheetName            | string  | Path      | Nombre de la hoja de cálculo. |
| range                | string  | Query     | Rango de celdas que contiene el filtro (por ejemplo, `A1:B1`). |
| fieldIndex           | integer | Query     | Índice basado en cero de la columna a la que se aplica el filtro. |
| criteria             | string  | Query     | Criterios del filtro (por ejemplo, un valor o expresión). |
| matchBlanks          | boolean | Query     | Establecer en `true` para incluir celdas en blanco en el filtro; de lo contrario, `false`. |
| refresh              | boolean | Query     | Establecer en `true` para actualizar el filtro tras aplicarlo; de lo contrario, `false`. |
| folder               | string  | Query     | Carpeta donde se almacena el libro de trabajo original. |
| storageName          | string  | Query     | Nombre del servicio de almacenamiento. |

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
| 401    | No autorizado               | Token JWT inválido o ausente. |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo utilizar la API PutWorksheetFilter con SDK

### Especificación de la API PutWorksheetFilter

La <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo invocar la API mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" \
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

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK maneja los detalles de bajo nivel, permitiéndole centrarse en su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}