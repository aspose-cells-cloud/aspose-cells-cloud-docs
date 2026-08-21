---
title: "Aspose.Cells Cloud – API para eliminar archivos"
second_title: "Documento"
ArticleTitle: "Aspose.Cells Cloud – API para eliminar archivos"
linktitle: "Eliminar archivo"
type: docs
url: /es/delete-file/
keywords: "Aspose Cells, API para eliminar archivos, almacenamiento en la nube de Excel, API REST, gestión de archivos"
description: "Elimine un archivo de Excel del almacenamiento en la nube de Aspose.Cells mediante la API REST para eliminar archivos. Incluye el punto de conexión, parámetros, autenticación y código de ejemplo."
weight: 100
---

La API **deleteFile** elimina el archivo especificado del almacenamiento en la nube, ayudándole a gestionar eficientemente sus recursos y datos.

## **API de Excel: Eliminar archivo**

### API web

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                      |
| :------------------- | :----- | :-------- | :----------------------------------------------------------------------------------------------- |
| `path`               | string | Ruta      | Ruta codificada en URL del archivo que se debe eliminar.                                        |
| `storageName`        | string | Consulta  | Nombre del almacenamiento donde reside el archivo. Omitir si se usa el almacenamiento predeterminado. |
| `versionId`          | string | Consulta  | Identificador de una versión específica del archivo que se va a eliminar. Si se omite, se elimina la versión más reciente. |

### Descripción de la respuesta

Una solicitud correcta devuelve **HTTP 200** con un cuerpo de respuesta vacío. No se devuelve ninguna carga útil JSON.

```json
{}
```

**Códigos de estado HTTP**

| Código | Significado            | Descripción                                                    |
| ------ | ---------------------- | -------------------------------------------------------------- |
| 200    | Correcto               | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta   | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado          | Token JWT inválido o ausente.                                   |
| 413    | Carga útil demasiado grande | El archivo subido supera el límite de tamaño.                 |
| 500    | Error interno del servidor | Error inesperado en el servidor.                               |

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer SU_TOKEN_DE_ACCESO" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK.