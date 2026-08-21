---
title: "Aspose.Cells Cloud API de movimiento de carpetas: Mueva rápidamente carpetas en la nube"
second_title: "Documentación"
ArticleTitle: "Gestión de archivos de Excel basada en la nube: Mueva rápidamente carpetas en la nube"
linktitle: "Mover carpeta"
type: docs
url: /es/move-folder/
keywords: "Aspose.Cells, Mover carpeta, Almacenamiento en la nube, API de Excel"
description: "Aprenda a mover carpetas en el almacenamiento en la nube de Aspose.Cells mediante la API RESTful de movimiento de carpetas. Incluye el endpoint, parámetros, ejemplo de cURL, códigos de error y ejemplos de SDK para C#, Java, Python y más."
weight: 100
---

Esta API mueve una carpeta de una ubicación a otra dentro del almacenamiento en la nube de Aspose.Cells. Ayuda a organizar archivos y gestionar eficientemente el almacenamiento en la nube.

## **API de Excel: Mover carpeta**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

**Ejemplo de solicitud cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
     -H "Authorization: Bearer {access_token}"
```

### **Seguridad y autenticación**

Las APIs de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud de la API **moveFolder**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                        |
| --------------------- | ------ | --------- | ------------------------------------------------------------------ |
| srcPath              | string | Path      | Ruta completa de la carpeta que se va a mover, por ejemplo, `FolderA/`. |
| destPath             | string | Query     | Ruta de destino donde se moverá la carpeta, por ejemplo, `FolderB/`.   |
| srcStorageName       | string | Query     | (Opcional) Nombre del almacenamiento de origen.                    |
| destStorageName      | string | Query     | (Opcional) Nombre del almacenamiento de destino.                   |

**Detalles de los parámetros**

- **srcPath** – obligatorio. Ruta de la carpeta de origen.
- **destPath** – obligatorio. Ruta de la carpeta de destino.
- **srcStorageName** – opcional. Identificador del almacenamiento de origen.
- **destStorageName** – opcional. Identificador del almacenamiento de destino.

### **Respuesta**

En caso de éxito, la API devuelve un cuerpo de respuesta vacío con el código de estado HTTP **200 OK**. Los errores se devuelven como objetos JSON que contienen un campo `error`.

**Códigos de estado HTTP**

| Código HTTP | Estado HTTP           | Descripción                                                       |
| ----------- | --------------------- | ----------------------------------------------------------------- |
| 200         | OK                    | La API web se llamó correctamente; la respuesta contiene detalles de la operación. |
| 400         | Solicitud incorrecta  | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401         | No autorizado         | Token JWT inválido o faltante.                                    |
| 413         | Payload demasiado grande | El archivo cargado excede el límite de tamaño.                  |
| 500         | Error interno del servidor | Error inesperado en el servidor.                                |

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK: