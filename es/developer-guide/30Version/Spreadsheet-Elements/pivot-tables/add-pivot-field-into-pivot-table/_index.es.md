---
title: "Agregar un campo de pivote a una tabla dinámica"
second_title: "Document"
linktype: "Add Pivot Field"
type: docs
url: /es/pivot-tables/add-pivot-field/
aliases: [  /es/add-a-pivot-table-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, tabla dinámica, agregar campo de pivote, REST API, SDK"
description: "Agregue un campo de pivote a una tabla dinámica existente mediante la API REST de Aspose.Cells Cloud. Incluye detalles de la solicitud, ejemplo de cURL y fragmentos de SDK."
weight: 40
ArticleTitle: "Agregar un campo de pivote a una tabla dinámica – Documentación de Aspose.Cells Cloud"
---

Esta **API REST** **agrega** un campo de pivote a una tabla dinámica existente.

> **Requisito previo:** Para llamar a este punto de conexión, debe incluir un token de autenticación JWT válido en el encabezado `Authorization` y asegurarse de que el libro esté almacenado en la carpeta especificada o en el almacenamiento predeterminado.

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                     |
|----------------------|---------|-----------|-----------------------------------------------------------------|
| name                 | string  | path      | Nombre del documento.                                           |
| sheetName            | string  | path      | Nombre de la hoja de cálculo.                                   |
| pivotTableIndex      | integer | path      | Índice de la tabla dinámica.                                    |
| pivotFieldType       | string  | query     | Tipo del área de campos (por ejemplo, Row, Column).            |
| request              | object  | body      | DTO que contiene los índices de campo que se van a agregar.    |
| needReCalculate      | boolean | query     | Establecer en **true** para recalcular la tabla dinámica tras la operación. |
| folder               | string  | query     | Carpeta donde se almacena el documento.                         |
| storageName          | string  | query     | Nombre del almacenamiento.                                      |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutPivotTableField) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para llamar a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo agregar un campo de pivote mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/PivotField?pivotFieldType=Row" \
  -X PUT \
  -d '{"Data":[1,2]}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

La respuesta correcta devuelve un objeto JSON con los campos `Code` y `Status`. Ejemplo de esquema:

```json
{
  "Code": 0,        // entero que indica el código de estado HTTP
  "Status": "OK"    // mensaje de texto
}
```

Las posibles respuestas de error incluyen **400 Bad Request** para parámetros faltantes, **401 Unauthorized** si el token no es válido y **500 Internal Server Error** para problemas del lado del servidor.

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de integrar esta funcionalidad. Los SDK manejan los detalles de bajo nivel, lo que le permite centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivotFieldInPivottable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotFieldInPivotTable.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivotFieldInPivottable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivotFieldInPivottable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "8f9b66d50f7cfa2b14c24fa7ddb396e7" >}}

{{< /tab >}}

{{< /tabs >}}

**Consulte también:**  
- [Agregar una tabla dinámica](https://docs.aspose.cloud/cells/pivot-tables/add-pivot-table/)  
- [Eliminar campo de pivote](https://docs.aspose.cloud/cells/pivot-tables/delete-pivot-field/)