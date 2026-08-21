---
title: "Excel a CSV"
second_title: "Documento"
linktitle: "Excel a CSV"
type: docs
url: /esconvert-excel-file-to-CSV-file/
aliases:
  - /convert-excel-file-to-CSV-in-cloud/
  - /convert/excel-to-csv/
  - /convert-excel-file-to-CSV-file/
keywords: "Excel a CSV, Aspose.Cells Cloud, REST API, conversión de hojas de cálculo, archivo CSV, conversión de archivos"
description: "Convierta hojas de cálculo de Excel a CSV utilizando la API REST de Aspose.Cells Cloud. Admite múltiples SDK y lenguajes de programación para una integración sencilla."
weight: 90
---

Esta API REST convierte un archivo de hoja de cálculo a un archivo en formato CSV.

## API REST

```http
POST https://api.aspose.cloud/v3.0/cells/convert/csv
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.


### Parámetros de consulta

| Nombre del parámetro      | Tipo   | Descripción                                                                                      |
| ------------------------- | ------ | ------------------------------------------------------------------------------------------------ |
| `password`                | string | Contraseña necesaria para abrir el archivo de Excel.                                             |
| `storageName`             | string | Nombre del almacenamiento donde se encuentra el archivo.                                         |
| `checkExcelRestriction`   | bool   | Indica si se deben verificar las restricciones del archivo de Excel cuando el usuario modifica objetos relacionados con celdas. |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo      | Descripción                                                          |
| -------------------- | --------- | -------------------------------------------------------------------- |
| `datafile`           | data file | Archivo de datos incluido en la primera parte del cuerpo de la solicitud multipart. |

### Respuesta

La API devuelve un objeto **FileInfo** que contiene el archivo CSV generado.

| Campo           | Tipo   | Descripción                                    |
| --------------- | ------ | ---------------------------------------------- |
| **Filename**    | string | Nombre del archivo CSV (por ejemplo, `ejemplo.csv`). |
| **FileSize**    | int    | Tamaño del archivo en bytes.                   |
| **FileContent** | string | Contenido del archivo CSV codificado en Base64. |

[FileInfo](/cells/file-info/)


**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                    |
|--------|-----------------------------|----------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante. |
| 413    | Payload demasiado grande     | El archivo cargado excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo utilizar la API PostConvertWorkbookToCSV con SDK

### Especificación de la API PostConvertWorkbookToCSV

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo llamar a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/csv" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.CSV",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK gestiona los detalles de bajo nivel, lo que le permite centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

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