---
title: "Crear carpeta – Aspose.Cells Cloud API | Gestión de almacenamiento de Excel"
second_title: "Documento"
ArticleTitle: "Crear carpeta – Aspose.Cells Cloud API"
linktitle: "Crear carpeta"
type: docs
url: /es/create-folder/
keywords: "Aspose.Cells, Cloud API, Crear carpeta, Gestión de almacenamiento, Excel"
description: "Cree una nueva carpeta en el almacenamiento en la nube de Aspose.Cells Cloud mediante una solicitud PUT sencilla. Consulte el formato de solicitud, los parámetros, la respuesta y el manejo de errores."
weight: 100
---

La operación **createFolder** crea una nueva carpeta en la ubicación especificada dentro del almacenamiento en la nube utilizado por la API de Excel. Esta operación es fundamental para organizar archivos y mantener una jerarquía de directorios estructurada.

## **API de Excel: Crear carpeta**

### API web

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud de la API **createFolder**

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio | Valor predeterminado | Descripción                                                                 |
| --------------------- | ------ | --------- | ----------- | -------------------- | --------------------------------------------------------------------------- |
| `path`               | String | Ruta      | Sí          | –                    | La ruta de la carpeta que se va a crear (por ejemplo, `miCarpeta/subCarpeta`). |
| `storageName`        | String | Consulta  | No          | –                    | El nombre del almacenamiento que se va a utilizar. Si se omite, se aplica el almacenamiento predeterminado. |

### Descripción de la respuesta

```json
{}
```

La operación no devuelve contenido en caso de éxito. Los códigos de estado HTTP habituales son los siguientes:

**Códigos de estado HTTP**

| Código HTTP | Estado HTTP           | Descripción                                                                 |
| ----------- | --------------------- | --------------------------------------------------------------------------- |
| 200         | OK                    | La API web se llamó correctamente; la respuesta contiene detalles de la operación. |
| 400         | Petición incorrecta   | Faltan parámetros o son inválidos (por ejemplo, tipo de archivo no admitido). |
| 401         | No autorizado         | Token JWT inválido o ausente.                                               |
| 413         | Carga demasiado grande | El archivo subido excede el límite de tamaño.                               |
| 500         | Error interno del servidor | Error inesperado en el servidor.                                           |

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/myFolder/subFolder" \
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

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{</tab>}}
{{< /tabs >}}