---
title: "Importar datos en archivos de Excel y exportar datos desde archivos de Excel"
second_title: "Document"
linktitle: "Importación y exportación de datos"
type: docs
url: /data-import-and-export/
keywords: "Aspose.Cells Cloud, importar datos, exportar Excel, API, CSV, JSON, imagen, matriz"
description: "Aprenda a importar datos desde CSV, JSON, matrices e imágenes en archivos de Excel y a exportar libros de trabajo, gráficos y formas a PDF, PNG y otros formatos utilizando la API de Aspose.Cells Cloud (v3.0)."
weight: 25
---

La API de Aspose.Cells Cloud admite la importación de datos desde diversas fuentes y permite exportar libros de trabajo, gráficos y otros objetos de Excel a distintos formatos, incluidos **XLSX**, **CSV**, **PDF**, **HTML**, **PNG**, entre otros. Esto simplifica y agiliza la gestión y el intercambio de datos.

**Versión de la API:** **v3.0** – Última actualización: **2024‑03‑15**

### Guía de inicio rápido

1. **Preparar la carga útil (payload)** – Construya un cuerpo JSON que describa las opciones de importación o exportación (por ejemplo, `ImportCSVDataOption`, `ExportOptions`).
2. **Enviar la solicitud** – Utilice `curl`, Postman o un SDK para llamar al punto de acceso adecuado (`POST /cells/import` o `POST /cells/export`).
3. **Procesar la respuesta** – En caso de éxito, recibirá el archivo procesado (binario o en Base64). En caso de error, revise el código de estado HTTP y el mensaje de error devuelto en el cuerpo JSON.

#### Requisitos previos

- Una cuenta activa de Aspose Cloud y un token JWT válido.
- El libro de trabajo de destino debe existir en la ubicación especificada del almacenamiento (para las API basadas en almacenamiento).
- Cabeceras `Content‑Type` correctas (`multipart/form-data` para cargas de archivos, `application/json` para cuerpos JSON).

## Cómo importar datos desde diversas fuentes

La importación de datos en un archivo de Excel implica varias consideraciones que deben abordarse durante el proceso. La capacidad de importar múltiples formatos y tipos de datos con calidad profesional es una característica principal de Aspose.Cells Cloud.

### Información sobre las API de importación de datos

A continuación se presentan las API disponibles para importar datos en uno o varios archivos de Excel:

| API                                                                                                | Descripción                                                  |
| :------------------------------------------------------------------------------------------------- | :----------------------------------------------------------- |
| [POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)              | Importar datos en archivos de Excel sin utilizar almacenamiento. |
| [POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) | Importar datos en un archivo de Excel almacenado en la nube. |

### Parámetros de solicitud

#### Sin utilizar almacenamiento

| Nombre del parámetro | Tipo          | Ubicación | Descripción                                        |
| :------------------- | :------------ | :-------- | :------------------------------------------------- |
| file                 | file          | formData  | Archivo para cargar                                |
| ImportOption         | ImportOptions | body      | Especifica el formato de importación (IntArray, DoubleArray, StringArray, TwoDimensionIntArray, TwoDimensionDoubleArray, TwoDimensionStringArray, BatchData, csvData, Picture) |

#### Utilizando almacenamiento

| Nombre del parámetro | Tipo          | Ubicación | Descripción                    |
| :------------------- | :------------ | :-------- | :----------------------------- |
| name                 | string        | path      | Nombre del archivo de Excel    |
| folder               | string        | query     | Ruta de la carpeta en almacenamiento |
| storageName          | string        | query     | Nombre del almacenamiento      |
| importData           | ImportOptions | body      | Carga útil con datos a importar |

#### Parámetros de la opción de importación de datos

**Los parámetros más importantes se describen en las tablas siguientes:**

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}

{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th>Parámetro</th><th>Tipo</th><th>Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>BatchData</td><td>List&lt;CellValue&gt;</td><td>Datos por lotes para importar</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nombre de la hoja de destino</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica si se deben insertar los datos (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Ubicación del archivo de datos cuando BatchData es null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="2" >}}

<table class="table">
  <thead>
    <tr><th>Parámetro</th><th>Tipo</th><th>Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>ConvertNumericData</td><td>boolean</td><td>Indica si se deben convertir los datos numéricos (true/false)</td></tr>
    <tr><td>FirstRow</td><td>int</td><td>Índice de la primera fila</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Índice de la primera columna</td></tr>
    <tr><td>SeparatorString</td><td>string</td><td>Separador de columnas</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nombre de la hoja de destino</td></tr>
    <tr><td>CustomParsers</td><td>List&lt;CustomParserConfig&gt;</td><td>Configuraciones de analizadores personalizados</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>CSVData</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Ubicación del archivo de datos cuando BatchData es null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="3" >}}

<table class="table">
  <thead>
    <tr><th>Parámetro</th><th>Tipo</th><th>Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Índice de la primera fila</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Índice de la primera columna</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Indica si la imagen se coloca verticalmente (true/false)</td></tr>
    <tr><td>Data</td><td>string[]</td><td>Datos de la imagen (cadenas en Base64)</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nombre de la hoja de destino</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica si se deben insertar los datos (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>Picture</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Ubicación del archivo de datos cuando BatchData es null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="4" >}}

<table class="table">
  <thead>
    <tr><th>Parámetro</th><th>Tipo</th><th>Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Índice de la primera fila</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Índice de la primera columna</td></tr>
    <tr><td>Data</td><td>int[,] </td><td>Matriz entera bidimensional</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nombre de la hoja de destino</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica si se deben insertar los datos (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionIntArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Ubicación del archivo de datos cuando BatchData es null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th>Parámetro</th><th>Tipo</th><th>Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Índice de la primera fila</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Índice de la primera columna</td></tr>
    <tr><td>Data</td><td>double[,] </td><td>Matriz de doble precisión bidimensional</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nombre de la hoja de destino</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica si se deben insertar los datos (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionDoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Ubicación del archivo de datos cuando BatchData es null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th>Parámetro</th><th>Tipo</th><th>Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Índice de la primera fila</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Índice de la primera columna</td></tr>
    <tr><td>Data</td><td>string[,] </td><td>Matriz de cadenas bidimensional</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nombre de la hoja de destino</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica si se deben insertar los datos (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Ubicación del archivo de datos cuando BatchData es null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th>Parámetro</th><th>Tipo</th><th>Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Índice de la primera fila</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Índice de la primera columna</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Indica si la matriz es vertical (true/false)</td></tr>
    <tr><td>Data</td><td>int[] </td><td>Matriz entera unidimensional</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nombre de la hoja de destino</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica si se deben insertar los datos (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>IntegerArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Ubicación del archivo de datos cuando BatchData es null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th>Parámetro</th><th>Tipo</th><th>Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Índice de la primera fila</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Índice de la primera columna</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Indica si la matriz es vertical (true/false)</td></tr>
    <tr><td>Data</td><td>double[] </td><td>Matriz de doble precisión unidimensional</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nombre de la hoja de destino</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica si se deben insertar los datos (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>DoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Ubicación del archivo de datos cuando BatchData es null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="9" >}}

<table class="table">
  <thead>
    <tr><th>Parámetro</th><th>Tipo</th><th>Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>UpperLeftRow</td><td>int</td><td>Índice de fila superior izquierdo</td></tr>
    <tr><td>UpperLeftColumn</td><td>int</td><td>Índice de columna superior izquierdo</td></tr>
    <tr><td>LowerRightRow</td><td>int</td><td>Índice de fila inferior derecho</td></tr>
    <tr><td>LowerRightColumn</td><td>int</td><td>Índice de columna inferior derecho</td></tr>
    <tr><td>Filename</td><td>string</td><td>Nombre del archivo de origen</td></tr>
    <tr><td>Data</td><td>string</td><td>Datos de cadena a importar</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nombre de la hoja de destino</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica si se deben insertar los datos (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>StringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Ubicación del archivo de datos cuando BatchData es null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}

<table class="table">
  <thead>
    <tr><th>Parámetro</th><th>Tipo</th><th>Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td><td>Índice de fila de la celda</td></tr>
    <tr><td>columnIndex</td><td>int</td><td>Índice de columna de la celda</td></tr>
    <tr><td>type</td><td>string</td><td>Tipo de dato del valor de la celda</td></tr>
    <tr><td>value</td><td>string</td><td>Valor de la celda</td></tr>
    <tr><td>style</td><td>Style (object)</td><td>Definición del estilo de celda</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="11" >}}

<table class="table">
  <thead>
    <tr><th>Parámetro</th><th>Tipo</th><th>Descripción</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>string</td><td>InMemoryFiles, CloudFileSystem o RequestFiles</td></tr>
    <tr><td>FilePath</td><td>string</td><td>Ruta al archivo de origen</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< /tabs >}}

## Cómo exportar objetos de Excel a distintos formatos de archivo

Si originalmente creó un archivo de Excel en un formato como **XLS**, **XLSX**, **XLSB** o **CSV**, es posible que desee convertirlo a otro formato para aprovechar características específicas. Por ejemplo, exportar a **PDF** protege el contenido frente a modificaciones no autorizadas y facilita su lectura y compartición.

La exportación de objetos de Excel implica varias consideraciones. Aspose.Cells Cloud proporciona una exportación de alta calidad de libros de trabajo, gráficos, formas e imágenes a una amplia gama de formatos:

_Formatos solo para exportación_: PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS.  
_Formatos con importación y exportación_: XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT.

La solicitud utiliza contenido multiparto según lo definido en [RFC 2046] y [RFC 1341]. La primera parte contiene el archivo de datos; la segunda parte contiene las opciones de guardado.

### Información sobre la API de exportación

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

#### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                   |
| :------------------- | :----- | :-------- | :-------------------------------------------------------------------------------------------- |
| file                 | file   | formData  | Archivo para cargar                                                                           |
| objectType           | string | query     | Tipo de objeto (`workbook`, `worksheet`, `chart`, `shape`, `picture`, `listobject`, `oleobject`) |
| format               | string | query     | Formato de archivo de salida deseado (ver [Formatos de archivo admitidos](/cells/supported-file-formats/)) |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) define una interfaz de programación públicamente accesible que permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para llamar a la API. El ejemplo siguiente muestra una solicitud y su respuesta JSON.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/export" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@example1.xlsx' \
  -F 'file2=@example2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "example1.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "example2.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

#### Códigos de estado HTTP comunes

| Estado | Significado                                                   | Acción recomendada                           |
| ------ | ------------------------------------------------------------- | -------------------------------------------- |
| 200    | Correcto – el archivo se ha exportado                         | Procesar el/los archivo(s) devuelto(s)       |
| 400    | Solicitud incorrecta – parámetros faltantes o inválidos       | Verifique la carga útil y las cadenas de consulta |
| 401    | No autorizado – token JWT inválido o caducado                 | Actualice el token y vuelva a intentarlo     |
| 404    | No encontrado – el libro de trabajo o la hoja especificados no existen | Compruebe el nombre del archivo y la ruta del almacenamiento |
| 500    | Error interno del servidor – condición inesperada en el servidor | Póngase en contacto con el soporte técnico de Aspose con el ID de solicitud |

## Cómo llamar a las API de importación y exportación

Los siguientes artículos explican cada API en detalle y contienen ejemplos de cURL y SDK:

- [Cómo importar datos en archivos de Excel sin utilizar almacenamiento.](/cells/import/without-using-storage)
- [Cómo importar datos en archivos de Excel utilizando almacenamiento.](/cells/import/with-using-storage)
- [Cómo importar datos por lotes en una hoja de cálculo de Excel](/cells/import-batch-data-into-excel-worksheet/)
- [Cómo importar datos CSV en una hoja de cálculo de Excel](/cells/import-CSV-data-into-excel-worksheet/)
- [Cómo importar una imagen en una hoja de cálculo de Excel](/cells/import-picture-into-excel-worksheet/)
- [Cómo importar una matriz entera en una hoja de cálculo de Excel](/cells/import-integer-array-into-excel-worksheet/)
- [Cómo importar una matriz de doble precisión en una hoja de cálculo de Excel](/cells/import-double-array-into-excel-worksheet/)
- [Cómo importar una matriz de cadenas en una hoja de cálculo de Excel](/cells/import-string-array-into-excel-worksheet/)
- [Cómo importar una matriz entera bidimensional en una hoja de cálculo de Excel](/cells/import-a-2D-integer-array-into-excel-worksheet/)
- [Cómo importar una matriz de doble precisión bidimensional en una hoja de cálculo de Excel](/cells/import-a-2D-double-array-into-excel-worksheet/)
- [Cómo importar una matriz de cadenas bidimensional en una hoja de cálculo de Excel](/cells/import-a-2D-string-array-into-excel-worksheet/)
- [Exportar un gráfico de Excel a otro formato de archivo](/cells/export-excel-chart-to-different-formats/)
- [Exportar un objeto de lista de Excel a otro formato de archivo](/cells/export-excel-listobject-to-different-formats/)
- [Exportar un objeto OLE de Excel a otro formato de archivo](/cells/export-excel-ole-object/)
- [Exportar una imagen de Excel a otro formato de archivo](/cells/export-excel-picture-to-different-formats/)
- [Exportar una forma de Excel a otro formato de archivo](/cells/export-excel-shape-to-different-formats/)
- [Exportar un libro de trabajo de Excel a otro formato de archivo](/cells/export-excel-to-different-formats/)
- [Exportar una hoja de cálculo de Excel a otro formato de archivo](/cells/export-excel-worksheet-to-different-formats/)