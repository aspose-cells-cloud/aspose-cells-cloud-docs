---
title: "Convertir Excel a PDF – Aspose.Cells Cloud API"
ArticleTitle: "Convertir Excel a PDF – Aspose.Cells Cloud API"
second_title: "Documento"
linktype: "Convertir Excel a PDF"
type: docs
url: /convert-excel-file-to-pdf-file/
aliases: [/convert-excel-file-to-pdf-in-cloud/, /convert/excel-to-pdf/]
keywords: "Aspose, Cells, Excel, PDF, conversión, API en la nube"
description: "Aprenda cómo convertir libros de Excel a PDF mediante la API REST de Aspose.Cells Cloud. Incluye ejemplos con cURL, SDK (C#, Java, Python) y una guía de autenticación."
weight: 80
---

Esta API REST convierte un archivo de hoja de cálculo en un archivo en formato PDF. **Requisitos previos:** Obtenga un token de acceso JWT válido, asegúrese de que el archivo Excel de origen esté almacenado en un almacenamiento compatible y tenga los permisos adecuados para invocar el punto de conexión de conversión.

## API PostConvertWorkbookToPDF

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pdf
```

### **Seguridad y autenticación**

Las APIs de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetro de consulta**

| Nombre del parámetro  | Tipo   | Descripción                                                                 |
| :-------------------- | :----- | :-------------------------------------------------------------------------- |
| password              | string | Contraseña para abrir el archivo Excel.                                     |
| storageName           | string | Nombre del almacenamiento donde se encuentra el archivo.                   |
| checkExcelRestriction | bool   | Indica si se deben aplicar restricciones del archivo Excel al modificar objetos relacionados con celdas. |

`checkExcelRestriction` tiene como valor predeterminado `false` si se omite.

### **Parámetro del cuerpo de solicitud**

| Nombre del parámetro | Tipo | Descripción                                                      |
| :------------------- | :--- | :--------------------------------------------------------------- |
| datafile             | file | Archivo de datos guardado como la primera parte del contenido multipart. |

### **Respuesta**

[FileInfo](/cells/file-info/)

La respuesta devuelve un objeto JSON con metadatos del archivo. El archivo PDF en sí se puede descargar usando el `FileContent` proporcionado (codificado en base64) o mediante el enlace `FileInfo`. La API devuelve un objeto JSON de tipo **FileInfo**:

- **FileInfo** – objeto que contiene el nombre, tamaño y contenido codificado en base64 del archivo **PDF** generado.

```json
{
  "Filename": "ejemplo.pdf",
  "FileSize": 12345,
  "FileContent": "cadena_codificada_en_base64"
}
```

**Códigos de estado HTTP**

| Código | Significado              | Descripción                                                   |
|--------|--------------------------|---------------------------------------------------------------|
| 200    | OK                       | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta     | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado            | Token JWT no válido o faltante.                               |
| 413    | Carga demasiado grande    | El archivo subido excede el límite de tamaño.                 |
| 500    | Error interno del servidor | Error inesperado en el servidor.                             |

## Cómo usar la API PostConvertWorkbookToPDF con SDKs

### Especificación de la API PostConvertWorkbookToPDF

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

**Encabezados de solicitud**

| Encabezado      | Tipo   | Descripción                                              |
| :-------------- | :----- | :------------------------------------------------------- |
| Authorization   | string | Token portador obtenido mediante autenticación JWT.     |
| Content-Type    | string | Debe ser `multipart/form-data` para subir archivos.    |
| Accept          | string | `application/json` para recibir metadatos de respuesta. |

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. Incluya un token de acceso en el encabezado `Authorization` y luego ejecute la siguiente solicitud.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "datafile=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "Contenido del archivo: cadena_codificada_en_base64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDKs de Aspose.Cells Cloud

El uso de un SDK puede simplificar el desarrollo al manejar detalles de bajo nivel. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante varios SDKs:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Otras APIs que implementan esta función

| **API**                 | **Tipo** | **Descripción**                                                                 | **Enlace Swagger**                                                                          |
| :---------------------- | :------- | :------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------ |
| /cells/convert          | PUT      | Convierte un libro de trabajo desde el contenido de la solicitud a un formato especificado. | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

La API [POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) le permite guardar un archivo de MS Excel como PDF con configuraciones adicionales y almacenar el resultado en el almacenamiento.

Esta API REST convierte un archivo Excel a PDF.

La API [PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) le permite convertir un archivo de MS Excel a PDF con configuraciones adicionales y devolver el resultado en la respuesta.

La API [GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) le permite convertir un archivo de MS Excel a PDF con configuraciones adicionales y devolver el resultado en la respuesta.

Estas APIs [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) y [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) definen una interfaz de programación accesible públicamente y permiten realizar interacciones REST directamente desde un navegador web.

Para opciones adicionales de conversión, consulte la página [Opciones de guardado](/cells/save-options/).