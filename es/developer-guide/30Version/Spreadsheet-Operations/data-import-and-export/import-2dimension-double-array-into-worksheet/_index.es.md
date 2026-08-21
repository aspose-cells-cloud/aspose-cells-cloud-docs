---
title: "Importar una matriz doble bidimensional en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Importar una matriz doble bidimensional"
type: docs
url: /es/import-a-2d-double-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-double-array-into-excel-worksheet/,
    /import-2dimension-double-array-into-worksheet/,
    /import-data/2dimension-double-array/,
    /import/2dimension-double-array/,
  ]
keywords: "Importar matriz doble bidimensional, Excel, Aspose Cells Cloud, API REST, hoja de cálculo, importación de datos"
description: "Aprenda cómo importar una matriz doble bidimensional en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye el formato de solicitud, los parámetros y ejemplos de código en SDK."
weight: 20
---

Esta **API REST importa una matriz doble bidimensional** en una hoja de cálculo de Excel.

La solicitud es un `POST` HTTP con contenido multipart (consulte [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del cuerpo multipart contiene los datos **Import2DimensionDoubleArrayOption**, y la segunda parte contiene el archivo de datos de origen.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

Los parámetros importantes se describen en la siguiente tabla:

### Import2DimensionDoubleArrayOption

| Nombre del parámetro | Tipo         | Descripción                                                                                                             |
| ------------------------ | ------------ | ----------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | `int`        | Índice de fila (basado en 1) donde comienza la importación.                                                            |
| **FirstColumn**          | `int`        | Índice de columna (basado en 1) donde comienza la importación.                                                         |
| **Data**                 | `Double[,]`  | Matriz bidimensional de valores dobles que se va a importar.                                                          |
| **DestinationWorksheet** | `string`     | Nombre de la hoja de cálculo que recibirá los datos.                                                                   |
| **IsInsert**             | `string`     | `"true"` para insertar filas, `"false"` para sobrescribir celdas existentes.                                         |
| **ImportDataType**       | `string`     | Tipo de datos que se importa (por ejemplo, `IntArray`, `DoubleArray`, `TwoDimensionDoubleArray`, `BatchData`, `csvData`, etc.). |
| **Source**               | `FileSource` | Indica la ubicación del archivo de datos cuando el parámetro `BatchData` es nulo.                                    |

**Ejemplo**

```json
{
  "Data": [
    [1.0, 2.9, 3.1],
    [2.0, 2.1, 3.1]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "importDataType": "TwoDimensionDoubleArray"
}
```

### Respuesta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                        |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400  | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401  | No autorizado               | Token JWT inválido o faltante. |
| 413  | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño. |
| 500  | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo usar la API PostImportData con SDK

### Especificación de la API PostImportData

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) define una interfaz de programación públicamente accesible que le permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

Usar un SDK es la forma más rápida de integrar esta funcionalidad. Los SDK gestionan los detalles de bajo nivel para que pueda centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}