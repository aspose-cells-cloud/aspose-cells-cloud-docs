﻿---
title: Excel'den HTM'ye
second_title: Aspose.Cells Cloud Documen
linktitle: Excel'den HTM'ye
type: docs
url: /tr/convert/excel-to-html/
aliases: [/convert-excel-file-to-html-in-cloud/]
keywords: Convert excel files to html files
description: Aspose.Cells Cloud REST API, excel dosyalarının html dosyalarına dönüştürülmesini destekler. SDK çeşitli geliştirme dillerini destekler. Bunlar arasında Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift bulunur
weight: 100
kwords: Excel, Office Cloud, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, Excel ila HTML
---
Bu REST API `saveas` excel dosyasını HTML'e ekleyin.

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API, MS Excel dosyasını ek ayarlarla HTML dosyası olarak kaydetmenizi ve sonucu depolama alanına kaydetmenizi sağlar.

Bu REST API `convert` excel dosyasını HTML'e ekleyin.

[PUT /hücreler/dönüştür](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API, MS Excel dosyasını ek ayarlarla HTML dosyasına dönüştürmenizi ve sonucu yanıta kaydetmenizi sağlar.

Bu REST API `export` excel dosyasını HTML'e ekleyin.

[GET /hücreler/{isim}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API, MS Excel dosyasını ek ayarlarla HTML dosyasına dönüştürmenizi ve sonucu yanıta kaydetmenizi sağlar.

## DİNLENME API

|**API**|**Tip**|**Tanım**|**Swagger Bağlantısı**|
|:- |:- |:- |:- |
|/hücreler/dönüştür|KOYMAK|Çalışma kitabını istek içeriğinden bazı biçimlere dönüştürür|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/hücreler/{isim}|ELDE ETMEK|Çalışma kitabını diğer formata aktarır.|[WorkBook'u Alın](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/cells/{name}/saveAs|POSTALAMAK|Çalışma kitabını Format'a aktar|[Belge SonrasıFarklı Kaydet](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|



Bu API'ler herkesin erişebileceği bir programlama arayüzünü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

 Kullanabilirsiniz**cURL**Aspose.Cells web hizmetlerine kolayca erişmek için komut satırı aracı. Aşağıdaki örnekte, cURL ile Cloud API'e nasıl çağrı yapılacağı gösterilmektedir.


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

## Bulut SDK Ailesi

 SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük düzeyli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanıza olanak tanır. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:


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
