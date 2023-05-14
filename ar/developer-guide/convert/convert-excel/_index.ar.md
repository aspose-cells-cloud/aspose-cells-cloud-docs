---
title: تحويل Exce
second_title: Aspose.Cells Cloud Documen
linktitle: كونفر
type: docs
url: /ar/convert/excel-to-different-formats/
aliases: [/convert-excel-workbook-to-different-file-formats/]
keywords: Convert excel files to kinds of format files
description: Aspose.Cells Cloud REST API يدعم تحويل ملفات Excel إلى أنواع من ملفات التنسيق. SDK يدعم أنواع لغات التطوير. وهي تشمل Android و C# و Go و Java و NodeJS و Perl و PHP و Python و Ruby و swift
weight: 10
---
يشير هذا REST API إلى `convert` ملف Excel إلى ملف تنسيق مختلف.

الطلب عبارة عن طلب HTTP بمحتوى متعدد الأجزاء (انظر[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)أو[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). يحتوي الجزء الأول من المحتوى متعدد الأجزاء على ملف البيانات والثاني يحتوي على خيارات الحفظ.

**معامِل الاستعلام**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|شكل|خيط| تنسيق الملف (csv / xls / html / mhtml / ods / pdf / xml / txt / tiff / xlsb / xlsm / xlsx / xltm / xltx / xps / png / jpg / gif / emf / bmp / md / Numbers / wmf / svg )|


**طلب معلمة الجسم**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|ملف البيانات| ملف البيانات|يتم حفظ ملف البيانات في الجزء الأول من المحتوى متعدد الأجزاء.|
|SaveOptions| هدف|حفظ الخيار حفظ في الجزء الثاني من المحتوى متعدد الأجزاء.|


## REST API

|**API**|**يكتب**|**وصف**|**رابط التباهي**|
|:- |:- |:- |:- |
|/ خلايا / تحويل|يضع|يحول المصنف من طلب المحتوى إلى تنسيق ما|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|


 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.

 يمكنك استخدام**cURL** أداة سطر الأوامر للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.


{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة Cloud SDK

 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة من Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام حزم SDK متنوعة:



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
