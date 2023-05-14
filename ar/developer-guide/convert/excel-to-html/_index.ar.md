---
title: Excel الى HTM
second_title: Aspose.Cells Cloud Documen
linktitle: Excel الى HTM
type: docs
url: /ar/convert/excel-to-html/
aliases: [/convert-excel-file-to-html-in-cloud/]
keywords: Convert excel files to html files
description: Aspose.Cells Cloud REST API يدعم تحويل ملفات Excel إلى ملفات html. SDK يدعم أنواع لغات التطوير. وهي تشمل Android و C# و Go و Java و NodeJS و Perl و PHP و Python و Ruby و swift
weight: 100
---
هذا REST API `saveas` ملف Excel إلى HTML.

[POST / الخلايا / {name} / saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) يتيح لك API حفظ ملف MS Excel كملف HTML بإعدادات إضافية وحفظ النتيجة في وحدة التخزين.

هذا REST API `convert` ملف Excel إلى HTML.

[وضع / خلايا / تحويل](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)يتيح لك API تحويل ملف MS Excel إلى ملف HTML بإعدادات إضافية وحفظ النتيجة في الاستجابة.

هذا REST API `export` ملف Excel إلى HTML.

[الحصول على / الخلايا / {name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  )يتيح لك API تحويل ملف MS Excel إلى ملف HTML بإعدادات إضافية وحفظ النتيجة في الاستجابة.

## REST API

|**API**|**يكتب**|**وصف**|**رابط التباهي**|
|:- |:- |:- |:- |
|/ خلايا / تحويل|يضع|يحول المصنف من طلب المحتوى إلى تنسيق ما|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/ خلايا / {name}|يحصل|يصدر المصنف إلى تنسيق آخر.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/ الخلايا / {name} / saveAs|بريد|تصدير المصنف إلى تنسيق|[PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|



تحدد واجهات برمجة التطبيقات هذه واجهة برمجة يمكن الوصول إليها بشكل عام وتتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.

 يمكنك استخدام**cURL** أداة سطر الأوامر للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.


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

## عائلة Cloud SDK

 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة من Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام حزم SDK متنوعة:


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
