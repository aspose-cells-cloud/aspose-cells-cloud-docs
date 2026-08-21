---
title: "Obtener una propiedad específica de un documento"
second_title: "Documento"
linktitle: "Obtener"
type: docs
url: /es/document-properties/get/
aliases: [  /es/get-a-particular-document-property/ ]
keywords: "Aspose.Cells, API en la nube, Obtener propiedad de documento, metadatos de Excel, REST GET, ejemplos de SDK"
description: "Recuperar una propiedad de documento con nombre (por ejemplo, Autor, Título) de un archivo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye ejemplo de cURL, fragmentos de SDK y esquema de respuesta."
weight: 20
---

Esta API REST lee una propiedad de documento por su nombre.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                      |
| -------------------- | ------ | --------- | ------------------------------------------------ |
| name                 | string | path      | El nombre del archivo de Excel.                  |
| propertyName         | string | path      | El nombre de la propiedad de documento a recuperar. |
| folder               | string | query     | La carpeta que contiene el archivo (opcional).   |
| storageName          | string | query     | El nombre del almacenamiento (opcional).         |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperty) define una interfaz de programación accesible públicamente y permite llevar a cabo interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperty": {
    "Name": "Author",
    "Value": "",
    "BuiltIn": "True",
    "link": {
      "Href": "/test.xlsx/documentproperties/Author",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Detalles de la respuesta

El objeto JSON devuelto por la API contiene los siguientes campos:

| Campo                           | Tipo    | Descripción                                                           |
| ------------------------------- | ------- | --------------------------------------------------------------------- |
| **DocumentProperty.Name**       | string  | El nombre de la propiedad (por ejemplo, `Author`).                   |
| **DocumentProperty.Value**      | string  | El valor de la propiedad. Puede estar vacío si no está establecido.  |
| **DocumentProperty.BuiltIn**    | boolean | Indica si la propiedad es una propiedad integrada de Excel.          |
| **DocumentProperty.link.Href**  | string  | URL relativa al recurso de la propiedad.                             |
| **DocumentProperty.link.Rel**   | string  | Tipo de relación, generalmente `self`.                               |
| **DocumentProperty.link.Title** | string  | Título legible (puede ser `null`).                                   |
| **DocumentProperty.link.Type**  | string  | Tipo MIME del recurso vinculado (puede ser `null`).                  |
| **Code**                        | integer | Código de estado HTTP devuelto por el servicio.                      |
| **Status**                      | string  | Descripción textual del estado (por ejemplo, `OK`).                  |

### Respuestas de error

| Estado HTTP | Código                 | Descripción                                         |
| ----------- | ---------------------- | --------------------------------------------------- |
| 400         | `InvalidParameter`     | Uno o más parámetros de la solicitud son inválidos. |
| 401         | `AuthenticationFailed` | Token JWT ausente o inválido.                       |
| 404         | `PropertyNotFound`     | La propiedad de documento especificada no existe.   |
| 500         | `InternalError`        | Se produjo un error inesperado en el servidor.      |

Un cuerpo de error típico tiene el siguiente aspecto:

```json
{
  "Code": 404,
  "Status": "Property not found"
}
```

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted se enfoque en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Terminología

| Término               | Definición                                                                                 |
| --------------------- | ------------------------------------------------------------------------------------------ |
| **Propiedad de documento** | Un fragmento de metadatos asociado a un libro de Excel (por ejemplo, Autor, Título, Creado). |
| **Metadatos**         | Término general para datos que describen otros datos; en este contexto se refiere a propiedades de documento. |
| **Propiedad personalizada** | Una propiedad definida por el usuario que no está incluida en el conjunto integrado.       |

### Preguntas frecuentes

**P:** _¿Cómo puedo recuperar la propiedad Autor de un archivo de Excel almacenado en Aspose Cloud?_  
**R:** Envíe una solicitud GET a `https://api.aspose.cloud/v3.0/cells/{nombrearchivo}/documentproperties/author` con un token Bearer válido. La respuesta JSON incluye `DocumentProperty.Name = "Author"` y su `Value`.

**P:** _¿Qué error devuelve la API si la propiedad solicitada no existe?_  
**R:** La API devuelve HTTP 404 con un cuerpo JSON que contiene `Code: 404` y `Status: "Property not found"`.

**P:** _¿Necesito especificar `storageName` cuando el archivo está en el almacenamiento predeterminado?_  
**R:** No. El parámetro de consulta `storageName` es opcional; omitálo para utilizar el almacenamiento predeterminado configurado para su cuenta.