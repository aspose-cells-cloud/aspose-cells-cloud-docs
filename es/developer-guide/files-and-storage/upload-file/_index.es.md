---
title: "API de carga de archivos de Aspose.Cells Cloud: Una interfaz para cargar archivos rápidamente en la nube"
second_title: "Documento"
ArticleTitle: "API de carga de archivos de Aspose.Cells Cloud: Una interfaz para cargar archivos rápidamente en la nube"
linktitle: "Cargar archivo"
type: docs
url: /es/upload-file/
keywords: "Aspose.Cells, carga de archivos, API de Excel, almacenamiento en la nube, API REST"
description: "Guía para cargar archivos con la API de Aspose.Cells Cloud, que cubre parámetros de solicitud, códigos de estado HTTP, manejo de errores y ejemplos de código."
weight: 100
---

La **API uploadFile** permite a los desarrolladores cargar archivos directamente en el almacenamiento en la nube para su procesamiento con Aspose Cells.

## **API de Aspose Cells: Cargar archivo**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Seguridad y autenticación**

Las APIs de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Los parámetros de solicitud de la API **uploadFile** son

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                    |
| :------------------- | :----- | :-------------------------------------- | :--------------------------------------------------------------------------------------------- |
| UploadFiles          | Archivo | FormData                                | Carga archivos en el almacenamiento en la nube.                                               |
| path                 | Cadena | Ruta                                    | Ruta de destino en el almacenamiento en la nube. Especifique la ruta donde se debe cargar el archivo. |
| storageName          | Cadena | Consulta                                | Nombre del almacenamiento en el que se cargará el archivo.                                    |

### **Respuesta**

```json
{
  "Name": "FilesUploadResult",
  "Description": ["Resultado de la carga de archivos"],
  "Type": "Clase",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": ["Lista de nombres de archivos cargados"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Contenedor",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": ["Lista de errores."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Contenedor",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Clase",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

La API devuelve los siguientes códigos de estado HTTP:

| Código de estado              | Descripción                                         |
| ----------------------------- | --------------------------------------------------- |
| **200 OK**                    | Archivo cargado correctamente.                     |
| **400 Bad Request**           | Parámetros inválidos o solicitud mal formada.      |
| **401 Unauthorized**          | Token de autenticación ausente o inválido.          |
| **403 Forbidden**             | Permisos insuficientes para el almacenamiento especificado. |
| **500 Internal Server Error** | Error inesperado en el servidor.                   |

## ¿Cómo usar la API de carga de archivos con SDK?

### Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/FileController/UploadFile) proporciona una descripción detallada de la API, lo que permite a los desarrolladores interactuar con ella directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/Folder/Book1.xlsx" \
  -H "Authorization: Bearer {access_token}" \
  -F "UploadFiles=@/path/to/Book1.xlsx" \
  -F "path=Folder/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Uploaded": ["Book1.xlsx"],
  "Errors": []
}
```

{{< /tab >}}

{{< /tabs >}}

### Uso de los SDK de Aspose.Cells Cloud

El uso de un SDK mejora la eficiencia del desarrollo al gestionar detalles de bajo nivel, permitiendo a los desarrolladores centrarse en las tareas del proyecto. Visite el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo llamar a los servicios web de Aspose.Cells mediante varios SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{</tab>}}
{{< /tabs >}}

**Consulte también**

- [API de descarga de archivos](/download-file/) – Recuperar un archivo del almacenamiento en la nube.
- [API de copia de archivos](/copy-file/) – Duplicar un archivo dentro del almacenamiento en la nube.
- [API de eliminación de archivos](/delete-file/) – Eliminar un archivo del almacenamiento en la nube.

---