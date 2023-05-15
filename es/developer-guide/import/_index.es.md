---
title: Importar
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: Import data into Excel files
description: Aspose.Cells Cloud REST API admite la importación de datos en archivos Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift
weight: 31
---
Importar datos a un archivo Excel es un proceso complejo. Muchos factores contribuyen a la complejidad y, por lo tanto, deben tenerse en cuenta durante el proceso de exportación. La capacidad de importar tipos de formatos y tipos de datos en el archivo con una calidad profesional precisa es una característica principal de Aspose.Cells Cloud.

## API de RSET

Se proporcionan las siguientes API para importar datos en un archivo Excel o varios archivos Excel:

|API|Descripción|
|:- |:- |
|[POST /celdas/importar](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Importe datos en archivos Excel sin usar almacenamiento.|
|[POST /celdas/{nombre}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Importe datos en el archivo Excel con el uso de almacenamiento.|

## Parámetros de solicitud
 
### Sin usar almacenamiento

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| archivo| archivo| formularioDatos| Subir Archivo|
| ImportOption| Opciones de importación| Cuerpo HTTP| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture|

### Con el uso de almacenamiento

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino||
| carpeta| cadena| consulta||
| NombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|
| datos de importacion|| cuerpo||


### Parámetro de opción de importación de datos

**Los parámetros importantes se describen en la siguiente tabla.**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>BatchData</td><td>Lista<CellValue></td> <td>datos por lotes</td> </tr>
    <tr> <td>DestinationWorksheet</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero Falso.</td></tr>
    <tr><td>Tipo de datos de importación</td><td> Cadena</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr> <td>Fuente</td><td> Origen del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>ConvertNumericData</td><td>Cadena</td> <td>verdadero Falso.</td> </tr>
    <tr> <td>Primera fila</td><td>En t</td> <td></td> </tr>
    <tr> <td>Primera columna</td><td>En t</td><td></td></tr>
    <tr><td>SeparatorString</td><td> Cadena</td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>Analizadores personalizados</td><td>Lista<CustomParserConfig></td><td></td></tr>
    <tr><td>Tipo de datos de importación</td><td> Cadena</td><td>CSVData</td></tr>
    <tr> <td>Fuente</td><td> Origen del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="3" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Primera fila</td><td>En t</td> <td></td> </tr>
    <tr> <td>Primera columna</td><td>En t</td><td></td></tr>
    <tr><td>esvertical</td><td>Cadena</td><td>verdadero Falso.</td></tr>
    <tr><td>Datos</td><td> Cadena[]</td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero Falso.</td></tr>
    <tr><td>Tipo de datos de importación</td><td> Cadena</td><td>Imagen</td></tr>
    <tr> <td>Fuente</td><td> Origen del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="4" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Primera fila</td><td>En t</td> <td></td> </tr>
    <tr> <td>Primera columna</td><td>En t</td><td></td></tr>
    <tr><td>Datos</td><td> Entero[,]</td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero Falso.</td></tr>
    <tr><td>Tipo de datos de importación</td><td> Cadena</td><td>TwoDimensionIntArray</td></tr>
    <tr> <td>Fuente</td><td> Origen del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Primera fila</td><td>En t</td> <td></td> </tr>
    <tr> <td>Primera columna</td><td>En t</td><td></td></tr>
    <tr><td>Datos</td><td> Doble[,]</td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero Falso.</td></tr>
    <tr><td>Tipo de datos de importación</td><td> Cadena</td><td>TwoDimensionDoubleArray</td></tr>
    <tr> <td>Fuente</td><td> Origen del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Primera fila</td><td>En t</td> <td></td> </tr>
    <tr> <td>Primera columna</td><td>En t</td><td></td></tr>
    <tr><td>Datos</td><td> Cadena[,]</td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero Falso.</td></tr>
    <tr><td>Tipo de datos de importación</td><td> Cadena</td><td>Matriz de cadena de dos dimensiones</td></tr>
    <tr> <td>Fuente</td><td> Origen del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Primera fila</td><td>En t</td> <td></td> </tr>
    <tr> <td>Primera columna</td><td>En t</td><td></td></tr>
    <tr><td>esvertical</td><td>Cadena</td><td>verdadero Falso.</td></tr>
    <tr><td>Datos</td><td> Entero[]</td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero Falso.</td></tr>
    <tr><td>Tipo de datos de importación</td><td> Cadena</td><td>IntegerArray</td></tr>
    <tr> <td>Fuente</td><td> Origen del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>Primera fila</td><td>En t</td> <td></td> </tr>
    <tr> <td>Primera columna</td><td>En t</td><td></td></tr>
    <tr><td>esvertical</td><td>Cadena</td><td>verdadero Falso.</td></tr>
    <tr><td>Datos</td><td> Doble[]</td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero Falso.</td></tr>
    <tr><td>Tipo de datos de importación</td><td> Cadena</td><td>matriz doble</td></tr>
    <tr> <td>Fuente</td><td> Origen del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr> <td>fila superior izquierda</td><td>En t</td> <td></td> </tr>
    <tr> <td>Columna superior izquierda</td><td>En t</td><td></td></tr>
    <tr> <td>FilaInferiorDerecha</td><td>En t</td> <td></td> </tr>
    <tr> <td>Columna inferior derecha</td><td>En t</td><td></td></tr>
    <tr><td>Nombre del archivo</td><td>Cadena</td><td></td></tr>
    <tr><td>Datos</td><td> Cadena</td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> Cadena</td><td> Nombre de la hoja de trabajo de destino.</td></tr>
    <tr><td>EsInsertar</td><td>Cadena</td><td>verdadero Falso.</td></tr>
    <tr><td>Tipo de datos de importación</td><td> Cadena</td><td>matriz de cadenas</td></tr>
    <tr> <td>Fuente</td><td> Origen del archivo</td><td>Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>índice de fila</td><td>En t</td> <td></td> </tr>
    <tr><td>índicecolumna</td><td>En t</td><td></td></tr>
    <tr><td>tipo</td><td>Cadena</td><td>tipo de datos</td></tr>
    <tr><td>valor</td><td> Cadena</td> <td></td></tr>
    <tr><td>estilo</td><td> Estilo (objeto)</td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parámetro</th><th scope="col">Tipo</th> <th scope="col">Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>Cadena</td> <td>InMemoryFiles/CloudFileSystem/RequestFiles</td> </tr>
    <tr><td>Ruta de archivo</td><td>Cadena</td><td> posición del archivo</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## Cómo llamar a las API de RSET

Los siguientes artículos explican cada API cómo llamar en detalle y contienen cURL y SDK Ejemplos de cada API:

- [Cómo importar datos en archivos Excel sin usar almacenamiento.](/cells/es/import/without-using-storage)
- [Cómo importar datos en archivos Excel con almacenamiento.](/cells/es/import/with-using-storage)
- [Cómo importar datos de lote en la hoja de trabajo Excel](/cells/es/import/batch-data/)
- [Cómo importar datos CSV en la hoja de trabajo Excel](/cells/es/import/csv-data/)
- [Cómo importar una imagen a la hoja de trabajo Excel](/cells/es/import/picture/)
- [Cómo importar Integer Array en la hoja de trabajo Excel](/cells/es/import/integer-array/)
- [Cómo importar Double Array en la hoja de trabajo Excel](/cells/es/import/double-array/)
- [Cómo importar String Array en la hoja de trabajo Excel](/cells/es/import/string-array/)
- [Cómo importar matriz de enteros de 2 dimensiones en la hoja de trabajo Excel](/cells/es/import/2dimension-integer-array/)
- [Cómo importar matriz doble de 2 dimensiones en la hoja de trabajo Excel](/cells/es/import/2dimension-double-array/)
- [Cómo importar matriz de cadenas de 2 dimensiones en la hoja de trabajo Excel](/cells/es/import/2dimension-string-array/)
