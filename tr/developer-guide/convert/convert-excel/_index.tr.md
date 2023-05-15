---
title: Excel'i Dönüştür
second_title: Aspose.Cells Cloud Documen
linktitle: Dönüştür
type: docs
url: /tr/convert/excel-to-different-formats/
aliases: [/convert-excel-workbook-to-different-file-formats/]
keywords: Convert excel files to kinds of format files
description: Aspose.Cells Cloud REST API, excel dosyalarını biçim dosyası türlerine dönüştürmeyi destekler. SDK, geliştirme dili türlerini destekler. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 10
---
Bu REST API, `convert` excel dosyasının farklı biçim dosyasına işaret eder.

İstek, çok parçalı içeriğe sahip bir HTTP isteğidir (bkz.[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)veya[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çok parçalı içeriğin ilk bölümü veri dosyasını içerir ve ikincisi kaydetme seçeneklerini içerir.

**Sorgu Parametresi**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
|biçim|sicim| dosya formatı(csv/xls/html/mhtml/ods/pdf/xml/txt/tiff/xlsb/xlsm/xlsx/xltm/xltx/xps/png/jpg/gif/emf/bmp/md/Numbers/wmf/svg) )|


**İstek Gövde Parametresi**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
|veri dosyası| veri dosyası|Veri dosyası, çok parçalı içeriğin ilk bölümüne kaydedilir.|
|Seçenekleri Kaydet| Nesne|Kaydet seçeneği, çok parçalı içeriğin ikinci bölümüne kaydedin.|


## DİNLENME API

|**API**|**Tip**|**Tanım**|**Havalı Bağlantı**|
|:- |:- |:- |:- |
|/hücreler/dönüştür|KOYMAK|Çalışma kitabını istek içeriğinden bir biçime dönüştürür|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|


 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

 Kullanabilirsiniz**cURL** Aspose.Cells web hizmetlerine kolayca erişmek için komut satırı aracı. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.


{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:



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
