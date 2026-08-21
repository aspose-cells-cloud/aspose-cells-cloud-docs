---
title: "Importar una matriz entera bidimensional en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Importar una matriz entera bidimensional"
type: docs
url: /import-a-2d-integer-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-integer-array-into-excel-worksheet/,
    /import-2dimension-integer-array-into-worksheet/,
    /import-data/2dimension-integer-array/,
    /import/2dimension-integer-array/,
  ]
keywords: "Aspose.Cells Cloud, importar matriz entera 2D, hoja de cálculo de Excel, API REST, SDK, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "La API REST de Aspose.Cells Cloud permite importar matrices enteras bidimensionales en hojas de cálculo de Excel. Los SDKs están disponibles para Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby y Swift."
weight: 20
---

Esta **API REST importa una matriz entera bidimensional** en una hoja de cálculo de Excel.

La solicitud es una solicitud HTTP con contenido multipart (consulte [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del contenido multipart contiene los datos `Import2DimensionIntegerArrayOption`, y la segunda parte contiene el archivo de datos.

Los parámetros importantes se describen en la siguiente tabla:

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Import2DimensionIntegerArrayOption**

| Nombre del parámetro   | Tipo       | Descripción                                                                                                                                                                                  |
| ---------------------- | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow               | int        | Índice basado en 1 de la primera fila donde se colocarán los datos.                                                                                                                          |
| FirstColumn            | int        | Índice basado en 1 de la primera columna donde se colocarán los datos.                                                                                                                       |
| Data                   | Integer[,] | Matriz entera bidimensional que contiene los valores que se van a importar.                                                                                                                 |
| DestinationWorksheet   | string     | Nombre de la hoja de cálculo de destino.                                                                                                                                                    |
| IsInsert               | string     | `"true"` para insertar los datos (desplazando las celdas existentes), `"false"` para sobrescribir las celdas existentes.                                                                    |
| ImportDataType         | string     | Especifica el formato de los datos. Valores admitidos: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| Source                 | FileSource | Indica la ubicación del archivo de datos cuando el parámetro `BatchData` es `null`.                                                                                                         |

### **Ejemplo**

```json
{
  "Data": [
    [1, 2],
    [3, 4]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionIntArray"
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

| Código | Significado                 | Descripción                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                                              |
| 413    | Carga útil demasiado grande | El archivo subido supera el límite de tamaño.                              |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                                            |

## Cómo utilizar la API PostImportData con SDKs

### Especificación de la API PostImportData

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) define una interfaz de programación accesible públicamente que permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDKs de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDKs:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}