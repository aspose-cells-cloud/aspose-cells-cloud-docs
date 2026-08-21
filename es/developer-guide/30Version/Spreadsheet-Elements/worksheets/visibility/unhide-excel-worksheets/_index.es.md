---
title: "Mostrar una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Mostrar"
type: docs
url: /es/worksheets/unhide/
aliases: [  /es/unhide-excel-worksheets/ ]
keywords: "Aspose.Cells, mostrar hoja de cálculo, API de Excel, hoja de cálculo en la nube, REST, visibilidad de hoja de cálculo, libro de Excel"
description: "Aprenda cómo utilizar la API REST de Aspose.Cells Cloud para mostrar una hoja de cálculo en un libro de Excel. Incluye detalles de la solicitud, ejemplos de cURL y fragmentos de código de SDK para múltiples lenguajes de programación."
weight: 60
---

Esta API REST proporciona un punto final para **mostrar una hoja de cálculo** en un libro de Excel.

**Prerrequisitos**  
Antes de llamar a esta operación, debe tener:

* Un token de acceso válido de Aspose Cloud (JWT) incluido en el encabezado `Authorization`.  
* El libro almacenado en una ubicación de almacenamiento compatible que especifique mediante los parámetros de consulta `folder` y `storageName`.  
* El libro debe estar en un formato compatible con Aspose.Cells (por ejemplo, `.xls`, `.xlsx`, `.xlsm`).  

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                |
| -------------------- | ------- | --------- | ------------------------------------------ |
| name                 | string  | path      | Nombre del documento.                      |
| sheetName            | string  | path      | Nombre de la hoja de cálculo.              |
| isVisible            | boolean | query     | Nuevo valor de visibilidad de la hoja (`true`). |
| folder               | string  | query     | Carpeta del documento.                     |
| storageName          | string  | query     | Nombre del almacenamiento.                 |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet) define una interfaz de programación pública accesible que le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para llamar fácilmente a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo realizar una solicitud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"   # reemplace <jwt token> con su token de acceso
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Códigos de respuesta posibles**

| Código HTTP | Significado                                              | Cuerpo de ejemplo (cuando corresponda)                              |
|-------------|----------------------------------------------------------|----------------------------------------------------------------------|
| 200         | Visibilidad de la hoja de cálculo actualizada correctamente | `{ "Code": 200, "Status": "OK" }`                                   |
| 400         | Solicitud incorrecta: parámetros faltantes o no válidos | `{ "Code": 400, "Message": "Invalid request parameters." }`        |
| 401         | No autorizado: token JWT faltante o no válido           | `{ "Code": 401, "Message": "Authentication failed." }`             |
| 404         | No encontrado: el libro o la hoja de cálculo no existen | `{ "Code": 404, "Message": "File or worksheet not found." }`       |
| 500         | Error interno del servidor                              | `{ "Code": 500, "Message": "An unexpected error occurred." }`      |

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Perl" tabName8="Android" tabName9="Objective C" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-UnhideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnhideExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnhideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnhideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e30ac521e9cdb174baa702a743be16ae" >}}

{{< /tab >}}

{{< /tabs >}}