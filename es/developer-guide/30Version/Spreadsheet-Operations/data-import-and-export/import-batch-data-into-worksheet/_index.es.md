---
title: "Importar datos por lotes en una hoja de cálculo de Excel"
second_title: "Document"
linktype: "Importar datos por lotes"
type: docs
url: /es/import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, API en la nube, importar datos por lotes, Excel, CSV, JSON, XML, matrices"
description: "Aprenda a importar datos por lotes (CSV, JSON, XML, matrices) en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye autenticación, ejemplos de solicitudes y respuestas, fragmentos de SDK y manejo de errores."
weight: 19
ArticleTitle: "Importar datos por lotes en una hoja de cálculo de Excel – Documentación de Aspose.Cells Cloud"
---

Esta API REST **importa datos por lotes** en una hoja de cálculo de Excel. Acepta una solicitud multiparte donde la primera parte contiene el objeto **ImportBatchDataOption** y la segunda parte lleva el archivo de datos real (CSV, JSON, XML, etc.).

La operación utiliza una solicitud HTTP con contenido multipart (consulte [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### ImportBatchDataOption

| Nombre del parámetro       | Tipo               | Descripción                                                                                                                                                                                   |
| -------------------------- | ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BatchData**              | `List<CellValue>`  | Colección de valores de celda que se escribirán directamente.                                                                                                                                |
| **DestinationWorksheet**   | `string`           | Nombre de la hoja de cálculo donde se importarán los datos.                                                                                                                                  |
| **IsInsert**               | `bool`             | Si es `true`, los datos se insertan y las celdas existentes se desplazan; si es `false`, los datos sobrescriben las celdas existentes.                                                       |
| **ImportDataType**         | `string`           | Formato de los datos que se van a importar. Valores permitidos: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**                 | `FileSource`       | Especifica la ubicación del archivo de datos cuando **BatchData** es `null`.                                                                                                                 |

### CellValue

| Nombre del parámetro | Tipo     | Descripción                                               |
| -------------------- | -------- | --------------------------------------------------------- |
| **rowIndex**         | `int`    | Índice de fila (base cero) de la celda de destino.        |
| **columnIndex**      | `int`    | Índice de columna (base cero) de la celda de destino.     |
| **type**             | `string` | Tipo de datos del valor (por ejemplo, `int`, `double`, `string`). |
| **value**            | `string` | El valor real que se escribirá en la celda.              |
| **style**            | `Style`  | Información opcional de estilo para la celda.            |

### FileSource

| Nombre del parámetro | Tipo     | Descripción                                                          |
| -------------------- | -------- | -------------------------------------------------------------------- |
| **FileSourceType**   | `string` | Origen del archivo: `InMemoryFiles`, `CloudFileSystem` o `RequestFiles`. |
| **FilePath**         | `string` | Ruta o identificador del archivo dentro del origen elegido.         |

### Ejemplo (XML)

```xml
<ImportBatchDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportBatchDataOption>
```

### Respuesta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                  | Descripción                                                        |
|--------|------------------------------|--------------------------------------------------------------------|
| 200    | Correcto                     | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta         | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado                | Token JWT no válido o faltante.                                    |
| 413    | Carga demasiado grande        | El archivo cargado supera el límite de tamaño.                    |
| 500    | Error interno del servidor   | Error inesperado en el servidor.                                   |

## Cómo usar la API PostImportData con SDK

### Especificación de la API PostImportData

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) define una interfaz de programación accesible públicamente que le permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

Usar un SDK es la forma más rápida de integrar esta funcionalidad. Los SDK manejan los detalles de bajo nivel para que pueda centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells con distintos SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}