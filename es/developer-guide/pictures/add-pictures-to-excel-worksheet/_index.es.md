---
title: Agregar imagen en un archivo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Anuncio
type: docs
url: /es/pictures/add/
aliases: [/add-pictures-to-excel-worksheet/]
keywords: Add a picture in an Excel file
description: Aspose.Cells Cloud REST API admite agregar una imagen en un archivo Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift
weight: 20
---
Este REST API le indica a `add` una nueva imagen para una hoja de trabajo Excel.
 
## RESET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino|El nombre del libro.|
| hojaNombre| cadena| camino| El nombre de la hoja de trabajo.|
| imagen|| cuerpo| Objeto de imagen|
| fila superior izquierda| entero| consulta|0 |
| columna superior izquierda| entero| consulta|0 |
| fila inferior derecha| entero| consulta|0 |
| columnaderechainferior| entero| consulta|0 |
| ruta de imagen| cadena| consulta| La ruta de la imagen, si no se proporcionan los datos de la imagen, se inspecciona en el cuerpo de la solicitud.|
| carpeta| cadena| consulta| La carpeta del libro de trabajo.|
| NombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|
 
 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Pictures/PutWorksheetAddPicture) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet6/pictures?picturePath=aspose-cloud.png" \
-X PUT \
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
 
## Familia SDK de la nube
 
 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se ocupa de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor, echa un vistazo a la[repositorio GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de Cloud.
 
Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:
 
 
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Pictures-AddPicturesWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pictures-AddPicturesWorksheet-add-pictures-worksheet.java" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Pictures-PutWorksheetAddPicture-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Pictures-add_a_new_worksheet_picture-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPictureToExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Pictures-AddPicturesWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pictures-AddPicturesWorksheet-add-pictures-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Pictures-AddPicturesWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "be89628a850c5f05b81105a97db96bef" >}}

{{< /tab >}}

{{< /tabs >}}
