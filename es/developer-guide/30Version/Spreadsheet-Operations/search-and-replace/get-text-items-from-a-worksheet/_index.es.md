---
title: "Obtener elementos de texto de una hoja de cálculo de Excel"
second_title: "Document"
linktitle: "Obtener elementos de texto en la hoja de cálculo"
type: docs
url: /worksheets/get-text-items/
aliases: [/get-text-items-from-a-worksheet/]
weight: 20
keywords: "Aspose.Cells, API en la nube, Excel, hoja de cálculo, elementos de texto, REST"
description: "Recuperar todos los elementos de texto de una hoja de cálculo específica en un archivo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye códigos de ejemplo para cURL y SDK, pasos de autenticación y esquema de respuesta."
ArticleTitle: "Obtener elementos de texto de una hoja de cálculo de Excel"
---

## API REST

Esta API REST lee los elementos de texto de una hoja de cálculo en un archivo de Excel.

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{worksheet}/textItems
```

### Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parámetros de solicitud


| Nombre del parámetro | Tipo   | Ubicación | Obligatorio | Descripción                                             |
| ---------------------| ------ | --------- | ----------- | ------------------------------------------------------- |
| name                 | string | path      | Sí          | Nombre del archivo del libro de trabajo.               |
| sheetName            | string | path      | Sí          | Nombre de la hoja de cálculo.                          |
| folder               | string | query     | No          | Ruta a la carpeta que contiene el libro de trabajo.    |
| storageName          | string | query     | No          | Nombre del almacenamiento de Aspose Cloud.             |

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

| Código | Significado                  | Descripción                                                  |
|--------|------------------------------|--------------------------------------------------------------|
| 200    | Correcto (OK)                | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta (Bad Request) | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado (Unauthorized) | Token JWT inválido o ausente.                                |
| 413    | Carga útil demasiado grande (Payload Too Large) | El archivo cargado excede el límite de tamaño.             |
| 500    | Error interno del servidor (Internal Server Error) | Error inesperado en el servidor.                            |

## Cómo usar la API GetWorksheetTextItems con SDKs

### Especificación de la API GetWorksheetTextItems

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetTextItems){:target="_blank" rel="noopener noreferrer"} define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/sheet1/textItems" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
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

### Utilizar los SDK de Aspose.Cells Cloud

Los SDK simplifican la integración al gestionar los detalles de bajo nivel y permitirle centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}