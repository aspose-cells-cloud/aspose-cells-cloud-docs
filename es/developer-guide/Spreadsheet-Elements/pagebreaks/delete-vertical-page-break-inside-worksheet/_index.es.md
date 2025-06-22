---
title: Eliminar salto de página vertical
second_title: Aspose.Cells Cloud Documen
linktitle: Eliminar salto de página vertical
type: docs
url: /es/page-breaks/delete-vertical-page-break/
aliases: [/delete-vertical-page-break-inside-worksheet/]
keywords: Delete a page break in an Excel worksheet
description: Aspose.Cells Cloud REST API permite eliminar un salto de página en una hoja de cálculo Excel. El SDK admite varios lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 60
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Eliminar salto de página vertical
---
Este REST API indica eliminar un salto de página `vertical`.

## RSET API

```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
 
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino||
| nombreHoja| cadena| camino||
| índice| entero| camino||
| carpeta| cadena| consulta||
| nombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
 
```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}
