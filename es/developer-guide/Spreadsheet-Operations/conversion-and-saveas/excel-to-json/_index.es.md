---
title: Excel a Jso
second_title: Aspose.Cells Cloud Documen
linktitle: Excel a Jso
type: docs
url: /es/convert-excel-file-to-json-file/
keywords: Convert excel files to json files
description: Aspose.Cells Cloud REST API admite la conversión de archivos de Excel a archivos JSON. El SDK es compatible con varios lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Excel a Json
---
Este REST API indica a `convert` un archivo de hoja de cálculo a un archivo de formato json.

**Parámetro de consulta**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|contraseña|cadena| La contraseña necesaria para abrir un archivo Excel.|
|nombreDeAlmacenamiento|cadena| El nombre de almacenamiento donde se encuentra el archivo.|
|comprobarRestricciónExcel|bool| Si verificar la restricción del archivo Excel cuando el usuario modifica objetos relacionados con celdas.|

**Parámetro del cuerpo de la solicitud**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|archivo de datos| archivo de datos|El archivo de datos se guarda en la primera parte del contenido multiparte.|

**Respuesta**

[Información del archivo](/cells/es/file-info/)

## Especificación REST API

|**API**|**Tipo**|**Descripción**|**Enlace Swagger**|
|:- |:- |:- |:- |
|/celdas/convertir/json|CORREO|Convierte una hoja de cálculo en un archivo pptx.|[Conversión posterior del libro de trabajo a JSON](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson)|

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

 Puedes utilizar**cURL** Herramienta de línea de comandos para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "xxxxxx.json",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToJson.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToJson.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToJson.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToJson.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToJson.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToJson.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToJson.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToJson.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Otras API implementan esta función

[POST /cells/{nombre}/guardar como](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API le permite guardar el archivo MS Excel como archivo HTML con configuraciones adicionales y guardar el resultado en el almacenamiento.

Este archivo de Excel REST API `convert` a HTML.

[PUT /células/convertir](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API le permite convertir el archivo MS Excel al archivo HTML con configuraciones adicionales y guardar el resultado en la respuesta.

Este archivo de Excel REST API `export` a HTML.

[OBTENER /células/{nombre}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API le permite convertir el archivo MS Excel al archivo HTML con configuraciones adicionales y guardar el resultado en la respuesta.
