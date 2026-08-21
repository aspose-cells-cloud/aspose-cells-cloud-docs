---
title: "Bloqueo por lotes de archivos Excel"
second_title: "Documento"
type: docs
url: /es/batch/lock
keywords: "bloqueo por lotes, Excel, Aspose.Cells, API en la nube, hoja de cálculo, protección de archivos"
description: "La API de Aspose.Cells en la nube permite el bloqueo por lotes de múltiples archivos Excel. Utilice el punto de conexión REST o cualquiera de los SDK admitidos (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, etc.) para bloquear archivos en masa."
weight: 100
---

Esta API REST permite el **bloqueo por lotes** de archivos Excel elegibles.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/lock
```

### **Seguridad y autenticación**

Las API de Aspose.Cells en la nube son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.


### Parámetros de solicitud

| Nombre del parámetro | Tipo               | Ubicación | Descripción                                 |
|----------------------|--------------------|-----------|---------------------------------------------|
| BatchLockRequest     | BatchLockRequest   | body      | Cuerpo JSON que contiene los parámetros de bloqueo. |

#### Propiedades de **BatchLockRequest**

| Nombre          | Tipo                     | Descripción                                            | Notas    |
|-----------------|--------------------------|--------------------------------------------------------|----------|
| SourceFolder    | string                   | Carpeta que contiene los archivos Excel de origen.     | opcional |
| MatchCondition  | MatchConditionRequest    | Condiciones utilizadas para seleccionar los archivos que se bloquearán. | opcional |
| Password        | string                   | Contraseña que se aplicará a los archivos bloqueados. | opcional |
| OutFolder       | string                   | Carpeta de destino para los archivos bloqueados.      | opcional |

#### Propiedades de **MatchConditionRequest**

| Nombre             | Tipo      | Descripción                                          | Notas    |
|--------------------|-----------|------------------------------------------------------|----------|
| RegexPattern       | string    | Patrón de expresión regular para coincidir con nombres de archivos. | opcional |
| FullMatchConditions| string[]  | Coincidencias exactas de nombres de archivos para bloqueo. | opcional |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción                                    |
| ------------------- | ---- | ---------------------------------------------- |
| data                | file | Contenido binario del archivo de libro que se va a crear. |
  
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
| 200 OK | Libro creado correctamente      | Flujo normal                                 |
| 201 Created | Libro creado (respuesta alternativa) | Cuando la API devuelve un estado creado |
| 400 Bad Request | Parámetros inválidos | Error del lado del cliente                   |
| 401 Unauthorized | Token ausente o inválido | Error de autenticación                  |
| 409 Conflict | El archivo existe y `isWriteOver=false` | Conflicto con un archivo existente    

## Cómo utilizar la API PostBatchLock con SDK

### Especificación de la API PostBatchLock

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo llamar a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}"
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

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel para que pueda centrarse en sus tareas de bloqueo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchLock.go" >}}

{{< /tab >}}

{{< /tabs >}}