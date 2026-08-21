---
title: "Excel a PNG"
second_title: "Documentos"
linktitle: "Excel a PNG"
type: docs
url: /esconvert-excel-file-to-png-file/
keywords: "Excel a PNG, Aspose.Cells Cloud, API REST, conversión de hojas de cálculo, formato PNG"
description: "Convierta hojas de cálculo de Excel a imágenes PNG mediante la API REST de Aspose.Cells Cloud. Admite múltiples SDK y proporciona ejemplos detallados para diversos lenguajes de programación."
weight: 90
---

Esta API REST convierte un archivo de hoja de cálculo al formato PNG.

## Especificación de la API REST

```
POST https://api.aspose.cloud/v3.0/cells/convert/png
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en tokens JWT</a>.

### **Parámetro de consulta**

| Nombre del parámetro  | Tipo   | Descripción                                                                                  |
| --------------------- | ------ | -------------------------------------------------------------------------------------------- |
| password              | string | Contraseña necesaria para abrir el archivo de Excel.                                         |
| storageName           | string | Nombre del almacenamiento donde se encuentra el archivo.                                    |
| checkExcelRestriction | bool   | Determina si se deben verificar las restricciones del archivo de Excel al modificar celdas u objetos relacionados. |

### **Parámetro del cuerpo de la solicitud**

| Nombre del parámetro | Tipo      | Descripción                                                               |
| -------------------- | --------- | ------------------------------------------------------------------------- |
| datafile             | data file | Archivo de hoja de cálculo incluido en la primera parte de la solicitud multipart. |

### **Respuesta**

La API devuelve un objeto **FileInfo** que contiene el archivo PNG generado.

| Campo           | Tipo   | Descripción                                   |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | Nombre del archivo PNG (por ejemplo, `ejemplo.png`). |
| **FileSize**    | int    | Tamaño del archivo en bytes.                  |
| **FileContent** | string | Contenido del archivo PNG codificado en Base64. |

[FileInfo](/cells/file-info/)


**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400  | Solicitud incorrecta        | Faltan parámetros o son inválidos (por ejemplo, tipo de archivo no admitido). |
| 401  | No autorizado               | Token JWT inválido o ausente. |
| 413  | Carga útil demasiado grande | El archivo subido excede el límite de tamaño. |
| 500  | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo usar la API PostConvertWorkbookToPNG con SDK

### Especificación de la API PostConvertWorkbookToPNG


La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/png" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.png",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPNG.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPNG.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPNG.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPNG.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPNG.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPNG.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPNG.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPNG.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Otras API que implementan funciones similares

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Guarda un archivo de Excel como CSV (u otros formatos) con ajustes adicionales y almacena el resultado.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Convierte un archivo de Excel a CSV (u otros formatos) con parámetros opcionales y devuelve el resultado en la respuesta.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Recupera un archivo de Excel y puede convertirlo a CSV (u otros formatos) sobre la marcha.

---