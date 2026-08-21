---
title: "Obtener una forma por índice en una hoja de cálculo de Excel"
second_title: "Document"
linktype: "Get"
type: docs
url: /es/shapes/get/
aliases: [/es/get-a-shape-by-index-inside-the-worksheet/]
keywords: "Aspose.Cells Cloud, API de formas de Excel, obtener forma por índice, forma de hoja de cálculo, API REST, recuperación de formas, Aspose.Cells SDK"
description: "Recuperar una forma por su índice en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye sintaxis de solicitud, parámetros, detalles de respuesta y ejemplos de SDK."
weight: 20
ArticleTitle: "Obtener una forma por índice en una hoja de cálculo de Excel – Documentación de Aspose.Cells Cloud"
---

Esta API REST recupera una forma (incluidos sus datos de imagen o metadatos) desde una hoja de cálculo de Excel.

## API GetWorksheetShape

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

**Prerrequisitos**  
- Un token de acceso válido de Aspose Cloud (Bearer JWT).  
- El libro de cálculo debe estar almacenado en su almacenamiento de Aspose Cloud o en una carpeta especificada.  

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                         |
| --------------------- | ------- | --------- | --------------------------------------------------- |
| name                  | string  | path      | Nombre del documento de Excel.                      |
| sheetName             | string  | path      | Nombre de la hoja de cálculo que contiene la forma. |
| shapeindex            | integer | path      | Índice de base cero de la forma dentro de la hoja.  |
| folder                | string  | query     | Ruta de la carpeta donde se almacena el documento.  |
| storageName           | string  | query     | Nombre del servicio de almacenamiento.              |

**Nota:** `shapeindex` es de base cero; la primera forma tiene índice 0. Asegúrese de que el libro esté almacenado en la `folder` y `storageName` especificadas si no utiliza el almacenamiento predeterminado.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
# Endpoint y ruta corregidos
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Shape": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Name": "string",
    "MsoDrawingType": "string",
    "AutoShapeType": "string",
    "Placement": "string",
    "UpperLeftRow": 0,
    "Top": 0,
    "UpperLeftColumn": 0,
    "Left": 0,
    "LowerRightRow": 0,
    "Bottom": 0,
    "LowerRightColumn": 0,
    "Right": 0,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "RotationAngle": 0,
    "HtmlText": "string",
    "Text": "string",
    "AlternativeText": "string",
    "TextHorizontalAlignment": "string",
    "TextHorizontalOverflow": "string",
    "TextOrientationType": "string",
    "TextVerticalAlignment": "string",
    "TextVerticalOverflow": "string",
    "IsGroup": true,
    "IsHidden": true,
    "IsLockAspectRatio": true,
    "IsLocked": true,
    "IsPrintable": true,
    "IsTextWrapped": true,
    "IsWordArt": true,
    "LinkedCell": "string",
    "ZOrderPosition": 0
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Códigos de estado HTTP posibles**

| Código | Descripción |
|--------|-------------|
| **200 OK** | La forma se recuperó correctamente. |
| **400 Bad Request** | La solicitud está mal formada o faltan parámetros obligatorios. |
| **401 Unauthorized** | La autenticación falló o falta/inválida el token. |
| **404 Not Found** | El libro, la hoja o el índice de forma especificados no existen. |
| **500 Internal Server Error** | Ocurrió un error inesperado en el servidor. |

**Errores comunes:** Utilizar un dominio base incorrecto (`api.aspose.com`) o el segmento obsoleto `/autoshapes/` provocará un error 404. Siempre utilice el segmento `/shapes/` con el dominio `api.aspose.cloud`.

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}

Para operaciones relacionadas, consulte la documentación sobre **[Agregar una forma](/es/shapes/add/)** y **[Actualizar una forma](/es/shapes/update/)**.