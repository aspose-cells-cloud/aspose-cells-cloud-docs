---
title: "Obtener elementos de texto de un libro de Excel"
ArticleTitle: "Obtener elementos de texto de un libro de Excel mediante la API de Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Obtener elementos de texto en el libro"
type: docs
url: /workbook/get-text-items/
aliases: [/get-text-items-from-a-workbook/]
weight: 10
keywords: "Excel, Aspose.Cells Cloud, REST API, hoja de cálculo, obtener elementos de texto, libro"
description: "Recuperar elementos de texto de un libro de Excel mediante la API REST de Aspose.Cells Cloud. Disponible a través de SDK para C#, Java, Python, PHP, Ruby, Go, Node.js, Perl y Swift."
---


## API REST

Esta API REST lee los **elementos de texto** de un libro en un archivo de Excel.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/textItems
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.


### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                             |
|----------------------|--------|-----------|---------------------------------------------------------|
| name                 | string | path      | El nombre del archivo del libro.                        |
| folder               | string | query     | La ruta de la carpeta en el almacenamiento donde reside el libro. |
| storageName          | string | query     | El nombre del servicio de almacenamiento.               |

### **Respuesta**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**Códigos de estado HTTP**

| Código | Significado                   | Descripción                                              |
|--------|-------------------------------|----------------------------------------------------------|
| 200    | Correcto                      | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta          | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado                 | Token JWT no válido o ausente.                           |
| 413    | Payload demasiado grande       | El archivo cargado excede el límite de tamaño.          |
| 500    | Error interno del servidor    | Error inesperado en el servidor.                         |

## Cómo utilizar la API GetWorkbookTextItems con SDK

### Especificación de la API GetWorkbookTextItems

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookTextItems) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/textItems" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

Códigos de respuesta HTTP típicos:

| Código | Descripción                                      |
|--------|--------------------------------------------------|
| 200    | Solicitud correcta; se devuelven los elementos de texto. |
| 401    | No autorizado: token ausente o no válido.        |
| 403    | Prohibido: permisos insuficientes.               |
| 404    | No encontrado: libro o recurso no encontrado.    |
| 500    | Error interno del servidor: fallo inesperado.    |

### Utilizar los SDK de Aspose.Cells Cloud

Este ejemplo utiliza la versión de la API **v3.0**; consulte el registro de cambios para versiones más recientes. Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}
---