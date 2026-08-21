---
title: "Protección por lotes de archivos Excel"
second_title: "Documento"
type: docs
url: /es/batch/protect
keywords: "Protección por lotes de archivos Excel, Aspose Cells Cloud, API REST, protección de Excel, protección por lotes"
description: "Aprenda a usar la API REST de Aspose.Cells Cloud para proteger por lotes múltiples archivos Excel. Incluye detalles de la solicitud, ejemplo de cURL y ejemplos de código SDK para varios lenguajes."
weight: 100
---

Esta API REST permite la **protección por lotes** de archivos Excel compatibles.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/protect
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro    | Tipo                | Ubicación | Descripción                                                                                              |
|-------------------------|---------------------|-----------|----------------------------------------------------------------------------------------------------------|
| batchProtectRequest     | BatchProtectRequest | body      | Payload JSON que especifica la carpeta de origen, las condiciones de coincidencia, el tipo de protección, la contraseña y la carpeta de salida. |

### Propiedades de BatchProtectRequest

| Nombre            | Tipo                     | Descripción                                                                                 | Notas |
|-------------------|--------------------------|---------------------------------------------------------------------------------------------|-------|
| SourceFolder      | string                   | Carpeta que contiene los archivos Excel de origen.                                          | opcional |
| MatchCondition    | MatchConditionRequest   | Criterios utilizados para seleccionar archivos que proteger.                                | opcional |
| ProtectionType    | string                   | Tipo de protección que aplicar (por ejemplo, `All`, `ReadOnly`).                            | opcional |
| Password          | string                   | Contraseña que establecer para los archivos protegidos.                                     | opcional |
| OutFolder         | string                   | Carpeta de destino para los archivos protegidos.                                            | opcional |

### Propiedades de MatchConditionRequest

| Nombre              | Tipo       | Descripción                                   | Notas |
|---------------------|------------|-----------------------------------------------|-------|
| RegexPattern        | string     | Expresión regular utilizada para coincidir con nombres de archivo. | opcional |
| FullMatchConditions | string[]   | Lista de condiciones exactas de nombre de archivo. | opcional |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción                                    |
| ------------------- | ---- | ---------------------------------------------- |
| data                | file | Contenido binario del archivo de libro que crear. |

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

| Código | Significado                 | Cuándo se devuelve                      |
|--------|-----------------------------|-----------------------------------------|
| 200 OK | Libro creado correctamente  | Flujo normal                            |
| 201 Created | Libro creado (respuesta alternativa) | Cuando la API devuelve un estado de creado |
| 400 Bad Request | Parámetros no válidos | Error del lado del cliente              |
| 401 Unauthorized | Token ausente o no válido | Error de autenticación                 |
| 409 Conflict | El archivo ya existe y `isWriteOver=false` | Conflicto con el archivo existente     |

## Cómo usar la API PostProtectConvert con SDK

### Especificación de la API PostProtectConvert

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/PostProtectConvert) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/protect" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\",\"ProtectionType\":\"All\"}"
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

Usar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}
---