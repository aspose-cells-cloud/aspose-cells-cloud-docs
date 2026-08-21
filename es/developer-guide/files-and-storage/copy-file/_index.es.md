---
title: "API de copia de archivos de Aspose.Cells Cloud: una interfaz para copiar y realizar operaciones por lotes de archivos de Excel en la nube"
second_title: "Documento"
ArticleTitle: "Solución de gestión de archivos de Excel basada en la nube – Explicación detallada de la funcionalidad de copia por lotes de la API Copy File de Aspose.Cells"
linktitle: "Copiar archivo"
type: docs
url: /copy-file/
keywords: "Aspose.Cells, API CopyFile, copia de archivo de Excel, almacenamiento en la nube, API REST"
description: "Aprenda a utilizar la API CopyFile de Aspose.Cells Cloud para duplicar archivos de Excel de forma eficiente y gestionarlos entre distintas ubicaciones de almacenamiento."
weight: 100
---

La **API copyFile** permite a los usuarios duplicar un archivo de Excel desde una ruta de origen especificada hasta una ruta de destino, admitiendo diversas opciones de almacenamiento.

## **API de Excel: Copiar archivo**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud de la **API copyFile**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                              |
| --------------------- | ------ | --------------------------------------- | -------------------------------------------------------- |
| srcPath               | String | Ruta                                    | Ruta de origen del archivo que se va a copiar.          |
| destPath              | String | Cadena de consulta                      | Ruta de destino donde se guardará el archivo.           |
| srcStorageName        | String | Cadena de consulta                      | Nombre del almacenamiento de origen.                    |
| destStorageName       | String | Cadena de consulta                      | Nombre del almacenamiento de destino.                   |
| versionId             | String | Cadena de consulta                      | ID opcional de la versión del archivo que se va a copiar. |

### **Respuesta**

La operación no devuelve contenido si se completa correctamente. Los códigos de estado HTTP típicos son:

**Códigos de estado HTTP**

| Código | Significado            | Descripción                                                      |
| ------ | ---------------------- | ---------------------------------------------------------------- |
| 200    | Correcto (OK)          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta (Bad Request) | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado (Unauthorized)      | Token JWT no válido o ausente.                                   |
| 413    | Carga demasiado grande (Payload Too Large) | El archivo cargado excede el límite de tamaño.                 |
| 500    | Error interno del servidor (Internal Server Error) | Error inesperado en el servidor.                               |

## ¿Cómo utilizar la API de copia de archivos con los SDK?

### Especificación de la API de copia de archivos

La [Especificación de la API de copia de archivos](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile) proporciona una interfaz de programación pública accesible para realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
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

Utilizar un SDK es la forma más rápida de desarrollar, ya que oculta los detalles de bajo nivel, lo que le permite convertir datos de tablas de hojas de cálculo en imágenes con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

---