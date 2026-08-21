---
title: "Importar datos CSV en una hoja de cálculo de Excel"
second_title: "Document"
linktype: "Importar datos CSV"
type: docs
url: /es/import-CSV-data-into-excel/
aliases:
  - /import-CSV-data-into-worksheet/
  - /import-data/csv-data/
  - /import/csv-data/
keywords: "Importar datos CSV, Excel, Aspose.Cells Cloud, API REST, hoja de cálculo, importación de CSV"
description: "La API REST de Aspose.Cells Cloud permite importar datos CSV en hojas de cálculo de Excel. Los SDK admitidos incluyen Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby y Swift."
weight: 19
---

Esta **API REST importa datos CSV** en una hoja de cálculo de Excel.

La solicitud es una solicitud HTTP con contenido multipart (consulte [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del contenido multipart contiene los datos `ImportCSVDataOption`, y la segunda parte contiene el archivo CSV.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en tokens JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

Los parámetros importantes se describen en las tablas a continuación.

### ImportCSVDataOption

| Nombre del parámetro | Tipo                       | Descripción                                                                 |
| ------------------- | -------------------------- | --------------------------------------------------------------------------- |
| SeparatorString     | string                     | Carácter utilizado para separar campos en el archivo CSV (por ejemplo, `,` o `;`). |
| ConvertNumericData  | string (`true`/`false`)    | Indica si las cadenas numéricas deben convertirse en valores numéricos.     |
| FirstRow            | int                        | Índice (basado en 1) de la primera fila donde se colocarán los datos.       |
| FirstColumn         | int                        | Índice (basado en 1) de la primera columna donde se colocarán los datos.     |
| SourceFile          | string                     | Nombre del archivo CSV de origen que se va a importar.                      |
| CustomParsers       | List\<CustomParserConfig\> | Colección de configuraciones de analizadores personalizados para columnas específicas. |

### CustomParserConfig

| Nombre del parámetro | Tipo   | Descripción                                                           |
| ------------------- | ------ | --------------------------------------------------------------------- |
| ColumnIndex         | int    | Índice (basado en 0) de la columna a la que se aplica el analizador personalizado. |
| ParseMethod         | string | Método de análisis para la columna (por ejemplo, `ToString`, `ToDate`, `ToNumber`). |
| CustomStyle         | string | Estilo personalizado (por ejemplo, formato numérico) aplicado a las celdas analizadas. |

**Ejemplo**

```xml
<ImportCSVDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>true</IsInsert>
    <ImportDataType>CSVData</ImportDataType>
    <SeparatorString>;</SeparatorString>
    <ConvertNumericData>true</ConvertNumericData>
    <FirstRow>1</FirstRow>
    <FirstColumn>2</FirstColumn>
    <SourceFile>TestImportDataCSV.CSV</SourceFile>
    <CustomParsers>
        <CustomParserConfig>
            <ColumnIndex>0</ColumnIndex>
            <ParseMethod>ToString</ParseMethod>
            <CustomStyle>#</CustomStyle>
        </CustomParserConfig>
    </CustomParsers>
</ImportCSVDataOption>
```
### Respuesta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado               | Descripción                                                   |
|--------|---------------------------|---------------------------------------------------------------|
| 200    | OK                        | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Petición inválida         | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado             | Token JWT inválido o ausente.                                 |
| 413    | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño.              |
| 500    | Error interno del servidor | Error inesperado en el servidor.                             |

## Cómo utilizar la API PostImportData con SDK

### Especificación de la API PostImportData

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) define una interfaz de programación accesible públicamente que le permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en la lógica de su negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

El siguiente ejemplo de código muestra cómo llamar al servicio web de Aspose.Cells utilizando el SDK de PHP:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}
{{< /tab >}}
{{< /tabs >}}