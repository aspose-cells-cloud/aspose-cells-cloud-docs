---
title: "حذف مرشح تاريخ – Aspose.Cells Cloud"
second_title: "مستند"
linktitle: "حذف مرشح التاريخ"
type: docs
url: /autofilter/delete-date-filter/
aliases:
  - /remove-a-date-filter/
  - /autofilter/delete-a-date-filter/
weight: 100
keywords: "Aspose.Cells, حذف مرشح تاريخ, Excel AutoFilter, REST API, SDK"
description: "تعرّف على كيفية حذف مرشح تاريخ من ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن عنوان النهاية (Endpoint)، المعلمات، مثال على cURL باستخدام HTTPS، حملة الاستجابة (Response Payload)، وأكواد مقتطفات SDK."
ArticleTitle: "حذف مرشح تاريخ – وثائق واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة (REST API) بحذف مرشح تاريخ من ورقة عمل Excel.

**المتطلبات المسبقة:** تأكّد من امتلاك رمز JWT صالح، ووجود الملف المصنف في مستودع Aspose Cloud، وامتلاك الصلاحيات المناسبة لتعديل ورقة العمل.

## واجهة DeleteWorksheetDateFilter API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات الطلب

| اسم المعلمة          | النوع   | الموقع | الوصف                                                                                     |
|----------------------|---------|--------|---------------------------------------------------------------------------------------------|
| name                 | string  | path   | اسم ملف Excel.                                                                             |
| sheetName            | string  | path   | اسم ورقة العمل.                                                                            |
| fieldIndex           | integer | query  | المؤشر الصفر-الأساسي للعمود الذي يُطبّق عليه المرشح.                                       |
| dateTimeGroupingType | string  | query  | نوع التجميع لمرشح التاريخ (مثل: Year، Month، Day).                                         |
| year                 | integer | query  | مكوّن السنة في المرشح (القيمة المبدئية 0).                                                  |
| month                | integer | query  | مكوّن الشهر في المرشح (القيمة المبدئية 0).                                                  |
| day                  | integer | query  | مكوّن اليوم في المرشح (القيمة المبدئية 0).                                                  |
| hour                 | integer | query  | مكوّن الساعة في المرشح (القيمة المبدئية 0).                                                 |
| minute               | integer | query  | مكوّن الدقيقة في المرشح (القيمة المبدئية 0).                                                |
| second               | integer | query  | مكوّن الثانية في المرشح (القيمة المبدئية 0).                                                |
| folder               | string  | query  | مسار المجلد في المستودع حيث يوجد الملف.                                                    |
| storageName          | string  | query  | اسم مستودع Aspose Cloud.                                                                   |

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**رموز حالة HTTP**

| الكود | المعنى                      | الوصف                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------|
| 200  | OK                          | تمت تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.           |
| 400  | Bad Request                 | معلمات ناقصة أو غير صالحة (مثل: نوع ملف غير مدعوم).                  |
| 401  | Unauthorized                | رمز JWT غير صالح أو مفقود.                                            |
| 413  | Payload Too Large           | حجم الملف المرفّق تجاوز الحد المسموح به.                              |
| 500  | Internal Server Error       | خطأ داخلي في الخادم غير متوقع.                                        |

تُعيد الواجهة رموز حالة HTTP القياسية التي تُشير إلى نتيجة عملية الحذف.

| الكود | المعنى | الوصف |
|------|---------|-------|
| 200  | OK      | تمت حذف مرشح التاريخ بنجاح؛ تحتوي الاستجابة على حالة العملية. |
| 400  | Bad Request | معلمات ناقصة أو غير صالحة (مثل: نوع ملف غير مدعوم). |
| 401  | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413  | Payload Too Large | حجم الملف المرفّق تجاوز الحد المسموح به. |
| 500  | Internal Server Error | خطأ داخلي في الخادم غير متوقع. |

## كيفية استخدام واجهة DeleteWorksheetDateFilter API باستخدام SDKs

### مواصفات واجهة DeleteWorksheetDateFilter API

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetDateFilter" rel="noopener noreferrer">مواصفات OpenAPI</a> تُعرّف واجهة برمجة تطبيقات قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?fieldIndex=0&dateTimeGroupingType=Year&year=1920" \
  -X DELETE \
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

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولّى SDK تفاصيل المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات لخدمات ويب Aspose.Cells باستخدام SDKs متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}