---
title: Anuncio
type: docs
url: /es/comments/add/
aliases: [/add-a-comment-to-a-cell-in-a-worksheet/]
keywords: REST API, spreadsheets, excel, add commen
description: "Cells.Cloud API para Excel operar: agregar comentario"
weight: 20
---
Este REST API indica Agregar comentario de celda de la hoja de trabajo.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino| El nombre del documento.|
| nombre de la hoja| cadena| camino| El nombre de la hoja de trabajo.|
| nombre de celda| cadena| camino| El nombre de la celda|
| comentario|| cuerpo| Objeto de comentario|
| carpeta| cadena| consulta| La carpeta de documentos.|
| nombredealmacenamiento| cadena| consulta| nombre del almacenamiento.|
 
 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetComment) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{ \"CellName\": \"a1\", \"Author\": \"test\", \"HtmlNote\": \"string\", \"Note\": \"this is a comment\", \"AutoSize\": true, \"IsVisible\": true, \"Width\": 10, \"Height\": 10}"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{

  "Comment": {

    "CellName": "A1",

    "Author": "test",

    "HtmlNote": "<Font Style=\"FONT-WEIGHT: bold;FONT-FAMILY: Tahoma;FONT-SIZE: 9pt;COLOR: #000000;TEXT-ALIGN: left;\">this is a comment</Font>",

    "Note": "this is a comment",

    "AutoSize": true,

    "IsVisible": true,

    "Width": 10,

    "Height": 10,

    "TextHorizontalAlignment": "Left",

    "TextOrientationType": "NoRotation",

    "TextVerticalAlignment": "Top",

    "link": {

      "Href": "/test.xlsx/worksheets/Sheet1/comments/a1",

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
 
 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor revisa el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de nube.
 
Los siguientes ejemplos de código demuestran cómo realizar llamadas a servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "6e4a5c5c04cab925b7125b533afeba01" >}}

{{< /tab >}}

{{< /tabs >}}
