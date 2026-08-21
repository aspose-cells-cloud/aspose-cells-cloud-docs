---
title: "إضافة كائن OLE في ورقة عمل Excel"
second_title: "الوثيقة"
linktitle: "إضافة كائن OLE"
type: docs
url: /oleobjects/add/
aliases: [/add-oleobject-to-excel-worksheet/]
keywords: "إضافة كائن OLE، Excel، Aspose.Cells Cloud، REST API، SDK"
description: "استخدم واجهة Aspose.Cells Cloud REST API لإضافة كائنات OLE إلى أوراق عمل Excel. يمكن استدعاء الواجهة مباشرةً أو عبر SDKs المُتاحة بلغات C#، Java، PHP، Ruby، Node.js، Python، Perl، و Go."
ArticleTitle: "إضافة كائن OLE إلى ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud API"
weight: 20
---

تتيح واجهة Aspose.Cells Cloud API التعديل البرمجي لملفات كتب عمل Excel، بما في ذلك إمكانية تضمين كائنات OLE (مثل مستندات Word، ملفات PDF، أو غيرها من الملفات الثنائية) مباشرة داخل ورقة عمل.

تُضيف هذه الواجهة عبر REST API **كائن OLE** إلى ورقة عمل Excel.

**المتطلبات المسبقة** – يجب أن تمتلك رمز مصادقة JWT ساري المفعول، وأن تُرفع أي ملفات مصادر يُشار إليها عبر `oleFile` أو `imageFile` إلى موقع التخزين المحدد مسبقًا قبل استدعاء نقطة النهاية.

## PutWorksheetOleObject API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### **الأمان والمصادقة**

واجهات Aspose.Cells Cloud API آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل     | النوع    | الموقع | الوصف                                              |
|----------------|---------|--------|----------------------------------------------------|
| name           | string  | path   | اسم ملف كتاب العمل.                                |
| sheetName      | string  | path   | اسم ورقة العمل.                                    |
| oleObject      | object  | body   | تعريف كائن OLE.                                     |
| upperLeftRow   | integer | query  | فهرس الصف للزاوية العلوية اليسرى (الافتراضي 0).     |
| upperLeftColumn| integer | query  | فهرس العمود للزاوية العلوية اليسرى (الافتراضي 0).   |
| height         | integer | query  | ارتفاع كائن OLE (الافتراضي 0).                      |
| width          | integer | query  | عرض كائن OLE (الافتراضي 0).                         |
| oleFile        | string  | query  | اسم ملف مصدر OLE.                                   |
| imageFile      | string  | query  | اسم ملف صورة المعاينة.                              |
| folder         | string  | query  | المجلد الذي يحتوي على كتاب العمل.                   |
| storageName    | string  | query  | اسم وحدة التخزين المراد استخدامها.                  |

**ملاحظات** – يستخدم `upperLeftRow` و `upperLeftColumn` الترقيم البادئ بصفر (zero-based indexing). يجب أن يكون `oleFile` (وباختياري `imageFile`) موجودًا مسبقًا في وحدة التخزين الهدف؛ وإلا سيُعاد خطأ في الطلب.

يعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/PutWorksheetOleObject) واجهة برمجة تطبيقية متاحة للعامة وتتيح إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** لاستدعاء خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إضافة كائن OLE باستخدام cURL. **يجب استخدام HTTPS في جميع المكالمات المُستخدمة في الإنتاج.**

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/oleobjects" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"ImageSourceFullName":"aspose-logo.png", "IsAutoSize":true, "SourceFullName":"Sample_Book2.xls", "UpperLeftRow":15, "Top":10, "UpperLeftColumn":5, "Left":10, "Width":400, "Height":400}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

![لقطة شاشة تُظهر كائن OLE مُدمج في ورقة عمل Excel](/cells/images/ole-object-example.png)

**رموز حالة HTTP المحتملة**

| الرمز | الوصف                                                |
|------|------------------------------------------------------|
| 200  | تمت إضافة كائن OLE بنجاح.                           |
| 400  | طلب غير صالح – معاملات مفقودة أو غير صحيحة.        |
| 401  | غير مخوّل – رمز JWT غير صالح أو مفقود.             |
| 404  | غير موجود – ملف كتاب العمل أو ورقة العمل أو ملف المصدر غير موجود. |
| 500  | خطأ داخلي في الخادم – فشل غير متوقع.               |

يُعاد استجابة نموذجية ناجحة مع حُمولة JSON التالية:

```json
{
  "Code": 200,
  "Status": "OK",
  "Data": {
    "OleObjectId": "12345",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Width": 400,
    "Height": 400,
    "SourceFullName": "Sample_Book2.xls",
    "ImageSourceFullName": "aspose-logo.png"
  }
}
```

## عائلة SDK للسحابة

استخدام SDK يُسرّع عملية التطوير، فهو يُجرّدك من التفاصيل التقنية منخفضة المستوى، ويسمح لك بالتركيز على منطق أعمالك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر واجهة الويب باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}