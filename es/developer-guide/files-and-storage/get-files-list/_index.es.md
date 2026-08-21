---
title: "Aspose.Cells Cloud API – Obtener lista de archivos (contenido de carpeta)"
description: "Recuperar una lista de archivos y subcarpetas desde una carpeta específica en el almacenamiento en la nube de Aspose.Cells."
keywords:
  - Aspose.Cells
  - API
  - Obtener lista de archivos
  - Almacenamiento en la nube
  - Excel
  - REST
type: docs
weight: 100
---

La operación **Obtener lista de archivos** devuelve la colección de archivos y subcarpetas almacenados en una carpeta específica del almacenamiento en la nube de Aspose.Cells.  
Es el punto de entrada principal para navegar por libros de Excel, archivos comprimidos y otros tipos de archivos compatibles almacenados en la nube.

## Aspose.Cells Cloud API – Obtener lista de archivos (contenido de carpeta)

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre            | Ubicación | Tipo    | Obligatorio | Descripción                                                                 |
| ----------------- | --------- | ------- | ----------- | --------------------------------------------------------------------------- |
| **path**          | Ruta      | string  | Sí          | Ruta de la carpeta en el almacenamiento en la nube.                        |
| **storageName**   | Consulta  | string  | No          | Nombre del almacenamiento que se utilizará. Si se omite, se usa el almacenamiento predeterminado. |
| **pageSize**      | Consulta  | integer | No          | Número máximo de elementos que devolver por página (predeterminado: 100).   |
| **pageNumber**    | Consulta  | integer | No          | Número de página que recuperar (comenzando en 1, predeterminado: 1).       |

- **Valor** – Matriz de objetos `StorageFile`. Cada objeto contiene:
  - `Name` – Nombre del archivo o carpeta.
  - `IsFolder` – `true` si la entrada es una carpeta.
  - `Size` – Tamaño en bytes (las carpetas informan `0`).
  - `ModifiedDate` – Marca de tiempo de la última modificación (ISO 8601).

### **Respuesta**

**Códigos de estado HTTP**

| Código HTTP | Estado HTTP           | Descripción                                                    |
| ----------- | --------------------- | -------------------------------------------------------------- |
| 200         | OK                    | La API web se llamó correctamente; la respuesta contiene los detalles de la operación. |
| 400         | Solicitud incorrecta  | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401         | No autorizado         | Token JWT inválido o ausente.                                   |
| 413         | Payload demasiado grande | El archivo cargado supera el límite de tamaño.              |
| 500         | Error interno del servidor | Error inesperado en el servidor.                             |
|             |                       |                                                                |

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/GetFilesList) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/{path}?storageName=MyStorage&pageSize=100&pageNumber=1" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "Size": 124578,
      "ModifiedDate": "2024-03-10T12:34:56Z"
    },
    {
      "Name": "Archives",
      "IsFolder": true,
      "Size": 0,
      "ModifiedDate": "2024-02-01T08:00:00Z"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Uso de SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

---