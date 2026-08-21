---
title: "Convertir un archivo de Excel a otro formato o guardarlo de forma diferente."
second_title: "Document"
linktitle: "Conversión y Guardar como"
type: docs
url: /es/conversion-and-save-as/
aliases: [  /es/convert-excel/ , /es/convert/ ]
keywords: "Aspose.Cells, API de conversión de Excel, convertir Excel a PDF, Excel a CSV, Excel a JSON, conversión en la nube de hojas de cálculo"
description: "Aprenda cómo convertir libros de Excel a PDF, CSV, JSON, HTML y más de 15 formatos más utilizando la API REST de Aspose.Cells Cloud. Incluye detalles de los puntos finales, comandos de ejemplo con cURL y fragmentos de código para SDK en Java, .NET, Python y otros lenguajes."
weight: 30
ArticleTitle: "Convierta archivos de Excel a PDF, CSV, JSON y otros formatos con Aspose.Cells Cloud"
---

Si originalmente creó un archivo de Excel en un formato determinado—como [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), o [CSV](https://docs.fileformat.com/spreadsheet/csv/)—puede resultarle útil convertir el archivo de Excel a otro formato para aprovechar características especiales. Por ejemplo, convertir un archivo de Excel a [PDF](https://docs.fileformat.com/pdf/) protege su contenido contra modificaciones no autorizadas y facilita su lectura y compartición.

**Prerrequisitos**  
Antes de llamar a las API de conversión, obtenga un token de acceso OAuth 2.0 de Aspose Cloud y asegúrese de que el libro esté almacenado en su almacenamiento en la nube de Aspose Cloud (o incluido en el cuerpo de la solicitud para el punto final de conversión PUT).

La conversión de documentos es un proceso complejo. Muchos factores contribuyen a la complejidad del proceso de conversión y deben considerarse durante la transformación. Proporcionar una conversión precisa y de calidad profesional entre formatos de Excel es una característica clave de Aspose.Cells Cloud.

El servicio funciona sin problemas para cualquier conversión de documentos entre formatos. Puede tanto importar como exportar documentos en los siguientes formatos:

**Formatos admitidos**  
- Importación/exportación: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/)
- Sólo exportación: [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/)

### API de conversión

| API                         | Descripción                                                                                     |
| :-------------------------- | :---------------------------------------------------------------------------------------------- |
| `GET /cells/{name}`         | Recupera un libro de Excel del almacenamiento en la nube y lo convierte al formato solicitado. |
| `PUT /cells/convert`        | Convierte un libro de Excel proporcionado en el cuerpo de la solicitud al formato de salida especificado. |
| `POST /cells/{name}/saveAs` | Guarda un libro de Excel existente en otro formato directamente en el almacenamiento en la nube. |

**Detalles de la API**

- **GET /cells/{name}**  
  - **Parámetros de ruta:** `name` – nombre del archivo del libro (obligatorio).  
  - **Parámetros de consulta:** `format` – formato de destino (por ejemplo, pdf, csv, json); `storage` – nombre del almacenamiento en la nube (opcional); `folder` – ruta de la carpeta dentro del almacenamiento (opcional).  
  - **Respuesta:** Flujo de archivo del libro convertido; `Content‑Type` coincide con el formato de destino.  
  - **Códigos de estado:** 200 OK, 400 Solicitud incorrecta, 401 No autorizado, 404 No encontrado, 500 Error interno del servidor.  

- **PUT /cells/convert**  
  - **Cuerpo de la solicitud:** multipart/form‑data que contiene el archivo del libro de origen (`file`) y un campo `format` obligatorio que indica el formato de salida deseado.  
  - **Respuesta:** Flujo binario del archivo convertido.  
  - **Códigos de estado:** 200 OK, 400 Solicitud incorrecta, 401 No autorizado, 500 Error interno del servidor.  

- **POST /cells/{name}/saveAs**  
  - **Parámetros de ruta:** `name` – nombre del libro existente.  
  - **Parámetros de consulta:** `format` – formato de destino; `outPath` – ruta de destino en el almacenamiento en la nube (opcional); `storage` – nombre del almacenamiento (opcional).  
  - **Respuesta:** Objeto JSON con el resultado de la operación y la ruta del archivo guardado. Ejemplo de respuesta:  

    ```json
    {
      "status": "OK",
      "code": 200,
      "message": "File saved successfully.",
      "path": "Converted/MyWorkbook.pdf"
    }
    ```  

  - **Códigos de estado:** 200 OK, 400 Solicitud incorrecta, 401 No autorizado, 404 No encontrado, 500 Error interno del servidor.  

**Ejemplo de cURL para convertir a PDF**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -o MyWorkbook.pdf
```

**Fragmento de código para SDK de Java (GET /cells/{name})**

```java
CellsApi apiInstance = new CellsApi();
String name = "MyWorkbook.xlsx";
String format = "pdf";
File result = apiInstance.cellsGetWorkbook(name, format, null, null);
result.renameTo(new File("MyWorkbook.pdf"));
```

**Fragmento de código para SDK de .NET (PUT /cells/convert)**

```csharp
var api = new CellsApi();
var file = File.ReadAllBytes("MyWorkbook.xlsx");
var format = "pdf";
var result = api.ConvertWorkbook(new MemoryStream(file), format);
File.WriteAllBytes("MyWorkbook.pdf", result);
```

**Fragmento de código para SDK de Python (POST /cells/{name}/saveAs)**

```python
import asposecellscloud
api = asposecellscloud.CellsApi()
api.post_save_as(name="MyWorkbook.xlsx", format="pdf", out_path="Converted/MyWorkbook.pdf")
```

Los siguientes artículos explican cada API con detalle e incluyen ejemplos adicionales con cURL y SDK:

- [Convertir un archivo de Excel a un formato diferente](/cells/convert-an-excel-file-to-different-formats)
- [Guardar un archivo de Excel como un formato diferente](/cells/save-an-excel-file-as-other-formats-files)
- [Convertir un archivo de Excel a un archivo CSV](/cells/convert-excel-file-to-csv-file)
- [Convertir un archivo de Excel a un archivo DOCX](/cells/convert-excel-file-to-docx-file)
- [Convertir un archivo de Excel a un archivo HTML](/cells/convert-excel-file-to-html-file)
- [Convertir un archivo de Excel a un archivo JSON](/cells/convert-excel-file-to-json-file)
- [Convertir un archivo de Excel a un archivo Markdown](/cells/convert-excel-file-to-markdown-file)
- [Convertir un archivo de Excel a un archivo PDF](/cells/convert-excel-file-to-pdf-file)
- [Convertir un archivo de Excel a un archivo PNG](/cells/convert-excel-file-to-png-file)
- [Convertir un archivo de Excel a un archivo PPTX](/cells/convert-excel-file-to-pptx-file)
- [Convertir un archivo de Excel a un archivo SQL](/cells/convert-excel-file-to-sql-file)
- [Convertir un archivo de Excel a un archivo TIFF](/cells/convert-excel-file-to-tiff-file)
---