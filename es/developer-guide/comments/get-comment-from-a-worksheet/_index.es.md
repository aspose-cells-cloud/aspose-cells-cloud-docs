---
title: ge
type: docs
url: /es/comments/get/
aliases: [/get-comment-from-a-worksheet/]
keywords: REST API, spreadsheets, excel, get commen
description: "Cells.Cloud API para Excel operar: obtener comentarios"
weight: 10
---
Este REST API indica Obtener comentario de hoja de trabajo por nombre de celda.
 
## RESET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino| El nombre del documento.|
| hojaNombre| cadena| camino| El nombre de la hoja de cálculo.|
| nombre de celda| cadena| camino| el nombre de la celda|
| carpeta| cadena| consulta| La carpeta de documentos.|
| NombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|
 
 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"


```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
    "Comment":{

    "CellName":"A1",

    "Author":"roy.wang",

    "HtmlNote": "",

    "Note": "Aspose.Cells Cloud.",

    "AutoSize": "True",

    "IsVisible": "True",

    "Width": 30,

    "Height": 10,

    "TextHorizontalAlignment": "Bottom",

    "TextOrientationType": "TopToBottom",

    "TextVerticalAlignment": "Bottom"

    },
 
   "Code": 200,

   "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Familia SDK de la nube
 
 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se ocupa de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor, echa un vistazo a la[repositorio GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de Cloud.
 
Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0f1e96858d650d16d9c09ca61723c335" >}}

{{< /tab >}}

{{< /tabs >}}
