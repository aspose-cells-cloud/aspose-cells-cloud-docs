---
title: Importar datos a archivos Excel y exportar datos de archivos Excel
second_title: Documen
linktitle: Datos de importación y exportación
type: docs
url: /es/data-import-and-export/
keywords: Excel data import vs. Direct database access; Batch data import vs. Row-by-row data writing; Automated data export vs. Manual data extraction
description: Generar nuevos documentos o informes que puedan incluir gráficos, tablas y otros elementos de visualización de datos
weight: 25
kwords: Excel Importación de datos vs. Acceso directo a la base de datos; Importación de datos por lotes vs. Escritura de datos fila por fila; Exportación de datos automatizada vs. Extracción manual de datos.
---
Aspose.Cells Cloud API admite la importación de datos de una variedad de fuentes de datos y puede exportar datos de Excel, gráficos y tablas a diferentes formatos, incluidos Excel, CSV, PDF, HTML, PNG, etc. Esto hace que la gestión y el uso compartido de datos sean simples y eficientes.

## Cómo importar datos de varias fuentes de datos

Importar datos a un archivo Excel es un proceso complejo. Muchos factores contribuyen a la complejidad y, por lo tanto, deben tenerse en cuenta durante el proceso de exportación. La capacidad de importar diversos formatos y tipos de datos al archivo con una calidad profesional es una característica destacada de Aspose.Cells Cloud.

### Información de las API de importación de datos

Se proporcionan las siguientes API para importar datos a un archivo Excel o a varios archivos Excel:

|API|Descripción|
|:- |:- |
|[POST /celdas/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Importe datos a archivos Excel sin utilizar almacenamiento.|
|[POST /cells/{nombre}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Importe datos al archivo Excel utilizando almacenamiento.|

### Parámetros de la solicitud

#### Sin utilizar almacenamiento

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| archivo| archivo| datos del formulario| Archivo para cargar|
| Opción de importación| Opciones de importación| Cuerpo HTTP| MatrizInt/MatrizDoble/MatrizDeCadenas/DosDimensionesMatrizInt/DosDimensionesMatrizDoble/DosDimensionesMatrizDeCadenas/DatosPorLote/DatosCSV/Imagen|

#### Con el uso del almacenamiento

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino||
| carpeta| cadena| consulta||
| nombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|
| importar datos|| cuerpo||

#### Parámetro de opción de importación de datos

**Los parámetros importantes se describen en la siguiente tabla.**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Datos por lotes</td><td>Lista<CellValue></td> <td>datos del lote</td> </tr>
    <tr> <td>Hoja de trabajo de destino</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero/falso.</td></tr>
    <tr><td>Importar tipo de datos</td><td> Cadena</td><td>Matriz de datos por lotes de cadenas de dos dimensiones</td></tr>
    <tr> <td>Fuente</td><td> Fuente del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Convertir datos numéricos</td><td>Cadena</td> <td>verdadero/falso.</td> </tr>
    <tr> <td>Primera fila</td><td>entero</td> <td></td> </tr>
    <tr> <td>Primera columna</td><td>entero</td><td></td></tr>
    <tr><td>Cadena separadora</td><td> Cadena</td> <td></td></tr>
    <tr> <td>Hoja de trabajo de destino</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>Analizadores personalizados</td><td>Lista<CustomParserConfig></td><td></td></tr>
    <tr><td>Importar tipo de datos</td><td> Cadena</td><td>Datos CSV</td></tr>
    <tr> <td>Fuente</td><td> Fuente del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="3" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Primera fila</td><td>entero</td> <td></td> </tr>
    <tr> <td>Primera columna</td><td>entero</td><td></td></tr>
    <tr><td>Es vertical</td><td>Cadena</td><td>verdadero/falso.</td></tr>
    <tr><td>Datos</td><td> Cadena[]</td> <td></td></tr>
    <tr> <td>Hoja de trabajo de destino</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero/falso.</td></tr>
    <tr><td>Importar tipo de datos</td><td> Cadena</td><td>Imagen</td></tr>
    <tr> <td>Fuente</td><td> Fuente del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="4" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Primera fila</td><td>entero</td> <td></td> </tr>
    <tr> <td>Primera columna</td><td>entero</td><td></td></tr>
    <tr><td>Datos</td><td> Entero[,]</td> <td></td></tr>
    <tr> <td>Hoja de trabajo de destino</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero/falso.</td></tr>
    <tr><td>Importar tipo de datos</td><td> Cadena</td><td>Matriz de dos dimensiones</td></tr>
    <tr> <td>Fuente</td><td> Fuente del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Primera fila</td><td>entero</td> <td></td> </tr>
    <tr> <td>Primera columna</td><td>entero</td><td></td></tr>
    <tr><td>Datos</td><td> Doble[,]</td> <td></td></tr>
    <tr> <td>Hoja de trabajo de destino</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero/falso.</td></tr>
    <tr><td>Importar tipo de datos</td><td> Cadena</td><td>Matriz doble de dos dimensiones</td></tr>
    <tr> <td>Fuente</td><td> Fuente del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Primera fila</td><td>entero</td> <td></td> </tr>
    <tr> <td>Primera columna</td><td>entero</td><td></td></tr>
    <tr><td>Datos</td><td> Cadena[,]</td> <td></td></tr>
    <tr> <td>Hoja de trabajo de destino</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero/falso.</td></tr>
    <tr><td>Importar tipo de datos</td><td> Cadena</td><td>Matriz de cadenas de dos dimensiones</td></tr>
    <tr> <td>Fuente</td><td> Fuente del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Primera fila</td><td>entero</td> <td></td> </tr>
    <tr> <td>Primera columna</td><td>entero</td><td></td></tr>
    <tr><td>Es vertical</td><td>Cadena</td><td>verdadero/falso.</td></tr>
    <tr><td>Datos</td><td> Entero[]</td> <td></td></tr>
    <tr> <td>Hoja de trabajo de destino</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero/falso.</td></tr>
    <tr><td>Importar tipo de datos</td><td> Cadena</td><td>Matriz de enteros</td></tr>
    <tr> <td>Fuente</td><td> Fuente del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Primera fila</td><td>entero</td> <td></td> </tr>
    <tr> <td>Primera columna</td><td>entero</td><td></td></tr>
    <tr><td>Es vertical</td><td>Cadena</td><td>verdadero/falso.</td></tr>
    <tr><td>Datos</td><td> Doble[]</td> <td></td></tr>
    <tr> <td>Hoja de trabajo de destino</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero/falso.</td></tr>
    <tr><td>Importar tipo de datos</td><td> Cadena</td><td>Matriz doble</td></tr>
    <tr> <td>Fuente</td><td> Fuente del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Fila superior izquierda</td><td>entero</td> <td></td> </tr>
    <tr> <td>Columna superior izquierda</td><td>entero</td><td></td></tr>
    <tr> <td>Fila inferior derecha</td><td>entero</td> <td></td> </tr>
    <tr> <td>Columna inferior derecha</td><td>entero</td><td></td></tr>
    <tr><td>Nombre del archivo</td><td>Cadena</td><td></td></tr>
    <tr><td>Datos</td><td> Cadena</td> <td></td></tr>
    <tr> <td>Hoja de trabajo de destino</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero/falso.</td></tr>
    <tr><td>Importar tipo de datos</td><td> Cadena</td><td>Matriz de cadenas</td></tr>
    <tr> <td>Fuente</td><td> Fuente del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>índice de fila</td><td>entero</td> <td></td> </tr>
    <tr><td>índice de columna</td><td>entero</td><td></td></tr>
    <tr><td>tipo</td><td>Cadena</td><td>tipo de datos</td></tr>
    <tr><td>valor</td><td> Cadena</td> <td></td></tr>
    <tr><td>estilo</td><td> Estilo(objeto)</td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>Tipo de origen del archivo</td><td>Cadena</td> <td>Archivos en memoria/Sistema de archivos en la nube/Archivos de solicitud</td> </tr>
    <tr><td>Ruta de archivo</td><td>Cadena</td><td> posición del archivo</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## Cómo exportar objetos Excel a varios formatos de archivo

Si originalmente ha creado un archivo Excel en un formato determinado, como[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) , y[CSV](https://docs.fileformat.com/spreadsheet/csv/) veces puede resultar útil convertir el archivo de Excel a otro formato para aprovechar sus funciones especiales. Por ejemplo, puede que desee exportar un archivo de Excel a...[PDF](https://docs.fileformat.com/pdf/) para proteger sus contenidos de cualquier modificación no autorizada y facilitar su lectura y compartición simultánea.

Exportar el objeto Excel es un proceso complejo. Muchos factores contribuyen a la complejidad y, por lo tanto, deben tenerse en cuenta durante el proceso. La capacidad de exportar el objeto Excel a un solo formato con una calidad profesional es una característica destacada de Aspose.Cells Cloud.

 Funciona perfectamente con libros, gráficos, formas e imágenes exportados desde un archivo de Excel. Puede exportar en los siguientes formatos:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [SAO](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/) Los formatos de solo exportación:[PDF](https://docs.fileformat.com/pdf/), [OET](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [Diferencia](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NÚMEROS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

La solicitud es una solicitud HTTP con contenido de varias partes (ver[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)o[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del contenido multiparte contiene el archivo de datos y la segunda contiene opciones de guardado.

El libro de trabajo REST API `export` y los objetos internos en archivos de formato diferente.

### Exportación API Información

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| archivo| archivo| datos del formulario| Archivo para cargar|
| tipo de objeto| cadena| consulta| tipo de objeto (libro de trabajo/hoja de trabajo/gráfico/forma/imagen/objeto de lista/objeto de ole)|
| formato| cadena| consulta|[Formato de archivo](/cells/es/supported-file-formats/)  |

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

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

## Cómo llamar a las API de importación y exportación

Los siguientes artículos explican en detalle cómo llamar a cada API y contienen ejemplos de SDK y cURL de cada API:

- [Cómo importar datos a archivos Excel sin usar almacenamiento.](/cells/es/import/without-using-storage)
- [Cómo importar datos a archivos Excel utilizando almacenamiento.](/cells/es/import/with-using-storage)
- [Cómo importar datos por lotes a la hoja de trabajo Excel](/cells/es/import-batch-data-into-excel-worksheet/)
- [Cómo importar datos CSV a la hoja de cálculo Excel](/cells/es/import-csv-data-into-excel-worksheet/)
- [Cómo importar imágenes a la hoja de trabajo Excel](/cells/es/import-picture-into-excel-worksheet/)
- [Cómo importar una matriz de enteros a la hoja de trabajo Excel](/cells/es/import-integer-array-into-excel-worksheet/)
- [Cómo importar una matriz doble a la hoja de trabajo Excel](/cells/es/import-double-array-into-excel-worksheet/)
- [Cómo importar una matriz de cadenas a la hoja de trabajo Excel](/cells/es/import-string-array-into-excel-worksheet/)
- [Cómo importar una matriz de enteros de dos dimensiones a la hoja de trabajo Excel](/cells/es/import-a-2D-integer-array-into-excel-worksheet/)
- [Cómo importar una matriz doble de dos dimensiones a la hoja de trabajo Excel](/cells/es/import-a-2D-double-array-into-excel-worksheet/)
- [Cómo importar una matriz de cadenas de dos dimensiones a la hoja de trabajo Excel](/cells/es/import-a-2D-string-array-into-excel-worksheet/)
- [Exportar el gráfico Excel a un formato de archivo diferente](/cells/es/export-excel-chart-to-different-formats/)
- [Exportar el objeto de lista Excel a un formato de archivo diferente](/cells/es/export-excel-listobject-to-different-formats/)
- [Exportar el objeto ole Excel a un formato de archivo diferente](/cells/es/export-excel-ole-object/)
- [Exportar la imagen Excel a un formato de archivo diferente](/cells/es/export-excel-picture-to-different-formats/)
- [Exportar la forma Excel a un formato de archivo diferente](/cells/es/export-excel-shape-to-different-formats/)
- [Exportar el libro de trabajo Excel a un formato de archivo diferente](/cells/es/export-excel-to-different-formats/)
- [Exportar la hoja de cálculo Excel a un formato de archivo diferente](/cells/es/export-excel-worksheet-to-different-formats//)
