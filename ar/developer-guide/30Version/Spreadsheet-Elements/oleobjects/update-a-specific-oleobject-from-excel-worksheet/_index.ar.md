---
title: "تحديث كائن OLE في ورقة عمل Excel"
second_title: "Document"
linktitle: "تحديث"
type: docs
url: /ar/oleobjects/update/
aliases: [  /ar/update-a-specific-oleobject-from-excel-worksheet/ ]
keywords: "تحديث كائن OLE، Excel، Aspose.Cells Cloud، REST API، SDK"
description: "تعرّف على كيفية تحديث كائن OLE (صورة، مخطط، إلخ) في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يشمل أمثلة لـ cURL وSDK، وخطوات المصادقة، ومعالجة الأخطاء."
weight: 30
author: "فريق توثيق Aspose Cloud"
lastmod: "2024-03-01"
ArticleTitle: "تحديث كائن OLE في ورقة عمل Excel – دليل واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية REST بتحديث **كائن OLE** في ورقة عمل Excel.

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud أمانًا وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

## واجهة برمجة تطبيقات PostUpdateWorksheetOleObject

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

معلمات الطلب هي:

| اسم المعلمة | النوع | موقع المعلمة | الوصف |
|------------|--------|----------------|----------------------------------------------------|
| name | string | path | اسم ملف المصنف. |
| sheetName | string | path | اسم ورقة العمل. |
| oleObjectIndex | integer | path | فهرس كائن OLE داخل ورقة العمل. |
| ole | object | body | التمثيل JSON لكائن OLE المراد تحديثه. |
| folder | string | query | المجلد الذي يحتوي على المصنف. |
| storageName | string | query | اسم خدمة التخزين. |

### حقول جسم الطلب

| الحقل | النوع | مطلوب | الوصف |
|-------|--------|--------|---------------------------------------------------------|
| ImageSourceFullName | string | اختياري | المسار إلى ملف الصورة المستخدم في كائن OLE. |
| IsAutoSize | boolean | اختياري | ما إذا كان يجب تلقائيًا ضبط حجم كائن OLE. |
| SourceFullName | string | مطلوب | ملف المصدر (مثل صورة أو مخطط) لكائن OLE. |
| UpperLeftRow | integer | مطلوب | فهرس الصف (مبني على الصفر) للزاوية العلوية اليسرى. |
| UpperLeftColumn | integer | مطلوب | فهرس العمود (مبني على الصفر) للزاوية العلوية اليسرى. |
| Left | integer | اختياري | الإزاحة الأفقية، بوحدات النقاط، من الزاوية العلوية اليسرى. |
| Top | integer | اختياري | الإزاحة الرأسية، بوحدات النقاط، من الزاوية العلوية اليسرى. |
| Width | integer | مطلوب | عرض كائن OLE، بوحدات النقاط. |
| Height | integer | مطلوب | ارتفاع كائن OLE، بوحدات النقاط. |

يعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/PostUpdateWorksheetOleObject) واجهة برمجة تطبيقات قابلة للوصول العام وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية استدعاء واجهة برمجة تطبيقات السحابة باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X POST \
  -d '{"ImageSourceFullName":"aspose-logo.png","IsAutoSize":true,"SourceFullName":"Sample_Book2.xls","UpperLeftRow":15,"Top":10,"UpperLeftColumn":5,"Left":10,"Width":400,"Height":400}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Index": 0,
    "ImageSourceFullName": "aspose-logo.png",
    "IsAutoSize": true,
    "SourceFullName": "Sample_Book2.xls",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Left": 10,
    "Top": 10,
    "Width": 400,
    "Height": 400
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## استجابات الأخطاء

| حالة HTTP | الكود | الرسالة |
|-----------|-------|--------------------------------------------------------------|
| 400 | 4000 | طلب خاطئ – معلمات مفقودة أو غير صالحة. |
| 401 | 4010 | غير مصرح به – رمز JWT غير صالح أو مفقود. |
| 404 | 4040 | غير موجود – المصنف أو ورقة العمل أو كائن OLE غير موجود. |
| 500 | 5000 | خطأ داخلي في الخادم – فشل غير متوقع من جانب الخادم. |

تعيد الواجهة البرمجية أيضًا حقلًا مخصصًا **Code** في جسم الاستجابة يطابق حالة HTTP (مثلًا: 200 → 2000، 400 → 4000، إلخ).

## متى تستخدم هذه الواجهة البرمجية؟

استخدم هذه النقطة النهائية عندما تحتاج إلى تعديل كائن OLE موجود—مثل صورة مضمنة أو مخطط أو مستند—بدون إعادة رفع ورقة العمل بالكامل. تتضمن السيناريوهات الشائعة تحديث مصدر الصورة، أو تغيير حجم الكائن، أو تعديل موقعه بعد إنشاء المصنف. للاطلاع على العمليات ذات الصلة، راجع [إضافة كائن OLE](/ar/oleobjects/add/) و [حذف كائن OLE](/ar/oleobjects/delete/).

## عائلة SDK للسحابة

استخدام SDK هو أسرع طريقة للتطوير. يُجرّد SDK التفاصيل منخفضة المستوى لتمكينك من التركيز على مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

يعرض المثال التالي بلغة C# كيفية تحديث كائن OLE باستخدام SDK لـ Aspose.Cells Cloud:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    AppSid = "<your-app-sid>",
    AppKey = "<your-app-key>"
};
var oleApi = new OleObjectsApi(config);
var request = new OleObjectUpdateRequest
{
    ImageSourceFullName = "aspose-logo.png",
    IsAutoSize = true,
    SourceFullName = "Sample_Book2.xls",
    UpperLeftRow = 15,
    UpperLeftColumn = 5,
    Left = 10,
    Top = 10,
    Width = 400,
    Height = 400
};

var response = oleApi.UpdateWorksheetOleObject("SampleBook.xlsx", "Sheet1", 0, request, folder: "myFolder");
Console.WriteLine($"Status: {response.Status}");
```

تعرض أمثلة الرمز التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}