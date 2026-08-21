---
title: "Exportar hoja de cálculo – Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Hoja de cálculo"
type: docs
url: /export-excel-worksheet-to-different-formats/
aliases: [/export/excel-worksheet-to-different-formats/]
keywords: "Aspose.Cells, exportar hoja de cálculo, API de Excel, PDF, CSV, TIFF, ODS, formatos de imagen"
description: "Aprenda a exportar una hoja de cálculo de Excel a PDF, CSV, TIFF y otros formatos utilizando la API REST de Aspose.Cells Cloud. Incluye un ejemplo con cURL, autenticación requerida, detalles de parámetros y manejo de respuestas."
weight: 20
ArticleTitle: "Exportar hoja de cálculo de Excel a varios formatos – Aspose.Cells Cloud"
---

Puede exportar una hoja de cálculo a los siguientes formatos:

- **XLS** – [Detalles del formato XLS](https://docs.fileformat.com/spreadsheet/xls/)
- **XLSX** – [Detalles del formato XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)
- **XLSB** – [Detalles del formato XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)
- **CSV** – [Detalles del formato CSV](https://docs.fileformat.com/spreadsheet/csv/)
- **TSV** – [Detalles del formato TSV](https://docs.fileformat.com/spreadsheet/tsv/)
- **XLSM** – [Detalles del formato XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)
- **ODS** – [Detalles del formato ODS](https://docs.fileformat.com/spreadsheet/ods/)
- **TXT** – [Detalles del formato TXT](https://docs.fileformat.com/word-processing/txt/)
- **PDF** – [Detalles del formato PDF](https://docs.fileformat.com/pdf/)
- **OTS** – [Detalles del formato OTS](https://docs.fileformat.com/spreadsheet/ots/)
- **XPS** – [Detalles del formato XPS](https://docs.fileformat.com/page-description-language/xps/)
- **DIF** – [Detalles del formato DIF](https://docs.fileformat.com/spreadsheet/dif/)
- **PNG** – [Detalles del formato PNG](https://docs.fileformat.com/Image/png/)
- **JPEG** – [Detalles del formato JPEG](https://docs.fileformat.com/image/jpeg/)
- **BMP** – [Detalles del formato BMP](https://docs.fileformat.com/image/bmp/)
- **SVG** – [Detalles del formato SVG](https://docs.fileformat.com/page-description-language/svg/)
- **TIFF** – [Detalles del formato TIFF](https://docs.fileformat.com/image/tiff/)
- **EMF** – [Detalles del formato EMF](https://docs.fileformat.com/image/emf/)
- **NUMBERS** – [Detalles del formato Numbers](https://docs.fileformat.com/spreadsheet/numbers/)
- **FODS** – [Detalles del formato FODS](https://docs.fileformat.com/spreadsheet/fods/)

[Explore operaciones de exportación relacionadas, como la exportación de un libro completo o de un gráfico.](https://docs.aspose.cloud/cells/export-excel-workbook-to-different-formats/)

## API PostExport

```http
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ruta / Cadena de consulta / Cuerpo HTTP | Obligatorio | Descripción                                                                 |
|----------------------|---------|-----------------------------------------|-------------|-----------------------------------------------------------------------------|
| file                 | archivo | formData                                | Sí          | Archivo a cargar                                                            |
| objectType           | string  | query                                   | Sí          | Tipo de objeto a exportar. Para la exportación de gráficos use `chart`. Otros valores posibles son `worksheet`, `picture`, etc. |
| format               | string  | query                                   | Sí          | Formato de salida deseado. Valores admitidos: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### Respuesta

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet3.tif",
      "FileSize": 2824,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4.tif",
      "FileSize": 1350,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet5.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet7.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet4.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

### **Manejo de errores**

Si la solicitud falla, la API devuelve un objeto JSON de error que contiene campos como `Code` y `Message`. Los códigos de estado HTTP típicos incluyen **401 Unauthorized** (token ausente o no válido) y **400 Bad Request** (parámetros no válidos).

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                    |
|--------|-----------------------------|----------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Bad Request                 | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | Unauthorized                | Token JWT no válido o ausente.                                |
| 413    | Payload Too Large           | El archivo cargado excede el límite de tamaño.                |
| 500    | Internal Server Error       | Error inesperado del servidor.                                |

**Notas**

- El tamaño máximo de archivo para carga es de 50 MB.  
- La API permite exportar varias hojas de cálculo en una única solicitud; cada hoja se devuelve como un archivo independiente dentro del array `Files`.  
- El procesamiento asíncrono está disponible para libros grandes; utilice la respuesta `202 Accepted` para sondear el estado de la operación.

## Cómo usar la API PostExport con SDKs

### Requisitos previos

Antes de llamar a la API, obtenga un token de acceso JWT válido mediante el flujo de autenticación de Aspose.Cells Cloud. Asegúrese de que el token esté incluido en la cabecera `Authorization` de cada solicitud. Los SDK gestionan automáticamente la adquisición del token cuando se configuran con sus credenciales de cliente.

### Especificación de la API PostExport

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo invocar la API en la nube con cURL.

```bash
# Exportar una hoja de cálculo al formato TIFF
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=worksheet&format=tiff" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "File=@MyWorkbook.xlsx"
```

### Uso de los SDKs de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar con Aspose.Cells Cloud. Un SDK abstracte los detalles de bajo nivel, lo que le permite centrarse en su lógica de negocio. Para obtener la lista completa de SDKs compatibles, visite el [repositorio de GitHub](https://github.com/aspose-cells-cloud).

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells utilizando diversos SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}
---