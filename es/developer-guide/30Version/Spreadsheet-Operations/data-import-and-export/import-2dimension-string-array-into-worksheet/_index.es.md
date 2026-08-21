---
title: "Importar una matriz de cadenas de 2 dimensiones en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Importar una matriz de cadenas de 2 dimensiones"
type: docs
url: /es/import-a-2d-string-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-string-array-into-excel-worksheet/,
    /import-2dimension-string-array-into-worksheet/,
    /import-data/-2dimension-string-array/,
    /import-data/2dimension-string-array/,
    /import/2dimension-string-array/,
  ]
keywords: "Aspose.Cells Cloud, importar matriz de 2D de cadenas, Excel, API REST, SDK"
description: "Aprenda a usar la API REST de Aspose.Cells Cloud para importar una matriz de cadenas de dos dimensiones en una hoja de cálculo de Excel. Incluye el formato de solicitud, detalles de los parámetros y ejemplos de código SDK para C#, PHP y Ruby."
weight: 20
---

Esta **API REST importa una matriz de cadenas de dos dimensiones** en una hoja de cálculo de Excel.

La solicitud es una solicitud HTTP con contenido multipart (consulte [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del contenido multipart contiene los datos `Import2DimensionStringArrayOption` y la segunda parte contiene el archivo de datos.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

Los parámetros importantes se describen en la siguiente tabla:

### **Import2DimensionStringArrayOption**

| Nombre del parámetro   | Tipo                | Descripción                                                                         |
| ---------------------- | ------------------- | ----------------------------------------------------------------------------------- |
| FirstRow               | int                 | Índice basado en cero de la fila donde comienza la importación.                    |
| FirstColumn            | int                 | Índice basado en cero de la columna donde comienza la importación.                 |
| Data                   | String[,]           | Matriz bidimensional que contiene los valores de cadena que se van a importar.    |
| DestinationWorksheet   | string              | Nombre de la hoja de cálculo que recibirá los datos importados.                    |
| IsInsert               | string (true/false) | Si es **true**, los datos se insertan y las celdas existentes se desplazan.        |
| ImportDataType         | string              | Especifica el tipo de datos; para esta operación use `TwoDimensionStringArray`.   |
| Source                 | FileSource          | Indica la ubicación del archivo de datos cuando el parámetro `BatchData` es null.  |

### Ejemplo de cuerpo de solicitud

```json
{
  "Data": [
    ["1.0", "2.9"],
    ["2.0", "2.1"]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 1,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionStringArray"
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

| Código | Significado                 | Descripción                                                     |
|--------|-----------------------------|-----------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido).   |
| 401    | No autorizado               | Token JWT inválido o ausente.                                   |
| 413    | Payload demasiado grande     | El archivo subido excede el límite de tamaño.                   |
| 500    | Error interno del servidor  | Error inesperado del servidor.                                  |

## Cómo usar la API PostImportData con SDK

### Especificación de la API PostImportData

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) define una interfaz de programación accesible públicamente que le permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

Usar un SDK es la forma más rápida de integrar esta funcionalidad. Un SDK abstracte los detalles de bajo nivel, por lo que puede centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante varios SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}