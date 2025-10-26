---
title: Aspose.Cells Cloud Web API - Convertir una hoja de cálculo a otro formato de archivo
second_title: Documen
ArticleTitle: Convert a Spreadsheet to another format file
linktitle: Convertir hoja de cálculo
type: docs
url: /es/convert-spreadsheet/
keywords: spreadsheet conversion, convert spreadsheet, cloud conversion, REST API, XLSX, PDF, CSV, JSON, Markdown, convert local file
description: Convierte sin esfuerzo una hoja de cálculo de una unidad local a varios formatos específicos utilizando Excel API
weight: 100
kwords: Excel, Office Nube, REST API, Conversión de hojas de cálculo, PDF, CSV, JSON, Markdown, Coincidir con todas las celdas en blanco en una hoja de cálculo Excel
---
Convierta un archivo de hoja de cálculo local/Excel a otro formato de archivo con Aspose.Cells Cloud Web API.

|**Formato de salida**|**Descripción**|
|:- |:- |
|[XLS](https://docs.fileformat.com/spreadsheet/xls/)|Excel 95/5.0 - 2003 Libro de trabajo.|
|[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)|Formato de archivo SpreadsheetML Office Open XML.|
|[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)|Excel Libro de trabajo binario.|
|[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)|Excel Libro de trabajo habilitado para macros.|
|[XLT](https://docs.fileformat.com/spreadsheet/xlt/)|Excel 97 - Excel 2003 Plantilla.|
|[XLTX](https://docs.fileformat.com/spreadsheet/xltx/)|Excel Plantilla.|
|[XLTM](https://docs.fileformat.com/spreadsheet/xltm/)|Excel Plantilla habilitada para macros.|
|[XLAM](https://docs.fileformat.com/spreadsheet/xlam/)|Un archivo de complemento habilitado para macros Excel que se utiliza para agregar nuevas funciones a Excel.|
|[CSV](https://docs.fileformat.com/spreadsheet/csv/)|Archivo CSV (valores separados por comas).|
|[TSV](https://docs.fileformat.com/spreadsheet/tsv/)|Archivo TSV (valores separados por tabulaciones).|
|[TXT](https://docs.fileformat.com/word-processing/txt/)|Archivo de texto plano delimitado.|
|[HTML](https://docs.fileformat.com/web/html/)|Formato HTML.|
|[MHTML](https://docs.fileformat.com/web/mhtml/)|Archivo MHTML.|
|[SAO](https://docs.fileformat.com/spreadsheet/ods/)|ODS (hoja de cálculo OpenDocument).|
|Hoja de cálculo ML|Excel 2003 Archivo XML.|
|[Números](https://docs.fileformat.com/spreadsheet/numbers/)|El documento es creado por la aplicación "Numbers" de Apple, que forma parte de la suite iWork office de Apple, un conjunto de aplicaciones que se ejecutan en los sistemas operativos Mac OS X e iOS.|
|[JSON](https://docs.fileformat.com/web/json/)|Notación de objetos de JavaScript|
|[Diferencia](https://docs.fileformat.com/spreadsheet/dif/)|Formato de intercambio de datos.|
|[DBF](https://docs.fileformat.com/database/dbf/)|El archivo con extensión .dbf es un archivo de base de datos utilizado por una aplicación de sistema de gestión de bases de datos llamada dBASE.|
|[PDF](https://docs.fileformat.com/pdf/)|Formato de documento portátil de Adobe.|
|[XPS](https://docs.fileformat.com/page-description-language/xps/)|Formato de especificación de papel XML.|
|[SVG](https://docs.fileformat.com/page-description-language/svg/)|Formato de gráficos vectoriales escalables.|
|[TIFF](https://docs.fileformat.com/image/tiff/)|Formato de archivo de imagen etiquetada|
|[PNG](https://docs.fileformat.com/image/png/)|Formato de gráficos de red portátil|
|[BMP](https://docs.fileformat.com/image/bmp/)|Formato de imagen de mapa de bits|
|[EMF](https://docs.fileformat.com/image/emf/)|Formato de metarchivo mejorado|
|[JPEG](https://docs.fileformat.com/image/jpeg/)|JPEG es un tipo de formato de imagen que se guarda utilizando el método de compresión con pérdida.|
|[GIF](https://docs.fileformat.com/image/gif/)|Formato de intercambio gráfico|
|[REDUCCIÓN](https://docs.fileformat.com/word-processing/md/)|Representa un documento rebajado.|
|[SXC](https://docs.fileformat.com/spreadsheet/sxc/)|Un formato basado en XML utilizado por OpenOffice y StarOffice|
|[FODS](https://docs.fileformat.com/spreadsheet/fods/)|Este es un formato de documento abierto almacenado como XML plano.|
|[DOCX](https://docs.fileformat.com/word-processing/docx/)|Un formato conocido para documentos de Word Microsoft que es una combinación de archivos XML y binarios.|
|[PPTX](https://docs.fileformat.com/presentation/pptx/)|El formato PPTX se basa en el formato de archivo de presentación XML abierto Microsoft PowerPoint.|
|[SQLScript](https://docs.fileformat.com/database/sql/)|Lenguaje de consulta estructurado.|
|[XHTML](https://docs.fileformat.com/web/xhtml/)|XHTML es un formato de archivo basado en texto con marcado en XML, que utiliza una reformulación de HTML 4.0.|
|[Publicación electrónica](https://docs.fileformat.com/ebook/epub/)|Los archivos con extensión .epub son un formato de archivo de libro electrónico que proporciona un formato de publicación digital estándar para editores y consumidores.|
|[XML](https://docs.fileformat.com/web/xml/)|XML significa lenguaje de marcado extensible, similar a HTML pero diferente en el uso de etiquetas para definir objetos.|
|[Ots](https://docs.fileformat.com/spreadsheet/ots/)|Abrir archivo de hoja de plantilla de documento (OTS).|
|[AZW3](https://docs.fileformat.com/ebook/azw3/)|AZW es un formato de archivo de libro electrónico digital desarrollado por Amazon para sus dispositivos Kindle. AZW3, también conocido como Formato Kindle 8 (KF8).|

## **Convertir hoja de cálculo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|Hoja de cálculo|Archivo|Datos del formulario|Sube el archivo de hoja de cálculo que deseas convertir.|
|formato|Cadena|Consulta|(Obligatorio) El formato de salida deseado (por ejemplo, "Xlsx", "Pdf", "Csv").|
|Ruta de salida|Cadena|Consulta|(Opcional) La ruta de la carpeta donde se almacenará el libro convertido. El valor predeterminado es nulo.|
|nombreAlmacenamientoExterno|Cadena|Consulta|Especifique un nombre de almacenamiento para el archivo de salida.|
|Ubicación de fuentes|Cadena|Consulta|Utilice fuentes personalizadas para la hoja de cálculo.|
|región|Cadena|Consulta|Especifique la configuración de la región de la hoja de cálculo.|
|contraseña|Cadena|Consulta|La contraseña para abrir el archivo de hoja de cálculo si está protegido.|

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

### Códigos de error

- **400 Solicitud incorrecta**: URI de nube Apose.Cells no válido API.
- **401 No autorizado**Token de acceso no válido. O ID de cliente y secreto no válidos.
- **404 No encontrado**:El archivo de hoja de cálculo no es accesible.
- **Error de servidor 500**:La hoja de cálculo ha encontrado una anomalía al obtener los datos de cálculo.

## ¿Por qué debería utilizar la hoja de cálculo Convert API?

- No necesita almacenamiento en la nube, lo que reduce la carga sobre los recursos de la nube.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## ¿Cómo utilizar la hoja de cálculo Convert API con SDK?

### Especificación de la hoja de cálculo Convert API

 El[Especificación de la hoja de cálculo Convert API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertSpreadsheet) define una interfaz de programación de acceso público que le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y le permite convertir un archivo de hoja de cálculo a otro formato de archivo con código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo invocar los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{< /tab >}}
{{< /tabs >}}
