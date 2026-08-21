---
title: "Agregar un objeto de lista (tabla) a una hoja de cálculo de Excel"
second_title: "Document"
linktype: "add"
type: docs
url: /es/list-objects/add/
aliases: [  /es/add-a-list-object-or-table-inside-the-worksheet/ , /es/tables/add/ ]
keywords: "Aspose.Cells Cloud, API de Excel, objeto de lista, tabla, API REST, hoja de cálculo"
description: "Aprenda cómo agregar un objeto de lista (tabla de Excel) a una hoja de cálculo mediante la API REST de Aspose.Cells Cloud. Incluye el punto de conexión, los parámetros, los pasos de autenticación, un ejemplo con cURL y ejemplos de código en SDK."
weight: 10
ArticleTitle: "Agregar un objeto de lista (tabla) a una hoja de cálculo de Excel – Documentación de Aspose.Cells Cloud"
---

Esta API REST agrega un **objeto de lista (tabla)** a una hoja de cálculo de Excel.

Antes de usar este punto de conexión, asegúrese de tener un token JWT válido, de que el libro esté almacenado en un almacenamiento en la nube compatible y de que la hoja de cálculo exista.

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                 |
|----------------------|---------|-----------|-----------------------------------------------------------------------------|
| **name**             | string  | path      | Nombre del archivo del libro.                                               |
| **sheetName**        | string  | path      | Nombre de la hoja de cálculo.                                               |
| **startRow**         | integer | query     | Índice de base cero de la primera fila del rango de la tabla.               |
| **startColumn**      | integer | query     | Índice de base cero de la primera columna del rango de la tabla.            |
| **endRow**           | integer | query     | Índice de base cero de la última fila del rango de la tabla.                |
| **endColumn**        | integer | query     | Índice de base cero de la última columna del rango de la tabla.             |
| **hasHeaders**       | boolean | query     | `true` si la primera fila contiene encabezados de columna; de lo contrario, `false`. |
| **listObject**       | object  | body      | Definición del objeto de lista (véase **Esquema del cuerpo de la solicitud**). |
| **folder**           | string  | query     | Carpeta que contiene el libro.                                              |
| **storageName**      | string  | query     | Nombre del almacenamiento.                                                  |

### Esquema del cuerpo de la solicitud

El objeto **listObject** describe la tabla que se creará. Solo se muestran las propiedades más comunes; consulte la especificación OpenAPI para obtener la lista completa.

```json
{
  "displayName": "MiTabla",
  "showTotals": false,
  "style": "TableStyleMedium2"
}
```

### Ejemplo de solicitud (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "displayName": "MiTabla",
        "showTotals": false,
        "style": "TableStyleMedium2"
      }'
```

### Ejemplo de respuesta

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Códigos de error

| Estado HTTP | Razón                 | Descripción                                              |
|-------------|-----------------------|----------------------------------------------------------|
| **400**     | Solicitud incorrecta  | Parámetros de rango inválidos o cuerpo JSON mal formado. |
| **401**     | No autorizado         | Token JWT ausente o caducado.                            |
| **404**     | No encontrado         | El libro o la hoja de cálculo especificados no existen.  |
| **500**     | Error interno del servidor | Fallo inesperado del lado del servidor.             |

**Ejemplo de respuesta 400**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Invalid range parameters."
}
```

**Ejemplo de respuesta 401**

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Authentication token is missing or expired."
}
```

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject) proporciona el contrato completo para esta operación.

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}