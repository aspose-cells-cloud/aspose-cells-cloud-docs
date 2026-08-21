---
title: "Importar matriz de enteros en una hoja de cálculo de Excel"
linktitle: "Importar matriz de enteros"
type: docs
url: /es/import-integer-array-into-excel-worksheet/
aliases:
  - /import-integer-array-into-excel-worksheet/
  - /import-integer-array-into-worksheet/
  - /import-data/integer-array/
  - /import/integer-array/
keywords: "Aspose.Cells Cloud, Excel, importar matriz de enteros, API REST, SDK, C#, PHP, Ruby, Java, Python"
description: "Aprenda cómo importar una matriz de enteros en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye sintaxis de solicitud, parámetros, código de ejemplo para múltiples SDK y detalles de respuesta."
weight: 30
ArticleTitle: "Importar matriz de enteros en una hoja de cálculo de Excel – API de Aspose.Cells Cloud"
---

Esta API REST importa una matriz de enteros en una hoja de cálculo de Excel.

La solicitud debe ser una solicitud HTTP **POST** con contenido multipart (consulte [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del cuerpo multipart contiene la carga útil JSON **ImportIntegerArrayOption**, y la segunda parte contiene el archivo de datos de origen (por ejemplo, un archivo CSV o un archivo binario de Excel).

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

Ambos puntos finales aceptan la misma carga útil multipart. El primer punto final realiza una operación de importación genérica, mientras que el segundo apunta a un libro de trabajo específico identificado por `{name}`.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

### ImportIntegerArrayOption

| Nombre del parámetro     | Tipo       | Descripción                                                                                                                                                                                    |
| ------------------------ | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | int        | Índice basado en cero de la primera fila donde se colocarán los datos.                                                                                                                         |
| **FirstColumn**          | int        | Índice basado en cero de la primera columna donde se colocarán los datos.                                                                                                                      |
| **IsVertical**           | boolean    | `true` para insertar la matriz verticalmente (en una columna); `false` para insertarla horizontalmente (en una fila).                                                                         |
| **Data**                 | Integer[]  | La matriz de enteros que se importará.                                                                                                                                                        |
| **DestinationWorksheet** | string     | Nombre de la hoja de cálculo que recibirá los datos.                                                                                                                                          |
| **IsInsert**             | boolean    | `true` para insertar filas/columnas antes de escribir los datos; `false` para sobrescribir celdas existentes.                                                                                |
| **ImportDataType**       | string     | Tipo de datos que se importan. Valores válidos: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | FileSource | Indica la posición del archivo de datos cuando el parámetro **BatchData** es `null`.                                                                                                          |

#### Ejemplo de cuerpo de solicitud

```json
{
  "Data": [1, 2, 4],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 1,
  "FirstColumn": 2,
  "IsVertical": true,
  "IsInsert": true,
  "ImportDataType": "IntArray"
}
```

### Respuesta

Una solicitud correcta devuelve **HTTP 200** con una carga útil JSON similar a:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Códigos de estado posibles:

| Código | Significado                               |
| ------ | ----------------------------------------- |
| 200    | Importación exitosa                       |
| 400    | Solicitud incorrecta: datos faltantes o no válidos |
| 401    | No autorizado: token no válido o faltante |
| 500    | Error interno del servidor                |

## Cómo utilizar la API PostImportData con SDK

### Especificación de la API PostImportData

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) define una interfaz de programación pública accesible y permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de integrar esta funcionalidad. Los SDK ocultan los detalles de bajo nivel, permitiéndole centrarse en la lógica de su negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}