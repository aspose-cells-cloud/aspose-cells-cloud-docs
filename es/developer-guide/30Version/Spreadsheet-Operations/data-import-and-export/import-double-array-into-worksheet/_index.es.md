---
title: "Importar matriz doble en hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Importar matriz doble"
type: docs
url: /import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Aspose.Cells, importar matriz doble, API de Excel, SDK en la nube"
description: "Aprenda a importar una matriz doble en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye autenticación, formato de solicitud, parámetros, ejemplo en XML/JSON y detalles de respuesta."
weight: 20
ArticleTitle: "Importar matriz doble en hoja de cálculo de Excel – Guía de Aspose.Cells Cloud"
---

Esta API REST **importa datos de matriz doble** en una hoja de cálculo de Excel.

> **Requisitos previos:** Debe tener un token JWT válido antes de llamar a esta API. Consulte la guía de autenticación para más detalles.

Envía una solicitud HTTP con contenido **multipart** (consulte [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
La primera parte del cuerpo multipart contiene los datos de **ImportDoubleArrayOption** y la segunda parte contiene el archivo de datos.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

#### **ImportDoubleArrayOption**

| Nombre del parámetro | Tipo       | Descripción                                                                                               |
| --------------------- | ---------- | --------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Índice de fila (base cero) donde se colocarán los datos.                                                 |
| FirstColumn          | int        | Índice de columna (base cero) donde se colocarán los datos.                                              |
| IsVertical           | boolean    | `true` / `false` – determina si la matriz se inserta verticalmente (`true`) u horizontalmente (`false`). |
| Data                 | Double[]   | Matriz de valores dobles para importar.                                                                  |
| DestinationWorksheet | string     | Nombre de la hoja de cálculo de destino.                                                                 |
| IsInsert             | boolean    | `true` / `false` – si es `true`, los datos se insertan; si es `false`, se sobrescriben las celdas existentes. |
| ImportDataType       | string     | Tipo de datos que se importan (por ejemplo, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`). |
| Source               | FileSource | Especifica la ubicación del archivo de datos cuando el parámetro `BatchData` es nulo.                    |

#### Ejemplo (XML)

```xml
<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Data>1.99,1.9,2.0</Data>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>
```

#### Ejemplo (JSON)

```json
{
  "Data": [1.99, 1.9, 2.0],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 0,
  "FirstColumn": 0,
  "IsVertical": false,
  "IsInsert": true,
  "ImportDataType": "DoubleArray"
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

| Código | Significado                                   |
| ------ | --------------------------------------------- |
| 200    | Importación correcta                          |
| 400    | Solicitud incorrecta: datos faltantes o inválidos |
| 401    | No autorizado: token inválido o ausente       |
| 500    | Error interno del servidor                    |

### Manejo de errores

Cuando ocurre un error, la API devuelve un objeto JSON que contiene el código de error y un mensaje descriptivo. Ejemplo para una solicitud no autorizada:

```json
{
  "Code": 401,
  "Status": "Error"
}
```

Para obtener más información sobre operaciones de importación relacionadas, consulte las páginas de documentación sobre “Importar matriz doble de 2 dimensiones” e “Importar matriz entera”.

## Cómo usar la API PostImportData con SDK

### Especificación de la API PostImportData

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

Usar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}