---
title: "Ordenar datos de ListObject en una hoja de cálculo de Excel"
second_title: "Document"
linktype: "Sort"
type: docs
url: /es/list-objects/sort-data/
aliases: [/get-a-list-object-or-table-inside-the-worksheet/, /tables/sort-data/]
keywords: "Aspose.Cells Cloud, Excel, ListObject, Ordenar datos, API REST, Hoja de cálculo"
description: "Aprenda cómo ordenar los datos de un ListObject (tabla) en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye el endpoint, los parámetros, una solicitud de ejemplo con cURL y ejemplos de SDK."
weight: 40
ArticleTitle: "Ordenar datos de ListObject en una hoja de cálculo de Excel – API de Aspose.Cells Cloud"
---

**Requisitos previos**  
Para invocar esta API, debe disponer de un token de acceso JWT válido de Aspose Cloud y el libro debe haberse cargado previamente en el almacenamiento de Aspose Cloud. Incluya el encabezado `Authorization: Bearer <jwt token>` en cada solicitud.

Esta API REST ordena los datos de una tabla en una hoja de cálculo de Excel.  
Para utilizar esta operación, proporcione el nombre del libro, el nombre de la hoja de cálculo y el índice del ListObject objetivo, junto con un cuerpo JSON `dataSorter` que defina los criterios de ordenación.

## API PostWorksheetListObjectSortTable

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/sort
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                     |
| --------------------- | ------- | --------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| name                  | string  | path                                    | Nombre del archivo de Excel almacenado en el almacenamiento de Aspose Cloud.                                   |
| sheetName             | string  | path                                    | Nombre de la hoja de cálculo que contiene el ListObject.                                                       |
| listObjectIndex       | integer | path                                    | Índice de base cero del ListObject (tabla) dentro de la hoja de cálculo.                                        |
| dataSorter            | object  | body                                    | Objeto JSON que especifica las opciones de ordenación (por ejemplo, `CaseSensitive`, `HasHeaders`, `KeyList`, `SortLeftToRight`). |
| folder                | string  | query                                   | Ruta de carpeta dentro del almacenamiento donde se encuentra el archivo de Excel.                              |
| storageName           | string  | query                                   | Nombre del almacenamiento de Aspose Cloud.                                                                     |

**Notas**  
El cuerpo de la solicitud debe ser un objeto JSON válido que coincida con el esquema `dataSorter`. Asegúrese de que el libro, la hoja de cálculo y el ListObject existan antes de invocar la operación de ordenación.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSortTable) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet7/listobjects/1/sort" \
  -X POST \
  -d '{
        "CaseSensitive": true,
        "HasHeaders": true,
        "KeyList": [
          {
            "Key": 1,
            "SortOrder": "Ascending",
            "CustomList": "string"
          }
        ],
        "SortLeftToRight": true
      }' \
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

**Códigos de estado HTTP**

| Código de estado | Descripción                                     |
|------------------|-------------------------------------------------|
| 200              | OK – ordenación completada correctamente.      |
| 400              | Solicitud incorrecta – parámetros no válidos.  |
| 401              | No autorizado – error de autenticación.        |
| 404              | No encontrado – libro, hoja de cálculo o ListObject no hallado. |
| 500              | Error interno del servidor – problema del lado del servidor. |

**Parámetros de respuesta**

| Parámetro | Tipo    | Descripción                                      |
|-----------|---------|--------------------------------------------------|
| Code      | integer | Código de estado HTTP devuelto por la API.      |
| Status    | string  | Descripción textual del resultado (por ejemplo, "OK"). |

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectSortTable.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectSortTable.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectSortTable.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectSortTable.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectSortTable.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectSortTable.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectSortTable.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectSortTable.go" >}}

{{< /tab >}}

{{< /tabs >}}

[Volver a la vista general de ListObjects](/list-objects/)