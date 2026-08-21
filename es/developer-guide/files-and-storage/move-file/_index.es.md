---
title: "API de movimiento de archivos de Aspose.Cells Cloud – Interfaz para mover archivos rápidamente en la nube"
second_title: "Documento"
ArticleTitle: "Solución eficiente para la gestión de archivos de Excel en la nube – Interfaz para mover archivos rápidamente en la nube"
linktitle: "Mover archivo"
type: docs
url: /es/move-file/
keywords: "Aspose.Cells, API de movimiento de archivos, almacenamiento en la nube, API de Excel, gestión de archivos"
description: "Cómo mover archivos entre carpetas en el almacenamiento en la nube de Aspose.Cells mediante la API de movimiento de archivos v4.0: punto de conexión, parámetros, ejemplos y enlaces a SDK."
weight: 100
---

La API **moveFile** mueve un archivo de una ubicación a otra dentro del almacenamiento en la nube de Aspose.Cells. Le ayuda a organizar archivos y gestionar el almacenamiento de forma eficiente.

## **API de Excel: Mover archivo**

### API web

```bash
PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de solicitud de la API **moveFile**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                      |
|----------------------|--------|------------------------------------------|--------------------------------------------------|
| srcPath              | String | Ruta                                     | Ruta de origen del archivo que se va a mover.    |
| destPath             | String | Cadena de consulta                       | Ruta de destino donde se moverá el archivo.      |
| srcStorageName       | String | Cadena de consulta                       | Nombre del almacenamiento de origen, si aplica.  |
| destStorageName      | String | Cadena de consulta                       | Nombre del almacenamiento de destino, si aplica. |
| versionId            | String | Cadena de consulta                       | ID de versión del archivo, si aplica.            |

### **Respuesta**

Una solicitud correcta devuelve **HTTP 200 OK** con un cuerpo JSON vacío.

```json
{}
```

**Códigos de estado HTTP**

| Código HTTP | Estado HTTP           | Descripción                                                  |
|-------------|-----------------------|--------------------------------------------------------------|
| 200         | OK                    | La API web se llamó correctamente; la respuesta contiene detalles de la operación. |
| 400         | Solicitud incorrecta  | Parámetros ausentes o inválidos (p. ej., tipo de archivo no admitido). |
| 401         | No autorizado         | Token JWT inválido o ausente.                                 |
| 413         | Carga demasiado grande | El archivo subido excede el límite de tamaño.                |
| 500         | Error interno del servidor | Error inesperado del servidor.                               |

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/FileController/MoveFile) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}?destPath={destPath}" \
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