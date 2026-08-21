---
title: "Mostrar columnas en una hoja de cálculo de Excel"
ArticleTitle: "Mostrar columnas en una hoja de cálculo de Excel: API de Aspose.Cells Cloud"
second_title: "Documentos"
linktitle: "Mostrar"
type: docs
url: /columns/unhide/
aliases:
  [/unhide-columns-in-an-excel-worksheet/, /unhide-columns-in-excel-worksheet/]
keywords: "Aspose.Cells, API en la nube, mostrar columnas, Excel, REST, SDK"
description: "Aprenda a utilizar la API REST de Aspose.Cells Cloud para mostrar columnas en una hoja de cálculo de Excel. Incluye detalles de la solicitud, un ejemplo con cURL y ejemplos de código SDK para varios lenguajes de programación."
weight: 50
---

Esta API REST muestra las columnas de una hoja de cálculo.

**Prerrequisitos**: Todos los puntos de conexión de Aspose.Cells Cloud requieren HTTPS y un token de acceso válido de OAuth 2.0. Asegúrese de haber obtenido un token de acceso y de incluirlo en el encabezado `Authorization` de sus solicitudes.

## API PostUnhideWorksheetColumns

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/unhide
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                       |
| -------------------- | ------- | --------- | ------------------------------------------------- |
| name                 | string  | path      | Nombre del libro de cálculo.                      |
| sheetName            | string  | path      | Nombre de la hoja de cálculo.                     |
| startColumn          | integer | query     | Índice de la primera columna que se procesará.    |
| totalColumns         | integer | query     | Número de columnas que se procesarán.             |
| width                | number  | query     | Anchura deseada de la columna (predeterminado: 50.0). |
| folder               | string  | query     | Carpeta que contiene el documento.                |
| storageName          | string  | query     | Nombre del servicio de almacenamiento.            |

La <a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetColumns" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/unhide?startColumn=1&totalColumns=1&width=15" -H "accept: application/json"
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

**Códigos de estado HTTP típicos**

| Código | Descripción                                         |
|--------|-----------------------------------------------------|
| 200    | OK – Las columnas se mostraron correctamente.      |
| 400    | Solicitud incorrecta – Parámetros inválidos.       |
| 401    | No autorizado – Token ausente o inválido.          |
| 404    | No encontrado – Libro de cálculo o hoja no hallados. |
| 500    | Error interno del servidor – Fallo inesperado.     |

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}