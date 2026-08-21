---
title: "División por lotes"
second_title: "Documento"
type: docs
url: /es/batch/split
keywords: "División por lotes, Aspose.Cells Cloud, API REST, Excel, PDF, CSV, JSON, hoja de cálculo, SDK en la nube"
description: "Documentación de la API REST de división por lotes de Aspose.Cells Cloud, que divide archivos de hojas de cálculo en múltiples formatos como PDF, CSV o JSON. Incluye detalles de la solicitud, comandos cURL de ejemplo y uso del SDK en varios lenguajes de programación."
weight: 100
---

Esta API REST realiza una **división por lotes** de los archivos elegibles.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/split
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo               | Ruta/Consulta/Cadena/Cuerpo HTTP | Descripción                                   |
|----------------------|--------------------|----------------------------------|-----------------------------------------------|
| BatchSplitRequest    | BatchSplitRequest  | body                             | Cuerpo de la solicitud que contiene las opciones de división. |

### Propiedades de **BatchSplitRequest**

| Nombre          | Tipo                | Descripción                                         | Notas        |
|-----------------|---------------------|-----------------------------------------------------|--------------|
| SourceFolder    | string              | Carpeta que contiene el archivo de origen.          | [opcional]   |
| SourceStorage   | string              | Nombre del almacenamiento donde reside el archivo de origen. | [opcional]   |
| MatchCondition  | MatchConditionRequest | Condiciones utilizadas para seleccionar archivos que se dividirán. | [opcional]   |
| Format          | string              | Formato de salida deseado (por ejemplo, pdf, csv). | [opcional]   |
| FromIndex       | integer             | Índice inicial de las páginas que se dividirán.    | [opcional]   |
| ToIndex         | integer             | Índice final de las páginas que se dividirán.      | [opcional]   |
| OutFolder       | string              | Carpeta de destino para los archivos divididos.    | [opcional]   |
| SaveOptions     | SaveOptions         | Opciones adicionales para guardar la salida.       | [opcional]   |

### Propiedades de **MatchConditionRequest**

| Nombre               | Tipo       | Descripción                                 | Notas        |
|----------------------|------------|---------------------------------------------|--------------|
| RegexPattern         | string     | Expresión regular para coincidir con nombres de archivos. | [opcional]   |
| FullMatchConditions  | string[]   | Lista de condiciones de coincidencia exacta. | [opcional]   |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción                                  |
|----------------------|------|----------------------------------------------|
| data                 | file | Contenido binario del archivo de libro para crear. |

### **Respuesta**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Códigos de estado HTTP**

| Código | Significado                     | Cuándo se devuelve                           |
|--------|---------------------------------|----------------------------------------------|
| 200 OK | Libro creado correctamente       | Flujo normal                                 |
| 201 Created | Libro creado (respuesta alternativa) | Cuando la API devuelve un estado de creado |
| 400 Bad Request | Parámetros inválidos | Error del lado del cliente                   |
| 401 Unauthorized | Token ausente o inválido | Error de autenticación                       |
| 409 Conflict | El archivo existe y `isWriteOver=false` | Conflicto con el archivo existente          |


## Cómo usar la API PostBatchSplit con SDK

### Especificación de la API PostBatchSplit

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en sus tareas de división. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}