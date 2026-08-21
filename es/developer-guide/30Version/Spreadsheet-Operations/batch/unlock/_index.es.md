---
title: "Desbloqueo por lotes"
second: "Documento"
type: docs
url: /batch/unlock
keywords: "desbloqueo por lotes, Aspose.Cells Cloud, Excel, API REST, hoja de cálculo, SDK en la nube"
description: "Desbloquea múltiples archivos de Excel en lotes utilizando la API REST de Aspose.Cells Cloud. Admite SDK para C#, Java, Python y otros lenguajes."
weight: 100
---

Esta API REST desbloquea archivos de Excel aptos en lotes.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/unlock
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo | Ubicación | Descripción |
|----------------------|------|-----------|-------------|
| **BatchLockRequest** |  | body | Cuerpo de la solicitud que contiene la configuración de desbloqueo. |

### Propiedades de **BatchLockRequest**

| Nombre          | Tipo                     | Descripción                                         | Notas       |
|-----------------|--------------------------|-----------------------------------------------------|-------------|
| SourceFolder    | string                   | Carpeta que contiene los archivos de Excel de origen. | [opcional] |
| MatchCondition  | MatchConditionRequest    | Criterios utilizados para seleccionar archivos que se desbloquearán. | [opcional] |
| Password        | string                   | Contraseña aplicada a los libros protegidos.        | [opcional] |
| OutFolder       | string                   | Carpeta de destino para los archivos desbloqueados.  | [opcional] |

### Propiedades de **MatchConditionRequest**

| Nombre             | Tipo      | Descripción                                 | Notas       |
|--------------------|-----------|---------------------------------------------|-------------|
| RegexPattern       | string    | Expresión regular para coincidir con nombres de archivo. | [opcional] |
| FullMatchConditions| string[]  | Condiciones exactas de nombre de archivo para coincidir. | [opcional] |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción                                    |
|----------------------|------|------------------------------------------------|
| data                 | file | Contenido binario del archivo de libro que se va a crear. |

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
| 401 Unauthorized | Token ausente o inválido | Error de autenticación                     |
| 409 Conflict | El archivo existe y `isWriteOver=false` | Conflicto con el archivo existente           |

## Cómo utilizar la API PostBatchLock con SDK

### Especificación de la API PostBatchLock

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchUnlock) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/unlock" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"SourceFolder":"CellsTests","OutFolder":"Output","MatchCondition":{"RegexPattern":"(^Book)(.+)(xlsx$)"},"Password":"123456"}'
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

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar funcionalidad de desbloqueo. Un SDK abstracta los detalles de bajo nivel para que pueda centrarse en su lógica empresarial. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}