---
title: Convertir un archivo Excel a un formato diferente
second_title: Aspose.Cells Cloud Documen
linktitle: Convertir Excel
type: docs
url: /es/convert-an-excel-file-to-different-formats/
aliases: [/convert-excel-workbook-to-different-file-formats/,/convert/excel-to-different-formats/]
keywords: Convert excel files to kinds of format files
description: Aspose.Cells Cloud REST API admite la conversión de archivos de Excel a diversos formatos. El SDK es compatible con diversos lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 10
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, Convertir Excel
---
Este REST API indica que el archivo de Excel `convert` es un archivo de formato diferente.

La solicitud es una solicitud HTTP con contenido de varias partes (ver[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)o[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del contenido multiparte contiene el archivo de datos y la segunda contiene opciones de guardado.

**Parámetro de consulta**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|formato|cadena|El formato de archivo: csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, SVG, etc.|
|contraseña|cadena| La contraseña necesaria para abrir un archivo Excel.|
|Ruta de salida|cadena| Ruta para guardar el resultado. Si se trata de un solo archivo, el código `outPath` debe incluir tanto el nombre del archivo como la extensión. Si se trata de varios archivos, el código `outPath` solo debe incluir la carpeta.|
|nombreDeAlmacenamiento|cadena| El nombre de almacenamiento donde se encuentra el archivo.|
|comprobarRestricciónExcel|bool| Si verificar la restricción del archivo Excel cuando el usuario modifica objetos relacionados con celdas.|
|formato de flujo|cadena| El formato del flujo de archivo de entrada.|
|región|cadena| La configuración regional del libro de trabajo.|
|Ajuste de ancho de página por hoja|bool| La página se ajusta al ancho de la hoja de cálculo.|
|Ajuste de altura de página por hoja|bool| La página se ajusta a la altura de la hoja de trabajo.|
|nombreHoja|cadena| Convertir la hoja de trabajo especificada.|
|índice de página|cadena| Convierte la página especificada de la hoja de trabajo, se requiere sheetName.|
|una página por hoja|bool| Al convertir al formato PDF, una página por hoja.|
|Ajuste automático de filas|bool| Ajusta automáticamente todas las filas de este libro.|
|Ajuste automático de columnas|bool| Ajusta automáticamente el ancho de las columnas en este libro.|

**Parámetro del cuerpo de la solicitud**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|archivo de datos| archivo de datos|El archivo de datos se guarda en la primera parte del contenido multiparte.|
|Opciones de guardado| Objeto|Opción Guardar: guardar en la segunda parte del contenido de varias partes.|

## RESTO API

|**API**|**Tipo**|**Descripción**|**Enlace Swagger**|
|:- |:- |:- |:- |
|/células/convertir|PONER|Convierte el libro de trabajo del contenido de la solicitud a algún formato|[PonerConvertirLibroDeTrabajo](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

 Puedes utilizar**cURL** Herramienta de línea de comandos para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
