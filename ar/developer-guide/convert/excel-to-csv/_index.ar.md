﻿---
title: Excel إلى CS
second_title: Aspose.Cells Cloud Documen
linktitle: Excel إلى CS
type: docs
url: /ar/convert/excel-to-csv/
aliases: [/convert-excel-file-to-csv-in-cloud/]
keywords: Convert excel files to csv files
description: Aspose.Cells Cloud REST API يدعم تحويل ملفات Excel إلى ملفات CSV. يدعم SDK أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 90
kwords: Excel، Office كلاود، ريست API، جدول البيانات، PDF، CSV، Json، Markdwon، Excel إلى CSV
---
هذا ملف Excel REST API `saveas` إلى CSV.

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) يتيح لك API حفظ ملف MS Excel كملف CSV مع إعدادات إضافية وحفظ النتيجة في وحدة التخزين.

هذا ملف Excel REST API `convert` إلى CSV.

[وضع /الخلايا/تحويل](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) يتيح لك API تحويل ملف MS Excel إلى ملف CSV بإعدادات إضافية وحفظ النتيجة في الاستجابة.

هذا ملف Excel REST API `export` إلى CSV.

[الحصول على /الخلايا/{الاسم}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) يتيح لك API تحويل ملف MS Excel إلى ملف CSV بإعدادات إضافية وحفظ النتيجة في الاستجابة.

## بقية API

|**API**|**يكتب**|**وصف**|**رابط التبختر**|
|:- |:- |:- |:- |
|/الخلايا/تحويل|يضع|تحويل المصنف من محتوى الطلب إلى بعض التنسيق|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/الخلايا/{الاسم}|يحصل|تصدير المصنف إلى تنسيق آخر.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/الخلايا/{name}/saveAs|بريد|تصدير المصنف إلى التنسيق|[PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|



تحدد واجهات برمجة التطبيقات هذه واجهة برمجة يمكن الوصول إليها بشكل عام وتتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.

 يمكنك استخدام**cURL**أداة سطر الأوامر للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.


{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=csv" \
-X PUT \
-d {"File":{}} \
-H "Content-Type:  multipart/form-data" \
-H "Accept:  multipart/form-data" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.csv" \
-X POST \
-d "{'SaveFormat':'csv', 'ImageFormat': 'csv'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=html" \
-X GET \
-d "{'SaveFormat':'csv', 'ExportImagesAsBase64': 'true'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"


```

{{< /tab >}}
{{< /tabs >}}

## عائلة Cloud SDK

 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. تهتم حزمة SDK بالتفاصيل ذات المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج (SDK) المتنوعة:



{{< tabs tabTotal="3" tabID="3" tabName1="C#" tabName2="Java" tabName3="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/
Aspose.Cells.Cloud.SDK.Api.CellsApi cellsApi = new CellsApi("your client id", "your client secret");
var response = cellsApi.CellsWorkbookPutConvertWorkbook( File.OpenRead(@".\TestData\datasource.xlsx"), "csv", null, null);
Assert.IsInstanceOf<System.IO.Stream>(response, "response is System.IO.Stream");

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/
try{
    LightCellsApi liteApi = new LightCellsApi(System.getenv("CellsCloudTestClientId"),System.getenv("CellsCloudTestClientSecret"));
    String AssemblyTestXlsx = "assemblytest.xlsx";
    String DataSourceXlsx = "datasource.xlsx";
    HashMap<String,File> fileMap = new HashMap<String,File>();
    fileMap.put(AssemblyTestXlsx , new File("TestData\\" + AssemblyTestXlsx));
    fileMap.put(DataSourceXlsx , new File("TestData\\" + DataSourceXlsx) );
    FilesResult response = liteApi.postExport(fileMap, "workbook","csv");
} catch (ApiException e) {
    e.printStackTrace();
}		

//2. solution
try{
    CellsApi api = new CellsApi(System.getenv("CellsCloudTestClientId"),System.getenv("CellsCloudTestClientSecret"));
    File response = api.cellsWorkbookPutConvertWorkbook(
        new File("TestData\\Book1.xlsx"), "csv", null, null);
} catch (ApiException e) {
    e.printStackTrace();
}	

```
{{< /tab >}}

{{< tab tabNum="3" >}}

```go

LightCellsAPI := NewLightCellsApiService(clientId, clientSecret)

var fileMap map[string]string
fileMap = make(map[string]string)
fileMap["Book1.xlsx"] = "TestData\\Book1.xlsx"
fileMap["Book2.xlsx"] = "TestData\\Book2.xlsx"
postOpts := new(PostExportOpts)
postOpts.Format = "csv"
postOpts.ObjectType = "workbook"
_, httpResponse, err := LightCellsAPI.PostExport(fileMap, postOpts)
if err != nil {
	t.Error(err)
} else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
	t.Fail()
} else {
	fmt.Printf("\tTestCellsPostExport \n")
}

CellsAPI := NewCellsApiService(clientId, clientSecret)
args := new(CellsWorkbookPutConvertWorkbookOpts)
args.Format = "csv"
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
