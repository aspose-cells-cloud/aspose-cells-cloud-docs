---
title: "Excel a Docx"
second_title: "Documento"
linktitle: "Excel a Docx"
type: docs
url: /es/esconvert-excel-file-to-docx-file/
keywords: "conversión de Excel a Docx, Aspose.Cells Cloud, API REST, conversión de hojas de cálculo, generación de documentos"
description: "Convierta hojas de cálculo de Excel a documentos DOCX mediante la API REST de Aspose.Cells Cloud. Admite múltiples SDK y lenguajes de programación para una integración fluida."
weight: 90
---

Esta API REST convierte un archivo de hoja de cálculo a un archivo en formato DOCX.

## API REST

```http
POST https://api.aspose.cloud/v3.0/cells/convert/docx
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.



**Parámetros de consulta**

| Nombre del parámetro    | Tipo   | Descripción                                                                                           |
| --------------------- | ------ | ----------------------------------------------------------------------------------------------------- |
| password              | string | Contraseña necesaria para abrir el archivo de Excel.                                                 |
| storageName           | string | Nombre del almacenamiento donde se encuentra el archivo.                                             |
| checkExcelRestriction | bool   | Indica si se deben verificar las restricciones del archivo de Excel cuando el usuario modifica objetos relacionados con celdas. |

**Parámetro del cuerpo de la solicitud**

| Nombre del parámetro | Tipo      | Descripción                                                           |
| -------------------- | --------- | --------------------------------------------------------------------- |
| datafile             | data file | Archivo de datos guardado en la primera parte del cuerpo de solicitud multipart. |

**Respuesta**

La API devuelve un objeto **FileInfo** que contiene el archivo de Word generado.

| Campo           | Tipo   | Descripción                                      |
| --------------- | ------ | ------------------------------------------------ |
| **Filename**    | string | Nombre del archivo de Word (por ejemplo, `ejemplo.docx`). |
| **FileSize**    | int    | Tamaño del archivo en bytes.                     |
| **FileContent** | string | Contenido del archivo de Word codificado en Base64. |


[FileInfo](/cells/file-info/)

**Códigos de estado HTTP**

| Código | Significado                | Descripción                                                             |
|--------|----------------------------|-------------------------------------------------------------------------|
| 200    | Correcto                   | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta       | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado              | Token JWT no válido o faltante.                                         |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño.                          |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                        |

## Cómo usar la API PostConvertWorkbookToDocx con SDK

### Especificación de la API PostConvertWorkbookToDocx

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/docx" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "ejemplo.docx",
  "FileSize": 12345,
  "FileContent": "Contenido del archivo: cadena_codificada_en_base64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToDocx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToDocx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToDocx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToDocx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToDocx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToDocx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToDocx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToDocx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Otras API que implementan esta función

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Guarda un archivo de Excel como archivo DOCX con configuraciones adicionales y almacena el resultado en el almacenamiento especificado.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Convierte un archivo de Excel a un archivo DOCX con configuraciones opcionales y devuelve el resultado en la respuesta.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Recupera un libro de Excel y lo convierte a un archivo DOCX con parámetros opcionales.

---