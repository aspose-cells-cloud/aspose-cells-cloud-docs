---
title: "Aspose.Cells Cloud API – Gestión de archivos y carpetas (cargar, descargar, copiar, mover)"
second_title: "Documento"
ArticleTitle: "Gestión de archivos en la nube para Excel – Una solución eficiente y segura para el almacenamiento y la organización inteligente de archivos de Excel"
linktitle: "Archivos y almacenamiento"
type: docs
url: /es/files-and-storage/
aliases: [  /es/working-with-files-and-storage-using-aspose-cells-cloud/ ]
keywords: "Aspose.Cells Cloud, API de almacenamiento de archivos, cargar archivo de Excel, descargar archivo de Excel, copiar archivo, mover archivo, eliminar archivo, gestión de carpetas, API REST, ejemplos de cURL"
description: "Guía completa sobre cómo gestionar archivos y carpetas en el almacenamiento de Aspose.Cells Cloud. Incluye operaciones de carga, descarga, copia, movimiento, eliminación y gestión de carpetas, con ejemplos en cURL, parámetros necesarios y notas sobre autenticación."
weight: 100
---

Aspose.Cells Cloud proporciona un conjunto completo de funciones auxiliares para trabajar con archivos almacenados en el almacenamiento de Aspose.Cells Cloud o en cualquier almacenamiento en la nube de terceros de su elección. Para obtener ayuda sobre la configuración de almacenamiento de terceros, consulte [Temas de ayuda de la interfaz de usuario de Aspose Cloud](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Cloud ofrece una amplia gama de API para operaciones sobre archivos, carpetas y almacenamiento.**

> **Nota:** Todas las llamadas a la API deben utilizar **HTTPS**. Consulte la [Guía de autenticación](/cells/authentication/) para obtener detalles sobre cómo obtener un token JWT.

**Requisitos previos:** Para utilizar estas API, debe tener una cuenta válida de Aspose Cloud, obtener un token de acceso JWT y tener configurada una ubicación de almacenamiento (ya sea el almacenamiento de Aspose Cloud o un almacenamiento de terceros conectado).

**Última actualización:** 2024-12-01

## **Cómo cargar un archivo**

### Información de la API para cargar un archivo

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Los parámetros de la solicitud se indican a continuación:

| Nombre del parámetro | Tipo   | Ubicación | Descripción |
|----------------------|--------|-----------|-------------|
| path                 | string | path      | Ruta donde se cargará el archivo, incluyendo el nombre y la extensión del archivo (por ejemplo, `/carpeta1/Informe.xlsx`). |
| file                 | file   | formData  | El archivo que se va a cargar. |
| storageName          | string | query     | Nombre del almacenamiento que se va a utilizar. |

**Respuestas HTTP**

| Código | Descripción                               |
|--------|-------------------------------------------|
| 200    | Archivo cargado correctamente.            |
| 400    | Solicitud incorrecta: faltan o son inválidos los parámetros. |
| 401    | No autorizado: token JWT inválido o faltante. |
| 404    | Almacenamiento no encontrado.             |
| 500    | Error interno del servidor.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/File/UploadFile) define una interfaz de programación públicamente accesible que permite interacciones REST directamente desde un navegador web.

### Ejemplo de carga de archivo

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo cargar un archivo con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MiCarpeta/Informe.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <token jwt>" \
  -F "File=@Informe.xlsx"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```json
{
  "Uploaded": [
    "MiCarpeta/Informe.xlsx"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*Nota: El tamaño máximo de archivo para cargar es de 100 MB. Podrían aplicarse límites de tasa.*

## **Cómo descargar un archivo**

### Información de la API para descargar un archivo

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Los parámetros de la solicitud se indican a continuación:

| Nombre del parámetro | Tipo   | Ubicación | Descripción |
|----------------------|--------|-----------|-------------|
| path                 | string | path      | Ruta del archivo (por ejemplo, `/carpeta/Informe.xlsx`). |
| storageName          | string | query     | Nombre del almacenamiento que se va a utilizar. |
| versionId            | string | query     | Identificador de la versión del archivo que se va a descargar (opcional). |

**Respuestas HTTP**

| Código | Descripción                               |
|--------|-------------------------------------------|
| 200    | Archivo descargado; se devuelve una secuencia binaria. |
| 400    | Solicitud incorrecta: parámetros inválidos. |
| 401    | No autorizado: token JWT inválido o faltante. |
| 404    | Archivo no encontrado.                    |
| 500    | Error interno del servidor.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/File/DownloadFile) define una interfaz de programación públicamente accesible que permite interacciones REST directamente desde un navegador web.

### Ejemplo de descarga de archivo

{{< tabs tabTotal="2" tabID="13" tabName13="Solicitud" tabName14="Respuesta" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MiCarpeta/Informe.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```json
{
  "Stream": "<datos binarios>"
}
```

{{< /tab >}}
{{< /tabs >}}

*Nota: La respuesta contiene la secuencia binaria del archivo. Guarde la salida en un archivo al utilizar cURL (`-o nombre_archivo.xlsx`).*

## **Cómo eliminar un archivo**

### Información de la API para eliminar un archivo

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Los parámetros de la solicitud se indican a continuación:

| Nombre del parámetro | Tipo   | Ubicación | Descripción |
|----------------------|--------|-----------|-------------|
| path                 | string | path      | Ruta del archivo (por ejemplo, `/carpeta/Informe.xlsx`). |
| storageName          | string | query     | Nombre del almacenamiento que se va a utilizar. |
| versionId            | string | query     | Identificador de la versión del archivo que se va a eliminar (opcional). |

**Respuestas HTTP**

| Código | Descripción                               |
|--------|-------------------------------------------|
| 200    | Archivo eliminado correctamente.          |
| 400    | Solicitud incorrecta: faltan o son inválidos los parámetros. |
| 401    | No autorizado: token JWT inválido.        |
| 404    | Archivo no encontrado.                    |
| 500    | Error interno del servidor.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/File/DeleteFile) define una interfaz de programación públicamente accesible que permite interacciones REST directamente desde un navegador web.

### Ejemplo de eliminación de archivo

{{< tabs tabTotal="2" tabID="15" tabName15="Solicitud" tabName16="Respuesta" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MiCarpeta/ViejoInforme.xlsx" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Nota: La eliminación de un archivo es permanente; asegúrese de tener una copia de seguridad si es necesario.*

## **Cómo copiar un archivo**

### Información de la API para copiar un archivo

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

Los parámetros de la solicitud se indican a continuación:

| Nombre del parámetro   | Tipo   | Ubicación | Descripción |
|------------------------|--------|-----------|-------------|
| srcPath                | string | path      | Ruta del archivo de origen (por ejemplo, `/carpeta/Origen.xlsx`). |
| destPath               | string | query     | Ruta del archivo de destino (por ejemplo, `/carpeta/Destino.xlsx`). |
| srcStorageName         | string | query     | Nombre del almacenamiento de origen (opcional). |
| destStorageName        | string | query     | Nombre del almacenamiento de destino (opcional). |
| versionId              | string | query     | ID de versión del archivo que se va a copiar (opcional). |

**Respuestas HTTP**

| Código | Descripción                               |
|--------|-------------------------------------------|
| 200    | Archivo copiado correctamente.            |
| 400    | Solicitud incorrecta: parámetros inválidos. |
| 401    | No autorizado: token JWT inválido o faltante. |
| 404    | Archivo de origen no encontrado.          |
| 500    | Error interno del servidor.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/File/CopyFile) define una interfaz de programación públicamente accesible que permite interacciones REST directamente desde un navegador web.

### Ejemplo de copia de archivo

{{< tabs tabTotal="2" tabID="17" tabName17="Solicitud" tabName18="Respuesta" >}}
{{< tab tabNum="17" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/copy/MiCarpeta/Informe.xlsx?destPath=MiCarpeta/InformeCopia.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Nota: La operación de copia no elimina el archivo de origen.*

## **Cómo mover un archivo**

### Información de la API para mover un archivo

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

Los parámetros de la solicitud se indican a continuación:

| Nombre del parámetro   | Tipo   | Ubicación | Descripción |
|------------------------|--------|-----------|-------------|
| srcPath                | string | path      | Ruta del archivo de origen (por ejemplo, `/carpeta/Origen.xlsx`). |
| destPath               | string | query     | Ruta del archivo de destino (por ejemplo, `/carpeta/Destino.xlsx`). |
| srcStorageName         | string | query     | Nombre del almacenamiento de origen (opcional). |
| destStorageName        | string | query     | Nombre del almacenamiento de destino (opcional). |
| versionId              | string | query     | ID de versión del archivo que se va a mover (opcional). |

**Respuestas HTTP**

| Código | Descripción                               |
|--------|-------------------------------------------|
| 200    | Archivo movido correctamente.             |
| 400    | Solicitud incorrecta: parámetros inválidos. |
| 401    | No autorizado: token JWT inválido o faltante. |
| 404    | Archivo de origen no encontrado.          |
| 500    | Error interno del servidor.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/File/MoveFile) define una interfaz de programación públicamente accesible que permite interacciones REST directamente desde un navegador web.

### Ejemplo de movimiento de archivo

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/move/MiCarpeta/Informe.xlsx?destPath=MiCarpeta/InformeMovido.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Nota: Al mover un archivo se conserva su historial de versiones.*

## **Cómo crear una carpeta**

### Información de la API para crear una carpeta

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Los parámetros de la solicitud se indican a continuación:

| Nombre del parámetro | Tipo   | Ubicación | Descripción |
|----------------------|--------|-----------|-------------|
| path                 | string | path      | Ruta de la carpeta que se va a crear (por ejemplo, `carpeta1/carpeta2/`). |
| storageName          | string | query     | Nombre del almacenamiento que se va a utilizar. |

**Respuestas HTTP**

| Código | Descripción                               |
|--------|-------------------------------------------|
| 200    | Carpeta creada correctamente.             |
| 400    | Solicitud incorrecta: ruta o parámetros inválidos. |
| 401    | No autorizado: token JWT inválido o faltante. |
| 500    | Error interno del servidor.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) define una interfaz de programación públicamente accesible que permite interacciones REST directamente desde un navegador web.

### Ejemplo de creación de carpeta

{{< tabs tabTotal="2" tabID="3" tabName3="Solicitud" tabName4="Respuesta" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/nuevacarpeta" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```json
{
  "Uploaded": [
    "nuevacarpeta"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*Nota: Las rutas de carpetas distinguen mayúsculas y minúsculas.*

## **Cómo obtener los archivos de una carpeta**

### Información de la API para obtener archivos

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Los parámetros de la solicitud se indican a continuación:

| Nombre del parámetro | Tipo   | Ubicación | Descripción |
|----------------------|--------|-----------|-------------|
| path                 | string | path      | Ruta de la carpeta (por ejemplo, `/carpeta`). |
| storageName          | string | query     | Nombre del almacenamiento que se va a utilizar. |

**Respuestas HTTP**

| Código | Descripción                               |
|--------|-------------------------------------------|
| 200    | Lista de archivos y subcarpetas devuelta. |
| 400    | Solicitud incorrecta: ruta inválida.      |
| 401    | No autorizado: token JWT inválido o faltante. |
| 404    | Carpeta no encontrada.                    |
| 500    | Error interno del servidor.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) define una interfaz de programación públicamente accesible que permite interacciones REST directamente desde un navegador web.

### Ejemplo de obtención de archivos

{{< tabs tabTotal="2" tabID="5" tabName5="Solicitud" tabName6="Respuesta" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/carpeta1" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```json
{
  "Value": [
    {
      "Name": "Informe.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 102400,
      "Path": "/carpeta1/Informe.xlsx"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

*Nota: La respuesta enumera tanto archivos como subcarpetas dentro de la ruta especificada.*

## **Cómo eliminar una carpeta**

### Información de la API para eliminar una carpeta

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Los parámetros de la solicitud se indican a continuación:

| Nombre del parámetro | Tipo    | Ubicación | Descripción |
|----------------------|---------|-----------|-------------|
| path                 | string  | path      | Ruta de la carpeta (por ejemplo, `/carpeta`). |
| storageName          | string  | query     | Nombre del almacenamiento que se va a utilizar. |
| recursive            | boolean | query     | Establezca en `true` para eliminar la carpeta recursivamente. |

**Respuestas HTTP**

| Código | Descripción                               |
|--------|-------------------------------------------|
| 200    | Carpeta eliminada correctamente.          |
| 400    | Solicitud incorrecta: parámetros inválidos. |
| 401    | No autorizado: token JWT inválido o faltante. |
| 404    | Carpeta no encontrada.                    |
| 500    | Error interno del servidor.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) define una interfaz de programación públicamente accesible que permite interacciones REST directamente desde un navegador web.

### Ejemplo de eliminación de carpeta

{{< tabs tabTotal="2" tabID="7" tabName7="Solicitud" tabName8="Respuesta" >}}
{{< tab tabNum="7" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/carpeta1" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Nota: La eliminación de una carpeta con `recursive=true` elimina permanentemente todo su contenido.*

## **Cómo copiar una carpeta**

### Información de la API para copiar una carpeta

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

Los parámetros de la solicitud se indican a continuación:

| Nombre del parámetro   | Tipo   | Ubicación | Descripción |
|------------------------|--------|-----------|-------------|
| srcPath                | string | path      | Ruta de la carpeta de origen (por ejemplo, `/origen`). |
| destPath               | string | query     | Ruta de la carpeta de destino (por ejemplo, `/destino`). |
| srcStorageName         | string | query     | Nombre del almacenamiento de origen (opcional). |
| destStorageName        | string | query     | Nombre del almacenamiento de destino (opcional). |

**Respuestas HTTP**

| Código | Descripción                               |
|--------|-------------------------------------------|
| 200    | Carpeta copiada correctamente.            |
| 400    | Solicitud incorrecta: parámetros inválidos. |
| 401    | No autorizado: token JWT inválido o faltante. |
| 404    | Carpeta de origen no encontrada.          |
| 500    | Error interno del servidor.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) define una interfaz de programación públicamente accesible que permite interacciones REST directamente desde un navegador web.

### Ejemplo de copia de carpeta

{{< tabs tabTotal="2" tabID="21" tabName21="Solicitud" tabName22="Respuesta" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/carpetaorigen?destPath=carpetadestino" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Nota: La operación de copia crea una nueva carpeta con el mismo contenido que la carpeta de origen.*

## **Cómo mover una carpeta**

### Información de la API para mover una carpeta

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

Los parámetros de la solicitud se indican a continuación:

| Nombre del parámetro   | Tipo   | Ubicación | Descripción |
|------------------------|--------|-----------|-------------|
| srcPath                | string | path      | Ruta de la carpeta de origen (por ejemplo, `/carpeta`). |
| destPath               | string | query     | Ruta de la carpeta de destino (por ejemplo, `/destino`). |
| srcStorageName         | string | query     | Nombre del almacenamiento de origen (opcional). |
| destStorageName        | string | query     | Nombre del almacenamiento de destino (opcional). |

**Respuestas HTTP**

| Código | Descripción                               |
|--------|-------------------------------------------|
| 200    | Carpeta movida correctamente.             |
| 400    | Solicitud incorrecta: parámetros inválidos. |
| 401    | No autorizado: token JWT inválido o faltante. |
| 404    | Carpeta de origen no encontrada.          |
| 500    | Error interno del servidor.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) define una interfaz de programación públicamente accesible que permite interacciones REST directamente desde un navegador web.

### Ejemplo de movimiento de carpeta

{{< tabs tabTotal="2" tabID="23" tabName23="Solicitud" tabName24="Respuesta" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/move/carpeta1?destPath=carpeta2" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="24" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Nota: Al mover una carpeta se conserva su estructura interna y las versiones de sus archivos.*

## **Cómo comprobar si existe un almacenamiento**

### Información de la API para comprobar la existencia de un almacenamiento

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

Los parámetros de la solicitud se indican a continuación:

| Nombre del parámetro | Tipo   | Ubicación | Descripción |
|----------------------|--------|-----------|-------------|
| storageName          | string | path      | Nombre del almacenamiento que se va a comprobar. |

**Respuestas HTTP**

| Código | Descripción                               |
|--------|-------------------------------------------|
| 200    | Se devuelve la existencia del almacenamiento (`true` o `false`). |
| 401    | No autorizado: token JWT inválido o faltante. |
| 404    | Almacenamiento no encontrado.             |
| 500    | Error interno del servidor.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) define una interfaz de programación públicamente accesible que permite interacciones REST directamente desde un navegador web.

### Ejemplo de comprobación de existencia de almacenamiento

{{< tabs tabTotal="2" tabID="33" tabName33="Solicitud" tabName34="Respuesta" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/MiAlmacenamiento/exist" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo comprobar si existe un archivo o una carpeta**

### Información de la API para comprobar la existencia de un objeto

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

Los parámetros de la solicitud se indican a continuación:

| Nombre del parámetro | Tipo   | Ubicación | Descripción |
|----------------------|--------|-----------|-------------|
| path                 | string | path      | Ruta del archivo o carpeta (por ejemplo, `/archivo.xlsx` o `/carpeta`). |
| storageName          | string | query     | Nombre del almacenamiento que se va a comprobar. |
| versionId            | string | query     | Identificador de la versión del archivo (opcional). |

**Respuestas HTTP**

| Código | Descripción                               |
|--------|-------------------------------------------|
| 200    | Se devuelve la información de existencia. |
| 401    | No autorizado: token JWT inválido o faltante. |
| 404    | Archivo o carpeta no encontrados.         |
| 500    | Error interno del servidor.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) define una interfaz de programación públicamente accesible que permite interacciones REST directamente desde un navegador web.

### Ejemplo de comprobación de existencia de un objeto

{{< tabs tabTotal="2" tabID="37" tabName37="Solicitud" tabName38="Respuesta" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/exist/Libro1.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```json
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo obtener el uso del disco**

### Información de la API para obtener el uso del disco

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/disc
```

Los parámetros de la solicitud se indican a continuación:

| Nombre del parámetro | Tipo   | Ubicación | Descripción |
|----------------------|--------|-----------|-------------|
| storageName          | string | query     | Nombre del almacenamiento que se va a consultar. |

**Respuestas HTTP**

| Código | Descripción                               |
|--------|-------------------------------------------|
| 200    | Se devuelve la información de uso del disco. |
| 401    | No autorizado: token JWT inválido o faltante. |
| 500    | Error interno del servidor.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) define una interfaz de programación públicamente accesible que permite interacciones REST directamente desde un navegador web.

### Ejemplo de obtención del uso del disco

{{< tabs tabTotal="2" tabID="40" tabName40="Solicitud" tabName41="Respuesta" >}}
{{< tab tabNum="40" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/disc?storageName=MiAlmacenamiento" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 987654321
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo obtener las versiones de un archivo**

### Información de la API para obtener las versiones de un archivo

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

Los parámetros de la solicitud se indican a continuación:

| Nombre del parámetro | Tipo   | Ubicación | Descripción |
|----------------------|--------|-----------|-------------|
| path                 | string | path      | Ruta del archivo (por ejemplo, `/archivo.xlsx`). |
| storageName          | string | query     | Nombre del almacenamiento que se va a consultar. |

**Respuestas HTTP**

| Código | Descripción                               |
|--------|-------------------------------------------|
| 200    | Lista de versiones del archivo devuelta.  |
| 401    | No autorizado: token JWT inválido o faltante. |
| 404    | Archivo no encontrado.                    |
| 500    | Error interno del servidor.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) define una interfaz de programación públicamente accesible que permite interacciones REST directamente desde un navegador web.

### Ejemplo de obtención de versiones de un archivo

{{< tabs tabTotal="2" tabID="46" tabName46="Solicitud" tabName47="Respuesta" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/version/Informe.xlsx?storageName=MiAlmacenamiento" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="47" >}}

```json
{
  "Value": [
    {
      "Name": "Informe.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 102400,
      "Path": "/Informe.xlsx",
      "VersionId": "1",
      "IsLatest": true
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}