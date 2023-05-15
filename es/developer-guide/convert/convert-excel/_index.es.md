---
title: Convertir Exce
second_title: Aspose.Cells Cloud Documen
linktitle: conversión
type: docs
url: /es/convert/excel-to-different-formats/
aliases: [/convert-excel-workbook-to-different-file-formats/]
keywords: Convert excel files to kinds of format files
description: Aspose.Cells Cloud REST API admite la conversión de archivos de Excel a tipos de archivos de formato. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift
weight: 10
---
Este REST API indica un archivo de Excel `convert` para un archivo de formato diferente.

La solicitud es una solicitud HTTP con contenido de varias partes (ver[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)o[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del contenido multiparte contiene el archivo de datos y la segunda contiene opciones para guardar.

**Parámetro de consulta**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|formato|cadena| formato de archivo (csv/xls/html/mhtml/ods/pdf/xml/txt/tiff/xlsb/xlsm/xlsx/xltm/xltx/xps/png/jpg/gif/emf/bmp/md/Numbers/wmf/svg )|


**Parámetro del cuerpo de la solicitud**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
|archivo de datos| archivo de datos|El archivo de datos se guarda en la primera parte del contenido de varias partes.|
|GuardarOpciones| Objeto|Guardar opción guardar en la segunda parte del contenido de varias partes.|


## DESCANSO API

|**API**|**Tipo**|**Descripción**|**Enlace arrogante**|
|:- |:- |:- |:- |
|/celdas/convertir|PONER|Convierte el libro de trabajo del contenido de la solicitud a algún formato|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|


 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

 Puedes usar**cURL** herramienta de línea de comandos para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo hacer llamadas a Cloud API con cURL.


{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

{{< /tab >}}

{{< /tabs >}}

## Familia SDK de la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se ocupa de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor, echa un vistazo a la[repositorio GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de Cloud.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:



{{< tabs tabTotal="3" tabID="3" tabName1="C#" tabName2="Java" tabName3="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/

Aspose.Cells.Cloud.SDK.Api.CellsApi cellsApi = new CellsApi("your client id", "your client secret");
var response = cellsApi.CellsWorkbookPutConvertWorkbook( File.OpenRead(@".\TestData\datasource.xlsx"), "pdf", null, null);
Assert.IsInstanceOf<System.IO.Stream>(response, "response is System.IO.Stream");

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/
try{
    CellsApi api = new CellsApi(System.getenv("CellsCloudTestClientId"),System.getenv("CellsCloudTestClientSecret"));
    File response = api.cellsWorkbookPutConvertWorkbook(
        new File("TestData\\Book1.xlsx"), "pdf", null, null);
} catch (ApiException e) {
    e.printStackTrace();
}	

```
{{< /tab >}}

{{< tab tabNum="3" >}}

```go

CellsAPI := NewCellsApiService(clientId, clientSecret)
args := new(CellsWorkbookPutConvertWorkbookOpts)
args.Format = "pdf"
file, err := os.Open("TestData\\Book1.xlsx")
if err != nil {
	return
}
localVarReturnValue, httpResponse, err := CellsAPI.CellsWorkbookPutConvertWorkbook(file, args)
if err != nil {
	t.Error(err)
} else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
	t.Fail()
} else {
	fmt.Printf("\t TestCellsPutConvertWorkbook - %d\n", httpResponse.StatusCode)
}
```

{{< /tab >}}

{{< /tabs >}}
