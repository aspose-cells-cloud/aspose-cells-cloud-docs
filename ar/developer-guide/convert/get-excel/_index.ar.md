---
title: يحصل على ملف Excel إلى تنسيق آخر
second_title: Aspose.Cells Cloud Documen
linktitle: جي
type: docs
url: /ar/export-different-formats/
aliases: [/export-excel-workbook-to-different-file-formats/]
keywords: Get excel files to kinds of format files
description: Aspose.Cells Cloud REST API دعم الحصول على ملفات Excel لأنواع الملفات ذات التنسيق. يدعم SDK أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 10
kwords: Excel، Office Cloud، REST API، جدول البيانات، PDF، CSV، Json، Markdwon، يحصل على ملف Excel إلى تنسيقات أخرى
---
يشير REST API إلى ملف Excel `get` إلى ملف بتنسيق مختلف.


**معلمة الاستعلام**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|شكل|خيط| تنسيق الملف (csv/xls/html/mhtml/ods/pdf/xml/txt/tiff/xlsb/xlsm/xlsx/xltm/xltx/xps/png/jpg/gif/emf/bmp/md/Numbers/wmf/svg )|
|كلمة المرور|خيط||
|com.isAutoFit|خيط|خطأ صحيح|
|this.onlySaveTable|خيط|خطأ صحيح|
|outPath|خيط|موقف الملف الجديد.|
|مجلد|خيط|مجلد المصنف الأصلي.|
|اسم التخزين|خيط|اسم التخزين.|



## بقية API

|**API**|**يكتب**|**وصف**|**رابط التبختر**|
|:- |:- |:- |:- |
|/الخلايا/{الاسم}|يحصل|تصدير المصنف إلى تنسيق آخر.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|


 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.

 يمكنك استخدام**cURL**أداة سطر الأوامر للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.


{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}
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
Aspose.Cells.Cloud.SDK.Api.LightCellsApi LightCellsApi = new Aspose.Cells.Cloud.SDK.Api.LightCellsApi("your client id", "your client secret");
IDictionary<string, Stream> mapFiles = new Dictionary<string, Stream>();
mapFiles.Add("assemblytest.xlsx", File.OpenRead(@".\TestData\assemblytest.xlsx"));
mapFiles.Add("datasource.xlsx", File.OpenRead(@".\TestData\datasource.xlsx"));
Aspose.Cells.Cloud.SDK.Model.FilesResult filesResult = LightCellsApi.PostExport(files, "Workbook", "pdf");
Assert.IsNotNull(filesResult);


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
    FilesResult response = liteApi.postExport(fileMap, "workbook","pdf");
} catch (ApiException e) {
    e.printStackTrace();
}		

```
{{< /tab >}}

{{< tab tabNum="3" >}}

```go
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/
LightCellsAPI := NewLightCellsApiService(clientId, clientSecret)

var fileMap map[string]string
fileMap = make(map[string]string)
fileMap["Book1.xlsx"] = "TestData\\Book1.xlsx"
fileMap["Book2.xlsx"] = "TestData\\Book2.xlsx"
postOpts := new(PostExportOpts)
postOpts.Format = "pdf"
postOpts.ObjectType = "workbook"
_, httpResponse, err := LightCellsAPI.PostExport(fileMap, postOpts)
if err != nil {
	t.Error(err)
} else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
	t.Fail()
} else {
	fmt.Printf("\tTestCellsPostExport \n")
}


```

{{< /tab >}}

{{< /tabs >}}
