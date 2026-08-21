---
title: "Importar imagen en hoja de cálculo de Excel"
ArticleTitle: "Importar imagen en hoja de cálculo de Excel – Guía de la API de Aspose.Cells Cloud"
second_title: "Documentos"
linktitle: "Importar imagen"
type: docs
url: /es/import-picture-into-excel-worksheet/
aliases:
  - /import-picture-into-worksheet/
  - /import-data/picture/
  - /import/picture/
keywords: "importar imagen, Excel, Aspose.Cells Cloud, API REST, v3.0"
description: "Aprenda a importar imágenes en hojas de cálculo de Excel mediante la API REST de Aspose.Cells Cloud v3.0. Incluye ejemplos de solicitudes multipart, códigos de ejemplo para SDK y orientación sobre el manejo de errores. Comience rápidamente con pasos claros y detallados."
weight: 19
---

Importar una imagen en una hoja de cálculo de Excel permite enriquecer las hojas de cálculo con contenido visual, como logotipos, gráficos o diagramas. Esta guía muestra cómo utilizar la operación **ImportPicture** de Aspose.Cells Cloud, el formato necesario para la solicitud y cómo manejar las respuestas.

**Requisitos previos:** Debe tener un token de autenticación JWT válido y un libro existente almacenado en Aspose Cloud Storage antes de invocar la operación de importación.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de la solicitud**

La solicitud es una HTTP **POST** con contenido **multipart/related** (consulte [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

- La **primera parte** contiene un objeto JSON denominado **ImportPictureOption** que describe dónde y cómo se debe colocar la imagen.
- La **segunda parte** transporta el archivo de imagen (o sus datos codificados en Base64).

### ImportPictureOption – definición

```json
{
  "UpperLeftRow": 0,
  "UpperLeftColumn": 0,
  "LowerRightRow": 10,
  "LowerRightColumn": 5,
  "Filename": "logo.png",
  "Data": "iVBORw0KGgoAAAANSUhEUgAA...",
  "DestinationWorksheet": "Hoja1",
  "IsInsert": true,
  "ImportDataType": "Picture",
  "Source": { "FileSource": "Storage" }
}
```

_`IsInsert` es un valor **booleano**: `true` inserta una nueva imagen, `false` reemplaza una existente._

### Parámetros importantes

**ImportPictureOption**

| Nombre del parámetro | Tipo        | Descripción                                                                                                                                                                         |
|----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UpperLeftRow         | int         | Índice de fila de la esquina superior izquierda donde se colocará la imagen.                                                                                                       |
| UpperLeftColumn      | int         | Índice de columna de la esquina superior izquierda donde se colocará la imagen.                                                                                                    |
| LowerRightRow        | int         | Índice de fila de la esquina inferior derecha que define los límites de la imagen.                                                                                                 |
| LowerRightColumn     | int         | Índice de columna de la esquina inferior derecha que define los límites de la imagen.                                                                                              |
| Filename             | string      | Nombre del archivo de imagen.                                                                                                                                                      |
| Data                 | string      | Datos binarios de la imagen codificados en Base64 (opcional si el archivo se envía como la segunda parte).                                                                        |
| DestinationWorksheet | string      | Nombre de la hoja de cálculo donde se insertará la imagen.                                                                                                                         |
| **IsInsert**         | **boolean** | `true` para insertar una nueva imagen; `false` para reemplazar una existente.                                                                                                      |
| ImportDataType       | string      | Tipo de datos que se va a importar (por ejemplo, `Picture`, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source               | FileSource  | Indica la ubicación del archivo de datos cuando el parámetro `BatchData` es null.                                                                                                 |

### Respuesta

Una solicitud correcta devuelve **HTTP 200** con una carga útil JSON similar a:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Códigos de estado posibles:

| Código | Significado                                         |
|--------|-----------------------------------------------------|
| 200    | Importación realizada con éxito                    |
| 400    | Solicitud incorrecta: datos faltantes o inválidos |
| 401    | No autorizado: token inválido o ausente            |
| 500    | Error interno del servidor                         |


## Cómo usar la API PostImportData con SDK

### Especificación de la API PostImportData

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
---