---
title: "Buscar texto en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Buscar en la hoja de cálculo"
type: docs
url: /es/worksheets/find-text/
aliases: [  /es/find-text-in-a-worksheet/ ]
weight: 40
keywords: "Excel, Aspose.Cells Cloud, API REST, buscar texto, hoja de cálculo, hoja de cálculo, búsqueda"
description: "Utilice la API REST de Aspose.Cells Cloud para buscar texto en una hoja de cálculo de Excel. La API está disponible en múltiples SDK y lenguajes de programación."
---

Esta API REST busca texto en una hoja de cálculo de Excel.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/findText
```


### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.


### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción              |
| --------------------- | ------ | --------- | ------------------------ |
| name                  | string | path      | Nombre del documento.    |
| sheetName             | string | path      | Nombre de la hoja de cálculo. |
| text                  | string | query     | Texto a buscar.          |
| folder                | string | query     | Carpeta del documento.   |
| storageName           | string | query     | Nombre del almacenamiento. |

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

| Código | Significado              | Descripción                                                  |
|--------|--------------------------|--------------------------------------------------------------|
| 200    | OK                       | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta     | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado            | Token JWT inválido o faltante.                               |
| 413    | Payload demasiado grande  | El archivo cargado supera el límite de tamaño.              |
| 500    | Error interno del servidor | Error inesperado en el servidor.                             |
## Cómo utilizar la API PostWorksheetTextSearch con SDK

### Especificación de la API PostWorksheetTextSearch

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetTextSearch) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo llamar a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/findText?text=a" -H "accept: application/json"
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

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetTextSearch.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetTextSearch.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetTextSearch.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetTextSearch.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetTextSearch.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetTextSearch.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetTextSearch.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetTextSearch.go" >}}

{{< /tab >}}

{{< /tabs >}}