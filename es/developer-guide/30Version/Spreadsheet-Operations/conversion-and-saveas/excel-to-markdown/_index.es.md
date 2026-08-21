---
title: "Convertir Excel a Markdown"
second_title: "Documento"
linktitle: "Excel a Markdown"
type: docs
url: /es/convert-excel-file-to-markdown-file/
keywords: "Excel, Markdown, conversión, Aspose.Cells Cloud, API REST, conversión de Excel a Markdown, API de Markdown de Aspose Cells, exportación de Excel a Markdown"
description: "Convierta hojas de cálculo de Excel a Markdown mediante la API REST de Aspose.Cells Cloud – incluye ejemplo de cURL, fragmentos de SDK, parámetros requeridos y detalles de autenticación."
weight: 100
ArticleTitle: "Convertir Excel a Markdown – Documentación de la API de Aspose.Cells Cloud"
---

Esta API REST convierte un archivo de hoja de cálculo en un archivo en formato Markdown.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```http
POST https://api.aspose.cloud/v3.0/cells/convert/markdown
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parámetros de consulta


| Nombre del parámetro    | Tipo   | Ubicación | Descripción                                                                                                   |
| ----------------------- | ------ | --------- | ------------------------------------------------------------------------------------------------------------- |
| password                | string | query     | Contraseña necesaria para abrir el archivo de Excel.                                                          |
| storageName             | string | query     | Nombre del almacenamiento donde se encuentra el archivo.                                                      |
| checkExcelRestriction   | bool   | query     | Indica si se deben aplicar restricciones específicas de Excel al modificar celdas u objetos relacionados.    |
| datafile                | file   | body      | El archivo de Excel que se cargará como la primera parte del contenido multipart.                            |

### Respuesta

La API devuelve un objeto JSON de tipo **FileInfo**:

- **FileInfo** – objeto que contiene el nombre, tamaño y contenido codificado en base64 del archivo Markdown generado.

```json
{
  "Filename": "ejemplo.md",
  "FileSize": 12345,
  "FileContent": "cadena_en_base64"
}
```

### Respuestas de error

| Código HTTP | Descripción                                                     | Cuerpo JSON de ejemplo                          |
| ----------- | --------------------------------------------------------------- | ----------------------------------------------- |
| 401         | No autorizado – token ausente o inválido.                       | `{"error":"Token de acceso inválido."}`         |
| 400         | Solicitud incorrecta – parámetros obligatorios ausentes o formato de archivo inválido. | `{"error":"El campo 'datafile' es obligatorio."}` |
| 500         | Error interno del servidor – problema inesperado en el servidor. | `{"error":"Ocurrió un error inesperado."}`      |



## Cómo utilizar la API PostConvertWorkbookToMarkdown con SDK

### Especificación de la API PostConvertWorkbookToMarkdown

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToMarkdown) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo invocar la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```shell
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/markdown" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "File=@su_archivo_excel.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "ejemplo.md",
  "FileSize": 12345,
  "FileContent": "cadena_en_base64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK maneja los detalles de bajo nivel, lo que le permite centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToMarkdown.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToMarkdown.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToMarkdown.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToMarkdown.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToMarkdown.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToMarkdown.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToMarkdown.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToMarkdown.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Otras API que implementan esta función

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Guarda un archivo de Excel como HTML con configuraciones adicionales y almacena el resultado.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Convierte un archivo de Excel a HTML con opciones adicionales y devuelve el resultado en la respuesta.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Recupera un archivo de Excel y puede convertirlo a HTML con configuraciones opcionales.
---