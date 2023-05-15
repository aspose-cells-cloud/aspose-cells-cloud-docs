---
title: Desproteger un libro de trabajo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: desproteger
type: docs
url: /es/workbook/unprotect/
aliases: [/unprotect-excel-workbooks/]
keywords: REST API, spreadsheets, excel, merg
description: "Cells. Cloud API para Excel operar: proteger un libro de trabajo Excel"
weight: 60
---
Este REST API desprotege un Excel `workbook`.

**Parámetro de consulta**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|carpeta|cadena|Carpeta original del libro de trabajo.|
|NombreDeAlmacenamiento|cadena|Nombre de almacenamiento.|

**Parámetro del cuerpo de la solicitud**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|proteccion|WorkbookProtectionRequest||

**WorkbookProtectionRequest**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|Tipo de protección|cadena|TODO/CONTENIDO/NINGUNO/OBJETOS/ESCENARIOS/ESTRUCTURA/VENTANAS|
|Contraseña|cadena||


## DESCANSO API

|**API**|**Tipo**|**Descripción**|**Enlace arrogante**|
|:- |:- |:- |:- |
|/celdas/{nombre}/protección|BORRAR|Desproteger un documento|[EliminarDesprotegerDocumento](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectDocument)|

 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectDocument) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

 Puedes usar**cURL** herramienta de línea de comandos para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo hacer llamadas a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection" -H "accept: application/json"  -H "Content-Type: application/json" -d "{ \"ProtectionType\": \"all\", \"Password\": \"aspose\"}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code":"200",

  "Status":"OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Familia SDK de la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se ocupa de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor, echa un vistazo a la[repositorio GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de Cloud.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Java" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookDeleteUnProtectDocument.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-DeleteUnProtectDocument-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Document-unprotect_document-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-UnprotectWorkbook-unprotect-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnProtectExcelWorkbooks.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-UnprotectWorkbook-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-UnprotectWorkbook-unprotect-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-UnprotectWorkbook-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e70e326db37cfb9a80aadf9d795687c5" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "a856eb7506ccc320def87e055b177ca5" >}}

{{< /tab >}}

{{< /tabs >}}
