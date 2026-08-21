---
title: "Actualizar un objeto de lista en una hoja de cálculo de Excel"
ArticleTitle: "Actualizar un objeto de lista o tabla dentro de la hoja de cálculo – Documentación de la API de Aspose.Cells Cloud"
second_title: "Documento"
linktype: "docs"
url: /es/list-objects/update/
aliases:
  - /update-a-list-object-or-table-inside-the-worksheet/
  - /tables/update/
keywords: "Aspose.Cells, ListObject, Actualizar tabla, API de Excel, REST, SDK en la nube, actualización de objeto de lista, hoja de cálculo de Excel, tabla"
description: "Aprenda cómo actualizar una tabla de Excel mediante la API de Aspose.Cells Cloud (v3.0). Incluye el punto de conexión, los parámetros, un ejemplo de cURL, códigos de error y ejemplos de SDK."
weight: 20
---

Esta API de REST actualiza las propiedades de un **objeto de lista** (tabla) en una hoja de cálculo de Excel.

## Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Esquema del cuerpo de la solicitud

El DTO `listObject` contiene los siguientes campos. Solo son obligatorios en el cuerpo de la solicitud los campos que desee modificar.

| Campo                                           | Tipo               | Obligatorio | Descripción                                                                |
| ----------------------------------------------- | ------------------ | ----------- | -------------------------------------------------------------------------- |
| **DisplayName**                                 | string             | opcional    | Nombre que se muestra para la tabla.                                       |
| **StartRow** / **StartColumn**                  | integer            | opcional    | Índice en base cero de la primera fila/columna de la tabla.                |
| **EndRow** / **EndColumn**                      | integer            | opcional    | Índice en base cero de la última fila/columna de la tabla.                 |
| **Range**                                       | string             | opcional    | Dirección estilo A1 que define el rango de la tabla (por ejemplo, `A1:D10`). |
| **ShowHeaderRow**                               | boolean            | opcional    | `true` para mostrar la fila de encabezados.                                |
| **ShowTotals**                                  | boolean            | opcional    | `true` para mostrar la fila de totales.                                    |
| **TableStyleName**                              | string             | opcional    | Nombre del estilo de tabla integrado que se aplicará.                      |
| **TableStyleType**                              | string             | opcional    | Tipo de estilo (`TableStyleLight`, `TableStyleMedium`, etc.).              |
| **ListColumns**                                 | matriz de objetos  | opcional    | Colección de definiciones de columnas (`Name`, `TotalsCalculation`).      |
| **Sorter**, **AutoFilter**, **ShowTableStyle…** | objeto             | opcional    | Opciones avanzadas de estilo y filtrado (consulte el DTO completo en la especificación OpenAPI). |

### Ejemplo mínimo de carga útil

```json
{
  "DisplayName": "SalesData",
  "Range": "A1:E20",
  "ShowHeaderRow": true,
  "ShowTotals": false
}
```

## API de REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                |
| -------------------- | ------ | --------- | ------------------------------------------ |
| **name**             | string | path      | Nombre del documento.                      |
| **sheetName**        | string | path      | Nombre de la hoja de cálculo.              |
| **listObjectIndex**  | integer| path      | Índice del objeto de lista que se va a actualizar. |
| **listObject**       | object | body      | DTO `ListObject` en el cuerpo de la solicitud. |
| **folder**           | string | query     | Carpeta que contiene el documento.         |
| **storageName**      | string | query     | Nombre del almacenamiento.                 |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Solicitud

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "DisplayName": "SalesData",
    "Range": "A1:E20",
    "ShowHeaderRow": true,
    "ShowTotals": false,
    "ListColumns": [
      { "Name": "Product", "TotalsCalculation": "None" },
      { "Name": "Quantity", "TotalsCalculation": "Sum" },
      { "Name": "Price", "TotalsCalculation": "Average" }
    ]
  }'
```

{{< /tab >}}

### Respuesta

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

La respuesta correcta incluye los siguientes campos:

| Campo                  | Tipo   | Descripción                                          |
| ---------------------- | ------ | ---------------------------------------------------- |
| Code                   | integer| Código de estado HTTP (200 para éxito).             |
| Status                 | string | Descripción textual del estado.                     |
| UpdatedObject *(opcional)* | object | Representación del `ListObject` actualizado, que contiene las propiedades modificadas. |

{{< /tab >}}

{{< /tabs >}}

## Respuestas de error

| Código HTTP | Descripción                                                                 | Carga útil de ejemplo                                  |
| ----------- | --------------------------------------------------------------------------- | ------------------------------------------------------ |
| **400**     | Solicitud incorrecta: faltan campos obligatorios o JSON mal formado.       | `{ "Code": 400, "Message": "Invalid request body." }`  |
| **401**     | No autorizado: el token JWT falta o no es válido.                          | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**     | No encontrado: el libro, la hoja de cálculo o el objeto de lista especificados no existen. | `{ "Code": 404, "Message": "Resource not found." }`    |
| **500**     | Error interno del servidor: condición inesperada en el lado del servidor.  | `{ "Code": 500, "Message": "Server error." }`          |

## Preguntas frecuentes

<details>  
<summary>¿Cómo actualizo un objeto de lista mediante la API de Aspose.Cells Cloud?</summary>

Utilice el punto de conexión `POST /cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}`. Incluya un cuerpo JSON con las propiedades que desee modificar (por ejemplo, `DisplayName`, `ShowHeaderRow`). Autentíquese mediante un token JWT en el encabezado `Authorization`.

</details>

<details>  
<summary>¿Qué respuesta recibo tras una actualización correcta?</summary>

Se devuelve un objeto JSON con `Code: 200` y `Status: "OK"`. Si se produce un error, la respuesta incluye el código de estado HTTP correspondiente y un objeto `Error` que describe el problema.

</details>

<details>  
<summary>¿Puedo actualizar solo un subconjunto de las propiedades del objeto de lista?</summary>

Sí. Incluya solo los campos que desee modificar en el cuerpo de la solicitud; todos los campos omitidos permanecerán sin cambios.

</details>

## Documentación relacionada

- [Agregar un objeto de lista](https://docs.aspose.cloud/cells/list-objects/add/)
- [Obtener objeto de lista](https://docs.aspose.cloud/cells/list-objects/get/)
- [Eliminar objeto de lista](https://docs.aspose.cloud/cells/list-objects/delete/)

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted se enfoque en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}