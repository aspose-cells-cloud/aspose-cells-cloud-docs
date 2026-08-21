---
title: "إضافة مرشح لون في ورقة عمل Excel"
second_title: "Document"
linktitle: "إضافة مرشح لون"
type: docs
url: /ar/autofilter/add-color-filter/
aliases: [  /ar/filter-a-list-using-a-color-filter/ , /ar/autofilter/add-a-color-filter/ ]
keywords: "Excel, مرشح لون, Aspose.Cells Cloud, REST API, مرشح تلقائي, مصادقة JWT"
description: "تعلم كيفية تطبيق مرشح لون على ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud API. يتضمن الرابط_endpoint_، المعاملات، مثال cURL، معالجة الأخطاء، وأمثلة SDKs."
weight: 65
ArticleTitle: "إضافة مرشح لون في ورقة عمل Excel باستخدام Aspose.Cells Cloud API"
---

تعلم كيفية إضافة مرشح لون إلى ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud API. يغطي هذا الدليل الرابط_المطلوب_، المعاملات، شروط المصادقة المسبقة، مثال طلب cURL، أمثلة SDKs، ومعالجة الاستجابة.

تضيف هذه الواجهة البرمجية REST **مرشح لون** إلى ورقة عمل Excel.

## PutWorksheetColorFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

### **الأمان والمصادقة**

تتطلب واجهات Aspose.Cells Cloud APIs أمانًا وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة مبنية على رمز JWT</a>.

### معاملات الطلب:


| اسم المعاملة | النوع    | الموقع | الوصف                                                                 |
|-------------|---------|--------|-----------------------------------------------------------------------------|
| name        | string  | path   | اسم ملف Excel.                                                 |
| sheetName   | string  | path   | اسم ورقة العمل التي تحتوي على البيانات المراد تصفية.           |
| range       | string  | query  | النطاق الخلوي الذي يُطبّق عليه المرشح (مثل `A1:B10`).            |
| fieldIndex  | integer | query  | المؤشر المبتدئ من الصفر للعمود الذي يُطبّق عليه مرشح اللون.       |
| colorFilter | object  | body   | كائن JSON يُعرّف الألوان الأمامية والخلفية المراد تصفيتها.   |
| matchBlanks | boolean | query  | ما إذا كانت الصفوف التي تحتوي على خلايا فارغة يجب تضمينها في نتائج التصفية.   |
| refresh     | boolean | query  | إذا كانت القيمة `true`، فتُحدّث ورقة العمل بعد تطبيق المرشح.           |
| folder      | string  | query  | المجلد في التخزين حيث يقع ملف Excel.                      |
| storageName | string  | query  | اسم خدمة التخزين (مثل Aspose Cloud Storage).              |

**مخطط JSON الخاص بـ `colorFilter`**

| الخاصية          | النوع   | الوصف                                                                    | الإلزام |
|-------------------|--------|--------------------------------------------------------------------------------|----------|
| Pattern           | string | نمط التصفية (مثل `"Solid"`).                                             | نعم      |
| ForegroundColor   | object | يُعرّف اللون الأمامي. يحتوي على خصائص فرعية مثل `Color`، `ColorIndex`، `IsShapeColor`، `ThemeColor`، و `Type`. | لا |
| BackgroundColor   | object | يُعرّف اللون الخلفي. نفس الخصائص الفرعية مثل `ForegroundColor`.      | لا |

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                      |
|-------|-----------------------------|--------------------------------------------------|
| 200   | OK                          | تم تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request                 | معاملات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401   | Unauthorized                | رمز JWT غير صالح أو مفقود. |
| 413   | Payload Too Large           | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500   | Internal Server Error       | خطأ غير متوقع في الخادم. |

## كيفية استخدام PutWorksheetColorFilter API باستخدام SDKs

### **مواصفات PutWorksheetColorFilter API**

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetColorFilter) واجهة برمجة قابلة للوصول العام وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات لواجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/colorFilter?range=A1%3AB1&fieldIndex=0" \
-X PUT \
-d "{ \"Pattern\": \"Solid\", \"ForegroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 1 }, \"Type\": \"Automatic\" }, \"BackgroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 0 }, \"Type\": \"Automatic\" }}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع التطوير. تعمل SDKs على إخفاء التفاصيل منخفضة المستوى حتى تتمكن من التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetColorFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetColorFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetColorFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetColorFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetColorFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetColorFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetColorFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetColorFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

**انظر أيضًا:** [إضافة مرشح مخصص](https://docs.aspose.cloud/cells/autofilter/add-custom-filter/)، [إضافة مرشح تاريخ](https://docs.aspose.cloud/cells/autofilter/add-date-filter/)، [حذف المرشح التلقائي](https://docs.aspose.cloud/cells/autofilter/remove-auto-filter/).