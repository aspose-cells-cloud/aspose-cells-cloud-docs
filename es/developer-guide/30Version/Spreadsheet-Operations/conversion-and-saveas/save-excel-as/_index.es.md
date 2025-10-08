---
title: Guardar como Excel
second_title: Documen
linktitle: Guardar un
type: docs
url: /es/save-an-excel-file-as-other-formats-files/
aliases: [/convert-excel-workbook-to-different-file-formats/, /saveas-other-formats/]
keywords: Save excel files as kinds of format files
description: Aspose.Cells Cloud REST API permite guardar archivos de Excel en diversos formatos. El SDK es compatible con diversos lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 30
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Guardar como Excel
---
Este REST API indica que el archivo Excel `save` tiene un formato de archivo diferente.

**Parámetro de ruta**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|nombre|cadena| El nombre del archivo.|

**Parámetro de consulta**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|nuevo nombre de archivo|cadena| nuevo nombre de archivo|
|esAutoAjustarFilas|cadena| Ajusta automáticamente todas las filas de este libro. El valor predeterminado es "falso".|
|esAutoAjustarColumnas|cadena| Ajusta automáticamente el ancho de las columnas en este libro. El valor predeterminado es "false".|
|carpeta|cadena|Carpeta del libro de trabajo original.|
|nombreDeAlmacenamiento|cadena| El nombre del almacenamiento donde se encuentra el archivo.|
|nombreAlmacenamientoExterno|cadena| El nombre de almacenamiento donde se encuentra el archivo guardado.|
|comprobarRestricción de Excel|bool| Si verificar la restricción del archivo Excel cuando el usuario modifica objetos relacionados con celdas.|
|región|cadena| La configuración regional del libro de trabajo.|
|Ajuste de ancho de página por hoja|bool| La página se ajusta al ancho de la hoja de cálculo.|
|Ajuste de altura de página por hoja|bool| La página se ajusta a la altura de la hoja de cálculo.|
|nombreHoja|cadena| Convertir la hoja de trabajo especificada.|
|índice de página|cadena| Convierte la página especificada de la hoja de trabajo, se requiere sheetName.|
|una página por hoja|bool| Al convertir al formato PDF, una página por hoja.|

**Parámetro del cuerpo de la solicitud**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|Opciones de guardado| Objeto|Opción Guardar: guardar en la segunda parte del contenido de varias partes.|

## RESTO API

|**API**|**Tipo**|**Descripción**|**Enlace de recursos**|
|:- |:- |:- |:- |
|/cells/{nombre}/guardar como|CORREO|Exportar libro de trabajo a formato|[Guardar como después del documento](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

 Puedes utilizar**cURL** Herramienta de línea de comandos para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" -H "accept: multipart/form-data" 

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
  "SaveResult": {
    "SourceDocument": {
      "Href": "test.xlsx",
      "Rel": null,
      "Title": null,
      "Type": null
    },
    "DestDocument": {
      "Href": "test.pdf",
      "Rel": null,
      "Title": null,
      "Type": null
    },
    "AdditionalItems": []
  },
  "Code": 200,
  "Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}
