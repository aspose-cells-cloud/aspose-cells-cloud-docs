---
title: Exportar libros de trabajo y objetos internos a tipos de formato
second_title: Aspose.Cells Cloud Documen
linktitle: Exportación
type: docs
url: /es/export/
keywords: Export workbook and internal objects to kinds of format files
description: Aspose.Cells Cloud REST API admite la exportación de archivos Excel y objetos internos a tipos de archivos de formato. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift
weight: 31
---
 Si originalmente creó un archivo Excel en un formato determinado, como[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) , y[CSV](https://docs.fileformat.com/spreadsheet/csv/) , a veces puede resultarle útil convertir el archivo de Excel a otro formato para poder aprovechar las funciones especiales que ofrece. Por ejemplo, es posible que desee exportar un archivo de Excel a[PDF](https://docs.fileformat.com/pdf/) para proteger su contenido de modificaciones no autorizadas y facilitar su lectura y uso simultáneo.

 La exportación de objetos Excel es un proceso complejo. Muchos factores contribuyen a la complejidad y, por lo tanto, deben tenerse en cuenta durante el proceso de exportación. La capacidad de exportar el objeto Excel a un archivo de formato con una calidad profesional precisa es una característica principal de Aspose.Cells Cloud.

 Funciona perfectamente para libros de trabajo, gráficos, formas e imágenes exportados desde un archivo de Excel. Puede exportar formatos:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [SAO](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/) . Los formatos de solo exportación:[PDF](https://docs.fileformat.com/pdf/), [OET](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NÚMEROS](https://docs.fileformat.com/spreadsheet/numbers/), [ALIMENTOS](https://docs.fileformat.com/spreadsheet/fods/).

La solicitud es una solicitud HTTP con contenido de varias partes (ver[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)o[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del contenido multiparte contiene el archivo de datos y la segunda contiene opciones para guardar.

El libro de trabajo REST API `export` y los objetos internos en un archivo de formato diferente.

## RESET API

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| archivo| archivo| formularioDatos| Subir Archivo|
| tipo de objeto| cadena| consulta|tipo de objeto (libro de trabajo/hoja de trabajo/gráfico/forma/imagen/objeto de lista/objeto ole)|
| formato| cadena| consulta|[Formato de archivo](/cells/es/supported-file-formats/)  |
 
 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/export" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Familia SDK de la nube


 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se ocupa de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor, echa un vistazo a la[repositorio GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de Cloud.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:


{{< tabs tabTotal="9" tabID="3" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" tabName10="C#" tabName11="Java" >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export.cs" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Export.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Export.php" >}}


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

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsExport.py" >}}
{{< /tab >}}

{{< /tabs >}}


Los siguientes artículos explican cada API en detalle y contienen cURL y SDK Ejemplos de cada API:


1. [Exporte el gráfico Excel a un formato de archivo diferente](/cells/es/export/excel-chart-to-different-formats/)
2. [Exportar Excel objeto de lista a un formato de archivo diferente](/cells/es/export/excel-listobject-to-different-formats/)
3. [Exportar Excel ole-objeto a un formato de archivo diferente](/cells/es/export/excel-ole-object/)
4. [Exportar imagen Excel a otro formato de archivo](/cells/es/export/excel-picture-to-different-formats/)
5. [Exporte la forma Excel a un formato de archivo diferente](/cells/es/export/excel-shape-to-different-formats/)
6. [Exportar el libro de trabajo Excel a un formato de archivo diferente](/cells/es/export/excel-to-different-formats/)
7. [Exportar la hoja de trabajo Excel a un formato de archivo diferente](/cells/es/export/excel-worksheet-to-different-formats//)
