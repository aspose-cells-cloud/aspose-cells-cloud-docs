---
title: "API de Aspose.Cells Cloud para obtener versiones de archivos: recuperación rápida del historial de versiones de archivos"
second_title: "Documento"
ArticleTitle: "Gestión de Excel en la nube: Recuperación rápida del historial de versiones de archivos en Aspose.Cells Cloud"
linktitle: "Obtener versiones de archivos"
type: docs
url: /es/get-file-versions/
keywords: "API de Aspose Cells, versiones de archivos, control de versiones de hojas de cálculo, API de almacenamiento en la nube, REST, historial de archivos de Excel"
description: "Obtenga una lista completa del historial de versiones de cualquier archivo de Excel almacenado en Aspose.Cells Cloud. Admite selección de almacenamiento, autenticación y códigos de error detallados."
weight: 100
---

Recupere una lista completa de registros de versión para una hoja de cálculo específica almacenada en Aspose.Cells Cloud. Este punto de conexión permite a los desarrolladores rastrear cambios, auditar modificaciones e implementar flujos de trabajo de control de versiones directamente desde el almacenamiento en la nube.

La API **GetFileVersions** devuelve todos los registros de versión para una hoja de cálculo específica almacenada en Aspose.Cells Cloud. Le ayuda a mantener un historial completo de cambios para cada archivo.

## **API de Excel: obtener versiones de archivos**

### API web

```
GET https://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Seguridad y autenticación**

Las APIs de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Los parámetros de solicitud de la API **GetFileVersions** son

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                                   |
| -------------------- | ------ | --------- | ------------------------------------------------------------------------------------------------------------- |
| `path`               | String | Ruta      | **Obligatorio.** Ruta completa al archivo cuyas versiones se están recuperando.                               |
| `storageName`        | String | Consulta  | Opcional. Nombre del almacenamiento que contiene el archivo. Si se omite, se utiliza el almacenamiento predeterminado. |

### **Respuesta**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Contiene una lista de versiones de archivo para el documento especificado."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": ["Una colección de detalles de versión del archivo."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

En caso de éxito, la API devuelve **HTTP 200 OK** con una carga útil JSON que contiene el array `Value` de objetos de versión de archivo, como se muestra arriba.

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT no válido o faltante.                                   |
| 413    | Payload demasiado grande | El archivo cargado excede el límite de tamaño.                    |
| 500    | Error interno del servidor | Error inesperado del servidor.                                    |

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions) proporciona una interfaz de programación completa para ejecutar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/version/MyFolder/MyFile.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "VersionId": "1",
      "IsLatest": false,
      "ModifiedDate": "2024-01-15T12:34:56Z",
      "Size": 10240
    },
    {
      "VersionId": "2",
      "IsLatest": true,
      "ModifiedDate": "2024-03-01T08:22:10Z",
      "Size": 10300
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

El uso de un SDK simplifica el desarrollo al abstraer las complejidades de bajo nivel, permitiendo a los desarrolladores centrarse en las funcionalidades principales. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo interactuar con los servicios web de Aspose.Cells en varios lenguajes de programación:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{</tab>}}
{{< /tabs >}}