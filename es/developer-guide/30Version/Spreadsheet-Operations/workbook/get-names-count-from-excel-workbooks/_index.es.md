---
title: "Obtener nombres de un libro de Excel"
second_title: "Documento"
linktitle: "Nombres"
type: docs
url: /get-names-from-an-excel-file/
aliases:
  [
    /get-names-count-from-excel-workbooks/,
    /workbook/names/,
    /workbook/get/names/,
  ]
keywords: "Aspose.Cells, Cloud, Excel, Libro de trabajo, Nombres, REST API, SDK"
description: "Recuperar todos los nombres definidos de un libro de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye orientación sobre autenticación, ejemplo de cURL, esquema de respuesta, manejo de errores y ejemplos de SDK."
weight: 120
ArticleTitle: "Obtener nombres de un libro de Excel – API de Aspose.Cells Cloud"
---

Esta API REST recupera los nombres definidos de un libro de Excel.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

## API GetWorkbookNames

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/names
```

Los parámetros de la solicitud son:

| Nombre del parámetro | Tipo   | Ubicación | Descripción                             |
| --------------------- | ------ | --------- | --------------------------------------- |
| name                  | string | path      | Nombre del archivo del libro de trabajo. |
| folder                | string | query     | Carpeta que contiene el libro de trabajo. |
| storageName           | string | query     | Nombre del almacenamiento a utilizar.    |

La solicitud debe incluir las siguientes cabeceras HTTP:

| Cabecera      | Tipo   | Descripción                                     |
|---------------|--------|-------------------------------------------------|
| Authorization | string | Token portador JWT (obligatorio)                |
| Accept        | string | `application/json`                              |
| Content-Type  | string | `application/json` (para solicitudes con cuerpo) |

**Autenticación** – La API requiere un token portador OAuth2/JWT. Obtenga un token en `https://api.aspose.cloud/connect/token` utilizando su client‑id y client‑secret, e incluya la cabecera `Authorization: Bearer <jwt token>` en cada solicitud.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookNames) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo llamar a la API de Aspose.Cells Cloud mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/names" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Names": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Count": 0,
    "NameList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        }
      }
    ]
  }
}
```

_Campos de la respuesta_

- **Status** _(string)_ – Mensaje de estado de la operación.
- **Names.link** _(object)_ – Información del hipervínculo para la colección.
- **Names.Count** _(integer)_ – Número total de nombres definidos devueltos.
- **Names.NameList** _(array)_ – Lista de objetos nombre; cada objeto contiene un objeto **link** con detalles de navegación.

**Manejo de errores** – El servicio puede devolver los siguientes códigos de estado HTTP:

| Código | Significado            | Acción recomendada                                             |
| ------ | ---------------------- | -------------------------------------------------------------- |
| 401    | No autorizado          | Verifique que se haya proporcionado un token JWT válido.       |
| 404    | No encontrado          | Compruebe que el nombre del libro de trabajo, la carpeta y el almacenamiento sean correctos. |
| 500    | Error interno del servidor | Inténtelo de nuevo más tarde o póngase en contacto con el soporte de Aspose si el problema persiste. |

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK gestiona los detalles de bajo nivel, permitiéndole centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookNames.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookNames.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookNames.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookNames.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookNames.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookNames.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookNames.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookNames.go" >}}

{{< /tab >}}

{{< /tabs >}}