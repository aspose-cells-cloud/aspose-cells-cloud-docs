---
title: Excel a PD
second_title: Aspose.Cells Cloud Documen
linktitle: Excel a PD
type: docs
url: /es/convert/excel-to-pdf/
aliases: [/convert-excel-file-to-pdf-in-cloud/]
keywords: Convert excel files to pdf files
description: Aspose.Cells Cloud REST API admite la conversión de archivos de Excel a archivos pdf. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift
weight: 80
---
Este archivo de Excel REST API `saveas` a PDF.

[POST /celdas/{nombre}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API le permite guardar el archivo MS Excel como archivo PDF con configuraciones adicionales y guardar el resultado en el almacenamiento.

Este archivo de Excel REST API `convert` a PDF.

[PUT /celdas/convertir](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)API le permite convertir el archivo MS Excel en un archivo PDF con configuraciones adicionales y guardar el resultado en la respuesta.

Este archivo de Excel REST API `export` a PDF.

[OBTENER /celdas/{nombre}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  )API le permite convertir el archivo MS Excel en un archivo PDF con configuraciones adicionales y guardar el resultado en la respuesta.

## DESCANSO API


|**API**|**Tipo**|**Descripción**|**Enlace arrogante**|
|:- |:- |:- |:- |
|/celdas/convertir|PONER|Convierte el libro de trabajo del contenido de la solicitud a algún formato|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/celdas/{nombre}|CONSEGUIR|Exporta el libro de trabajo a otro formato.|[ObtenerLibroDeTrabajo](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/celdas/{nombre}/guardar como|CORREO|Exportar libro de trabajo a Formato|[PublicarDocumentoGuardarComo](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|



 Estos[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [ObtenerLibroDeTrabajo](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook), [PublicarDocumentoGuardarComo](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) Las API definen una interfaz de programación de acceso público y le permiten realizar interacciones REST directamente desde un navegador web.

 Puedes usar**cURL** herramienta de línea de comandos para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo hacer llamadas a Cloud API con cURL.




{{< tabs tabTotal="3" tabID="11" tabName11="Convert Workbook API" tabName12="Get Workbook format API" tabName13="Save  Workbook as format API" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}



```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}


```

{{< /tab >}}

{{< tab tabNum="13" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" -H "accept: multipart/form-data" 



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
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/
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
