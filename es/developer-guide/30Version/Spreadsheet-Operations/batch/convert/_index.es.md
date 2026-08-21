---
title: "Conversión por lotes de archivos de Excel"
second_title: "Documento"
type: docs
url: /batch/convert
keywords: "conversión por lotes, Excel, Aspose.Cells Cloud, API REST, PDF, CSV, JSON, Markdown, hoja de cálculo"
description: "Aprenda a utilizar la API de Aspose.Cells Cloud para convertir por lotes varios archivos de Excel en formatos como PDF, CSV, JSON o Markdown. Esta guía incluye detalles sobre los puntos finales de la API REST, parámetros de solicitud, ejemplo de cURL y fragmentos de código SDK para varios lenguajes."
weight: 100
---

Esta API REST permite la **conversión por lotes** de archivos compatibles.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/convert
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                           |
|----------------------|--------|-----------|-------------------------------------------------------|
| **batchConvertRequest** | objeto | cuerpo    | Cuerpo de la solicitud que contiene la configuración de conversión. |

#### Propiedades de BatchConvertRequest

| Nombre             | Tipo                  | Descripción                                           | Notas       |
|--------------------|-----------------------|-------------------------------------------------------|-------------|
| **SourceFolder**   | string                | Ruta a la carpeta que contiene los archivos de Excel de origen. | [opcional]  |
| **MatchCondition** | MatchConditionRequest | Condiciones utilizadas para seleccionar archivos para la conversión. | [opcional]  |
| **Format**         | string                | Formato de destino para la conversión (por ejemplo, `pdf`, `csv`). | [opcional]  |
| **OutFolder**      | string                | Carpeta de destino donde se guardarán los archivos convertidos. | [opcional]  |
| **SaveOptions**    | SaveOptions           | Opciones adicionales que controlan cómo se guardan los archivos. | [opcional]  |

#### Propiedades de MatchConditionRequest

| Nombre                  | Tipo       | Descripción                                          | Notas       |
|-------------------------|------------|------------------------------------------------------|-------------|
| **RegexPattern**        | string     | Expresión regular utilizada para filtrar nombres de archivos. | [opcional]  |
| **FullMatchConditions** | string[]   | Lista de condiciones exactas de nombres de archivos para coincidencia. | [opcional]  |


### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción                                    |
| --------------------- | ---- | ---------------------------------------------- |
| data                  | archivo | Contenido binario del archivo de libro para crear. |
  
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

| Código | Significado                  | Cuándo se devuelve                     |
|--------|------------------------------|----------------------------------------|
| 200 OK | Libro creado correctamente   | Flujo normal                           |
| 201 Created | Libro creado (respuesta alternativa) | Cuando la API devuelve un estado de creado |
| 400 Bad Request | Parámetros inválidos | Error del lado del cliente             |
| 401 Unauthorized | Token faltante o inválido | Error de autenticación               |
| 409 Conflict | El archivo ya existe y `isWriteOver=false` | Conflicto con el archivo existente |

## Cómo utilizar la API PostBatchConvert con SDK

### Especificación de la API PostBatchConvert

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/PostBatchConvert) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/convert" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\",\"SaveOptions\":{\"SaveFormat\":\"pdf\",\"CalculateFormula\":true,\"EnableHTTPCompression\":true,\"OnePagePerSheet\":true,\"CreateDirectory\":false,\"Compliance\":\"None\"}}"
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

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Batch-Convet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Batch-Convet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-Batch-Convet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Batch-Convet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Batch-Convet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Batch-Convet.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Batch-Convet.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d763dc80b0aff6275403dc1d82ad59a5" "Examples-Batch-Convet.go" >}}

{{< /tab >}}

{{< /tabs >}}