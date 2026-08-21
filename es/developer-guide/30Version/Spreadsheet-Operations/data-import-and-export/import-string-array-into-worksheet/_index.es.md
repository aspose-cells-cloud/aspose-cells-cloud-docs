---
title: "Importar matriz de cadenas en hoja de cálculo de Excel – Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Importar matriz de cadenas"
type: docs
url: /import-string-array-into-excel-worksheet/
aliases:
  - /import-string-array-into-worksheet/
  - /import-data/string-array/
  - /import/string-array/
keywords: "Aspose.Cells Cloud, importar matriz de cadenas, API REST de Excel, carga multipart, importación de datos en hoja de cálculo, SDK en la nube"
description: "Aprenda cómo importar una matriz de cadenas en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye formato de solicitud, parámetros y ejemplos de SDK."
weight: 40
ArticleTitle: "Importar matriz de cadenas en hoja de cálculo de Excel – Aspose.Cells Cloud"
---

Importar una matriz de cadenas en una hoja de cálculo de Excel es una tarea común al poblar hojas con datos basados en listas. Esta operación resulta útil en escenarios como cargar valores de configuración, transferir datos desde fuentes externas o inicializar hojas con colecciones predefinidas de cadenas.

**Requisitos previos:**  
- Un token JWT válido obtenido mediante el flujo de autenticación de Aspose.Cells Cloud.  
- Un libro existente (o la capacidad de crear uno) en el almacenamiento de Aspose Cloud.  
- La versión adecuada del SDK que admite el modelo `ImportStringArrayOption`.

Esta API REST importa datos de matriz de cadenas en una hoja de cálculo de Excel.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

La solicitud utiliza contenido HTTP multipart (consulte [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
La primera parte del cuerpo multipart contiene una carga útil **ImportStringArrayOption**; la segunda parte contiene el archivo de datos de origen.

Los parámetros importantes se describen en la siguiente tabla:

<caption>Parámetros de ImportStringArrayOption</caption>
### **ImportStringArrayOption**

| Nombre del parámetro | Tipo       | Descripción                                                                                                                                                                         |
| -------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Índice de fila inicial (basado en 1) donde se colocarán los datos.                                                                                                                     |
| FirstColumn          | int        | Índice de columna inicial (basado en 1) donde se colocarán los datos.                                                                                                                  |
| IsVertical           | boolean    | `true` para insertar los datos verticalmente; `false` para insertar horizontalmente.                                                                                                                   |
| Data                 | String[]   | Matriz de cadenas que se va a importar.                                                                                                                                                    |
| DestinationWorksheet | string     | Nombre de la hoja de cálculo que recibirá los datos.                                                                                                                               |
| IsInsert             | boolean    | `true` para insertar filas/columnas (desplazando las celdas existentes); `false` para sobrescribir las celdas existentes.                                                                                       |
| ImportDataType       | string     | Tipo de datos que se importan (por ejemplo, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source               | FileSource | Describe dónde reside el archivo de datos cuando **BatchData** es null (por ejemplo, `CloudFileSystem`, `LocalFile`). Obligatorio si no se proporciona `BatchData`.                                   |

### Ejemplo

```xml
<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>
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

| Código | Significado                                 |
| ---- | --------------------------------------- |
| 200  | Importación realizada con éxito                        |
| 400  | Solicitud incorrecta: datos faltantes o no válidos   |
| 401  | No autorizado: token no válido o ausente |
| 500  | Error interno del servidor                   |


## Cómo usar la API PostImportData con SDK

### Especificación de la API PostImportData

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}