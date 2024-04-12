---
title: Excel a HTM
second_title: Aspose.Cells Cloud Documen
linktitle: Excel a HTM
type: docs
url: /es/convert/excel-to-html/
aliases: [/convert-excel-file-to-html-in-cloud/]
keywords: Convert excel files to html files
description: Aspose.Cells Cloud REST API admite la conversión de archivos de Excel a archivos html. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 100
---
Este archivo de Excel REST API `saveas` a HTML.

[POST /celdas/{nombre}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API le permite guardar el archivo MS Excel como archivo HTML con configuraciones adicionales y guardar el resultado en el almacenamiento.

Este archivo de Excel REST API `convert` a HTML.

[PUT /celdas/convertir](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)API le permite convertir el archivo MS Excel al archivo HTML con configuraciones adicionales y guardar el resultado en la respuesta.

Este archivo de Excel REST API `export` a HTML.

[OBTENER /celdas/{nombre}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  )API le permite convertir el archivo MS Excel al archivo HTML con configuraciones adicionales y guardar el resultado en la respuesta.

## DESCANSO API

|**API**|**Tipo**|**Descripción**|**Enlace de arrogancia**|
|:- |:- |:- |:- |
|/celdas/convertir|PONER|Convierte el libro de trabajo del contenido de la solicitud a algún formato|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/celdas/{nombre}|CONSEGUIR|Exporta el libro de trabajo a otro formato.|[Obtener libro de trabajo](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/celdas/{nombre}/saveAs|CORREO|Exportar libro de trabajo a formato|[Publicar documento guardar como](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|



Estas API definen una interfaz de programación de acceso público y le permiten realizar interacciones REST directamente desde un navegador web.

 Puedes usar**cURL** Herramienta de línea de comandos para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.


{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
-X PUT \
-d {"File":{}} \
-H "Content-Type:  multipart/form-data" \
-H "Accept:  multipart/form-data" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.html" \
-X POST \
-d "{'SaveFormat':'html', 'ExportImagesAsBase64': 'true'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=html" \
-X GET \
-d "{'SaveFormat':'html', 'ExportImagesAsBase64': 'true'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"


```

{{< /tab >}}
{{< /tabs >}}

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor revisa el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a servicios web Aspose.Cells utilizando varios SDK:


{{< tabs tabTotal="3" tabID="3" tabName1="C#" tabName2="Java" tabName3="Go" >}}

{{< tab tabNum="1" >}}

```csharp

Aspose.Cells.Cloud.SDK.Api.CellsApi cellsApi = new CellsApi("your client id", "your client secret");
var response = cellsApi.CellsWorkbookPutConvertWorkbook( File.OpenRead(@".\TestData\datasource.xlsx"), "html", null, null);
Assert.IsInstanceOf<System.IO.Stream>(response, "response is System.IO.Stream");

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

try{
    CellsApi api = new CellsApi(System.getenv("CellsCloudTestClientId"),System.getenv("CellsCloudTestClientSecret"));
    File response = api.cellsWorkbookPutConvertWorkbook(
        new File("TestData\\Book1.xlsx"), "html", null, null);
} catch (ApiException e) {
    e.printStackTrace();
}	

```
{{< /tab >}}

{{< tab tabNum="3" >}}

```go

CellsAPI := NewCellsApiService(clientId, clientSecret)
args := new(CellsWorkbookPutConvertWorkbookOpts)
args.Format = "html"
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
