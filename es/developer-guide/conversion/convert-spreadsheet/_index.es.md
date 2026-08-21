---
title: "Aspose.Cells Cloud Web API: Convertir una hoja de cálculo a otro formato - Herramienta gratuita en línea"
second_title: "Documento"
ArticleTitle: "Cómo convertir una hoja de cálculo a otro formato: Guía paso a paso"
linktitle: "Convertir hoja de cálculo"
type: docs
url: /es/convert-spreadsheet/
keywords: "Aspose, Aspose.Cells, conversión de hojas de cálculo, Excel a PDF, API de Excel, conversión de archivos en la nube"
description: "Convierta un archivo de hoja de cálculo a otro formato utilizando la API de Aspose.Cells Cloud."
weight: 100
---

Convierta una hoja de cálculo o archivo de Excel local a otro formato con la API web Aspose.Cells Cloud.

## **API de conversión de hojas de cálculo**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                   |
| :------------------- | :----- | :--------------------------------------- | :-------------------------------------------------------------------------------------------- |
| Spreadsheet          | Archivo | FormData                                 | Cargue el archivo de hoja de cálculo que desea convertir.                                    |
| format               | Cadena | Query                                    | (Obligatorio) El formato de salida deseado (por ejemplo, “XLSX”, “PDF”, “CSV”).             |
| outPath              | Cadena | Query                                    | (Opcional) Ruta de carpeta donde se guardará el libro convertido. El valor predeterminado es null. |
| outStorageName       | Cadena | Query                                    | Especifique el nombre del almacenamiento de archivos de salida.                              |
| fontsLocation        | Cadena | Query                                    | Utilice fuentes personalizadas para la hoja de cálculo.                                      |
| region               | Cadena | Query                                    | Especifique la configuración regional de la hoja de cálculo.                                 |
| password             | Cadena | Query                                    | Contraseña para abrir el archivo de hoja de cálculo si está protegido.                        |

### **Respuesta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Estado de éxito**

- **200 OK** – La conversión se realizó correctamente y el cuerpo de la respuesta contiene el flujo del archivo convertido.
- La cabecera `Content-Type` refleja el tipo MIME del formato de salida solicitado (por ejemplo, `application/pdf` para PDF).

**Códigos de estado HTTP**

| Código | Significado            | Descripción                                                        |
| ------ | ---------------------- | ------------------------------------------------------------------ |
| 200    | OK                     | Filtro aplicado correctamente; la respuesta contiene detalles.    |
| 400    | Solicitud incorrecta   | Faltan parámetros o son inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado          | Token JWT inválido o faltante.                                     |
| 413    | Payload demasiado grande | El archivo cargado supera el límite de tamaño.                   |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                  |

## Formatos

| **Formato de salida**                                                                                         | **Descripción**                                                                                                              |
| :------------------------------------------------------------------------------------------------------------ | :--------------------------------------------------------------------------------------------------------------------------- |
| <a href="https://docs.fileformat.com/spreadsheet/xls/" rel="noopener noreferrer">XLS</a>                      | Libro de Excel 95/5.0 - 2003.                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xlsx/" rel="noopener noreferrer">XLSX</a>                    | Formato de archivo de hoja de cálculo XML de Office Open.                                                                    |
| <a href="https://docs.fileformat.com/spreadsheet/xlsb/" rel="noopener noreferrer">XLSB</a>                    | Libro binario de Excel.                                                                                                      |
| <a href="https://docs.fileformat.com/spreadsheet/xlsm/" rel="noopener noreferrer">XLSM</a>                    | Libro con macro habilitadas de Excel.                                                                                        |
| <a href="https://docs.fileformat.com/spreadsheet/xlt/" rel="noopener noreferrer">XLT</a>                      | Plantilla de Excel 97 - 2003.                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xltx/" rel="noopener noreferrer">XLTX</a>                    | Plantilla de Excel.                                                                                                          |
| <a href="https://docs.fileformat.com/spreadsheet/xltm/" rel="noopener noreferrer">XLTM</a>                    | Plantilla con macro habilitadas de Excel.                                                                                    |
| <a href="https://docs.fileformat.com/spreadsheet/xlam/" rel="noopener noreferrer">XLAM</a>                    | Archivo de complemento con macro habilitadas de Excel, utilizado para añadir nuevas funciones a Excel.                       |
| <a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>                      | Archivo CSV (valores separados por comas).                                                                                   |
| <a href="https://docs.fileformat.com/spreadsheet/tsv/" rel="noopener noreferrer">TSV</a>                      | Archivo TSV (valores separados por tabulaciones).                                                                            |
| <a href="https://docs.fileformat.com/word-processing/txt/" rel="noopener noreferrer">TXT</a>                  | Archivo de texto plano delimitado.                                                                                           |
| <a href="https://docs.fileformat.com/web/html/" rel="noopener noreferrer">HTML</a>                            | Formato HTML.                                                                                                                |
| <a href="https://docs.fileformat.com/web/mhtml/" rel="noopener noreferrer">MHTML</a>                          | Archivo MHTML.                                                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/ods/" rel="noopener noreferrer">ODS</a>                      | ODS (Hoja de cálculo OpenDocument).                                                                                          |
| SpreadsheetML                                                                                                 | Archivo XML de Excel 2003.                                                                                                   |
| <a href="https://docs.fileformat.com/spreadsheet/numbers/" rel="noopener noreferrer">Numbers</a>              | El documento lo crea la aplicación “Numbers” de Apple, parte de la suite iWork para macOS e iOS.                             |
| <a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>                            | Notación de objetos JavaScript.                                                                                              |
| <a href="https://docs.fileformat.com/spreadsheet/dif/" rel="noopener noreferrer">DIF</a>                      | Formato de intercambio de datos.                                                                                             |
| <a href="https://docs.fileformat.com/database/dbf/" rel="noopener noreferrer">DBF</a>                         | Archivo con extensión .dbf, utilizado por el sistema de gestión de bases de datos dBASE.                                    |
| <a href="https://docs.fileformat.com/pdf/" rel="noopener noreferrer">PDF</a>                                  | Formato de documento portátil de Adobe.                                                                                      |
| <a href="https://docs.fileformat.com/page-description-language/xps/" rel="noopener noreferrer">XPS</a>        | Formato XML Paper Specification.                                                                                             |
| <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a>        | Formato de gráficos vectoriales escalables.                                                                                  |
| <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>                          | Formato de archivo de imagen etiquetada.                                                                                     |
| <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>                            | Formato de gráficos de red portátil.                                                                                         |
| <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>                            | Formato de imagen de mapa de bits.                                                                                           |
| <a href="https://docs.fileformat.com/image/emf/" rel="noopener noreferrer">EMF</a>                            | Formato de metaarchivo mejorado.                                                                                             |
| <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>                          | JPEG es un tipo de formato de imagen que se guarda mediante compresión con pérdida.                                          |
| <a href="https://docs.fileformat.com/image/gif/" rel="noopener noreferrer">GIF</a>                            | Formato de intercambio de gráficos.                                                                                          |
| <a href="https://docs.fileformat.com/word-processing/md/" rel="noopener noreferrer">MARKDOWN</a>              | Representa un documento Markdown.                                                                                            |
| <a href="https://docs.fileformat.com/spreadsheet/sxc/" rel="noopener noreferrer">SXC</a>                      | Formato basado en XML utilizado por OpenOffice y StarOffice.                                                                 |
| <a href="https://docs.fileformat.com/spreadsheet/fods/" rel="noopener noreferrer">FODS</a>                    | Este es un formato Open Document almacenado como XML plano.                                                                  |
| <a href="https://docs.fileformat.com/word-processing/docx/" rel="noopener noreferrer">DOCX</a>                | Formato conocido para documentos de Microsoft Word que combina archivos XML y binarios.                                      |
| <a href="https://docs.fileformat.com/presentation/pptx/" rel="noopener noreferrer">PPTX</a>                   | El formato PPTX se basa en el formato de archivo de presentación XML abierto de Microsoft PowerPoint.                       |
| <a href="https://docs.fileformat.com/database/sql/" rel="noopener noreferrer">SqlScript</a>                   | Lenguaje de consulta estructurado.                                                                                           |
| <a href="https://docs.fileformat.com/web/xhtml/" rel="noopener noreferrer">XHtml</a>                          | XHTML es un formato de archivo de texto basado en XML con marcado, utilizando una reexpresión de HTML 4.0.                   |
| <a href="https://docs.fileformat.com/ebook/epub/" rel="noopener noreferrer">Epub</a>                          | Los archivos con extensión .epub son un formato de libro electrónico que proporciona una publicación digital estándar para editores y consumidores. |
| <a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Xml</a>                              | XML significa lenguaje de marcado extensible; es similar a HTML, pero utiliza etiquetas para definir objetos.                |
| <a href="https://docs.fileformat.com/spreadsheet/ots/" rel="noopener noreferrer">Ots</a>                      | Archivo de plantilla de hoja de cálculo Open Document (OTS).                                                                 |
| <a href="https://docs.fileformat.com/ebook/azw3/" rel="noopener noreferrer">AZW3</a>                          | AZW es un formato de archivo de libro electrónico desarrollado por Amazon para dispositivos Kindle. AZW3, también conocido como Kindle Format 8 (KF8). |

## ¿Dónde debería utilizar la API de conversión de hojas de cálculo?

- **Migración de sistemas heredados**: Convertir miles de archivos XLS heredados a XLSX para sistemas modernos.
- **Estandarización de archivos archivados**: Normalizar diversos formatos de hojas de cálculo (XLS, XLSM, ODS, CSV) a un único formato para archivar.
- **Interoperabilidad entre suites ofimáticas**: Convertir archivos de Excel a formatos compatibles con LibreOffice, Google Sheets o Apple Numbers.
- **Normalización de fuentes de datos**: Convertir diversos formatos de hojas de cálculo a CSV o JSON para su inserción en bases de datos.
- **Publicación web**: Convertir modelos financieros a HTML para su visualización en la web.

## ¿Por qué debería utilizar la API de conversión de hojas de cálculo?

- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido, y cuenta con documentación exhaustiva. Comparado con la construcción de soluciones personalizadas de renderizado de gráficos, esto reduce significativamente la carga de desarrollo.
- **Rentable**: Puede convertir datos tabulares sin cargar previamente el libro, lo que ahorra espacio de almacenamiento y reduce costos.
- **Amplia compatibilidad de formatos**: Convierta entre más de 20 formatos de hojas de cálculo.
- **Preserva la fidelidad y el formato de los datos**.

## ¿Cómo utilizar la API de conversión de hojas de cálculo con SDK?

Los siguientes ejemplos de código demuestran cómo utilizar la API de conversión de hojas de cálculo con diversos SDK.

### **Especificación de la API de conversión de hojas de cálculo**

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheet" rel="noopener noreferrer">Especificación de la API de conversión de hojas de cálculo</a> define una interfaz de programación públicamente accesible, lo que le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert?format=pdf \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="file.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### **Utilizar los SDK de Aspose.Cells Cloud**

Utilizar el SDK es la forma más rápida de desarrollar, ya que abstracte los detalles de bajo nivel, permitiéndole convertir un archivo de hoja de cálculo a otro formato con código conciso. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{</tab>}}
{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Convert Spreadsheet",
  "description": "Convierta un archivo de hoja de cálculo a otro formato utilizando Aspose.Cells Cloud.",
  "url": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
  "documentation": "https://docs.aspose.cloud/cells/convert-spreadsheet/",
  "targetPlatform": "Web",
  "authenticationType": "OAuth2",
  "operation": [
    {
      "@type": "HttpOperation",
      "httpMethod": "PUT",
      "urlTemplate": "/cells/convert/spreadsheet",
      "description": "Convierta una hoja de cálculo al formato especificado."
    }
  ]
}
</script>