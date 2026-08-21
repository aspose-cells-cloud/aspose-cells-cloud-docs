---
title: "API de Existencia de Objeto – Verificar la Presencia de Archivo/Carpeta en Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "API de Existencia de Objeto – Verificar la Presencia de Archivo o Carpeta en Aspose.Cells Cloud"
linktype: "docs"
url: /es/object-exists/
keywords: "Aspose.Cells, almacenamiento en la nube, existencia de objeto, existencia de archivo, existencia de carpeta, API"
description: "Utilice la API de Existencia de Objeto para verificar rápidamente si un archivo o carpeta existe en el almacenamiento en la nube de Aspose.Cells. Admite el nombre opcional del almacenamiento y el ID de versión, y funciona con objetos con versiones."
weight: 100
---

La **API de Existencia de Objeto** permite a los desarrolladores determinar si un archivo o carpeta específico está presente en el almacenamiento en la nube de Aspose.Cells. Devuelve un valor booleano simple que indica la existencia y si la ruta apunta a una carpeta.

## **API de Excel: Existencia de Objeto**

### API web

```http
GET https://api.aspose.cloud/v5.0/cells/storage/exist/{path}
```

_`{path}`_ es la ruta completa al archivo o carpeta en el almacenamiento.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio | Descripción                                                              |
|----------------------|--------|-----------|-------------|--------------------------------------------------------------------------|
| `path`               | string | Ruta      | Sí          | Ruta completa al archivo o carpeta.                                      |
| `storageName`        | string | Consulta  | No          | Nombre del almacenamiento; utiliza el almacenamiento principal si se omite. |
| `versionId`          | string | Consulta  | No          | Identificador específico de la versión del archivo (si la versionado está habilitado). |

**Códigos de estado HTTP**

| Código HTTP | Estado HTTP           | Descripción                                                      |
|-------------|-----------------------|------------------------------------------------------------------|
| 200         | OK                    | La API web se llamó correctamente; la respuesta contiene detalles de la operación. |
| 400         | Solicitud incorrecta  | Parámetros faltantes o no válidos (p. ej., tipo de archivo no admitido). |
| 401         | No autorizado         | Token JWT no válido o faltante.                                  |
| 413         | Payload demasiado grande | El archivo cargado excede el límite de tamaño.                 |
| 500         | Error interno del servidor | Error inesperado en el servidor.                              |

### **Respuesta**

Una llamada correcta devuelve una carga útil JSON con dos propiedades:

```json
{
  "Exists": true,
  "IsFolder": false
}
```

- **Exists** – `true` si el archivo o carpeta existe; de lo contrario, `false`.
- **IsFolder** – `true` cuando la ruta apunta a una carpeta; `false` para un archivo.

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/exist/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
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

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK. Si un Gist no se carga, se proporciona un ejemplo estático a continuación de cada pestaña.

---