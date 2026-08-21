---
title: "Obtener todas las propiedades del documento"
second_title: "Documento"
linktitle: "Obtener todas"
type: docs
url: /es/document-properties/get-all/
aliases: [  /es/get-all-document-properties/ ]
keywords: "Obtener todas las propiedades del documento, Aspose.Cells Cloud, propiedades de documentos de Excel, API REST, SDK, metadatos de Excel"
description: "Recuperar todas las propiedades del documento desde un archivo de Excel usando la API REST de Aspose.Cells Cloud. El punto de conexión funciona con todos los SDK y lenguajes de programación admitidos."
ArticleTitle: "Obtener todas las propiedades del documento – Aspose.Cells Cloud API"
weight: 25
---

Esta API REST lee las propiedades del documento.

## API GetDocumentProperties

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                         |
| --------------------- | ------ | --------- | ----------------------------------- |
| name                  | string | path      | Nombre del archivo de Excel.        |
| folder                | string | query     | Carpeta que contiene el archivo.    |
| storageName           | string | query     | Nombre del servicio de almacenamiento. |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperties) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo invocar la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperties": {
    "DocumentPropertyList": [
      {
        "Name": "Title",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Title",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Subject",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Subject",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Author",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Author",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Keywords",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Keywords",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Comments",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Comments",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "LastSavedBy",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/LastSavedBy",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "CreateTime",
        "Value": "6/5/2015 6:17:20 PM",
        "BuiltIn": "True",
        "link": {
          "Href": "/CreateTime",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "LastSavedTime",
        "Value": "9/27/2019 9:09:43 PM",
        "BuiltIn": "True",
        "link": {
          "Href": "/LastSavedTime",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Category",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Category",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "NameOfApplication",
        "Value": "Microsoft Excel",
        "BuiltIn": "True",
        "link": {
          "Href": "/NameOfApplication",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Version",
        "Value": "16.0300",
        "BuiltIn": "True",
        "link": {
          "Href": "/Version",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Security",
        "Value": "0",
        "BuiltIn": "True",
        "link": {
          "Href": "/Security",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "ScaleCrop",
        "Value": "False",
        "BuiltIn": "True",
        "link": {
          "Href": "/ScaleCrop",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Template",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Template",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Manager",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Manager",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Company",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Company",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "LinksUpToDate",
        "Value": "False",
        "BuiltIn": "True",
        "link": {
          "Href": "/LinksUpToDate",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/documentproperties",
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

**Códigos de estado HTTP**

| Código | Significado                | Descripción                                                  |
|--------|----------------------------|--------------------------------------------------------------|
| 200    | Correcto                   | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta       | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado              | Token JWT inválido o faltante.                               |
| 413    | Payload demasiado grande   | El archivo cargado supera el límite de tamaño.              |
| 500    | Error interno del servidor | Error inesperado en el servidor.                             |

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperties.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperties.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperties.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperties.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperties.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperties.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperties.go" >}}

{{< /tab >}}

{{< /tabs >}}