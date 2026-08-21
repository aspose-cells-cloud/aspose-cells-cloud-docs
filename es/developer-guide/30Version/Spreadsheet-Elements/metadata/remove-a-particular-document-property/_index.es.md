---
title: "Eliminar una propiedad específica de un documento"
second_title: "Documento"
linktitle: "Eliminar"
type: docs
url: /es/document-properties/delete/
aliases: [  /es/remove-a-particular-document-property/ ]
keywords: "Aspose.Cells, eliminar propiedad de documento, API de metadatos de Excel, REST, SDK en la nube, ejemplo de cURL"
description: "Eliminar una propiedad específica de un documento de un libro de Excel utilizando la API REST de Aspose.Cells Cloud v3.0. Incluye ejemplos de cURL y SDK para C#, Java, Python y más."
weight: 50
---

Esta API REST elimina una propiedad de documento de un libro de trabajo.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio | Descripción                                      |
| -------------------- | ------ | --------- | ----------- | ------------------------------------------------ |
| name                 | string | path      | Sí          | El nombre del libro de Excel.                    |
| propertyName         | string | path      | Sí          | El nombre de la propiedad de documento a eliminar. |
| folder               | string | query     | No          | La ruta de la carpeta donde se almacena el libro. |
| storageName          | string | query     | No          | El nombre del servicio de almacenamiento.        |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperty) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
     -X DELETE \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Respuestas de error

| Estado HTTP | Descripción                                                        | Ejemplo JSON                                                |
| ----------- | ------------------------------------------------------------------ | ----------------------------------------------------------- |
| 400         | Solicitud incorrecta: faltan parámetros obligatorios o valores no válidos. | `{"Code":400,"Message":"Missing required parameter 'name'."}` |
| 401         | No autorizado: token JWT inválido o ausente.                       | `{"Code":401,"Message":"Invalid access token."}`           |
| 404         | No encontrado: el libro o la propiedad especificada no existe.   | `{"Code":404,"Message":"Document property not found."}`    |
| 500         | Error interno del servidor: se produjo una condición inesperada. | `{"Code":500,"Message":"An unexpected error has occurred."}` |

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}