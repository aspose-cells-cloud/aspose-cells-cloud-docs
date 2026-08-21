---
title: "Obtener información de filas de una hoja de cálculo de Excel"
second_title: "Documentos"
linktype: "filas"
type: docs
url: /rows/get/rows/
aliases: [/get-row-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, API para obtener filas, filas de hojas de cálculo de Excel, API REST, ejemplo en cURL, ejemplos de SDK, .NET, Java, Python"
description: "Aprenda cómo recuperar la información de filas de una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye el punto de conexión, parámetros, autenticación, ejemplos en cURL y de SDK para C#, Java, Python y más."
weight: 10
ArticleTitle: "Obtener información de filas de una hoja de cálculo de Excel – Documentación de la API de Aspose.Cells Cloud"
---

Esta API REST recupera la información de filas de una hoja de cálculo de Excel.

**Requisitos previos**  
Para llamar a este punto de conexión, debe proporcionar un token JWT válido en el encabezado `Authorization`. El token debe obtenerse mediante el flujo de autenticación de Aspose.Cloud y debe incluir los ámbitos necesarios para operaciones con celdas. La API sigue el esquema de versionado v3.0 y está sujeta a las políticas estándar de limitación de tasa.

## API GetWorksheetRows

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                   |
| --------------------- | ------ | --------- | ----------------------------- |
| name                  | string | path      | El nombre del libro.          |
| sheetName             | string | path      | El nombre de la hoja de cálculo. |
| folder                | string | query     | La carpeta del libro.         |
| storageName           | string | query     | El nombre del almacenamiento. |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRows) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Rows": {
    "MaxRow": 20,
    "RowsCount": 17,
    "RowsList": [
      { "link": { "Href": "/0", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/1", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/2", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/3", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/4", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/5", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/6", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/7", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/8", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/9", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/10", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/11", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/12", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/13", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/14", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/15", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/16", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/17", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/18", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/19", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/20", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/21", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/22", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/23", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/24", "Rel": "self", "Title": null, "Type": null } }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/rows",
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

**Códigos de respuesta**

| Código | Significado                  | Descripción                                                                 |
|--------|------------------------------|-----------------------------------------------------------------------------|
| 200    | OK                           | La solicitud se realizó correctamente y se devuelve la información de filas. |
| 400    | Solicitud incorrecta         | La solicitud está mal formada (por ejemplo, faltan parámetros obligatorios). |
| 401    | No autorizado                | Token JWT inválido o ausente.                                               |
| 404    | No encontrado                | El libro o la hoja de cálculo especificados no existen.                     |
| 500    | Error interno del servidor   | Se produjo un error inesperado en el servidor.                              |

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```java
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Rows": {
    "MaxRow": 20,
    "RowsCount": 17,
    "RowsList": [
      { "link": { "Href": "/0", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/1", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/2", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/3", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/4", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/5", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/6", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/7", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/8", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/9", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/10", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/11", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/12", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/13", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/14", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/15", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/16", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/17", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/18", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/19", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/20", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/21", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/22", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/23", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/24", "Rel": "self", "Title": null, "Type": null } }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/rows",
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

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que pueda centrarse en las tareas de su proyecto. A continuación se presentan ejemplos de código específicos por lenguaje para recuperar filas de hojas de cálculo.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}