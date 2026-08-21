---
title: "إضافة مرشح تواريخ إلى ورقة عمل Excel"
second_title: "مستند"
linktitle: "إضافة مرشح تواريخ"
type: docs
url: /ar/autofilter/add-date-filter/
aliases:
  - /ar/add-date-filter-in-a-worksheet/
  - /ar/autofilter/add-a-date-filter/
description: "تعرّف على كيفية إضافة مرشح تواريخ إلى ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API (النسخة 3.0). يتضمن مثالًا باستخدام cURL، ومقتطفات من أكواد SDK (C#، Java، Python، إلخ)، والمعلمات، وإدارة الأخطاء."
weight: 65
ArticleTitle: "إضافة مرشح تواريخ إلى ورقة عمل Excel | واجهة Aspose.Cells Cloud API"
keywords: "Aspose.Cells، مرشح تواريخ Excel، واجهة AutoFilter، واجهة REST API، SDK في السحابة، cURL، أتمتة جداول البيانات"
---

تقوم هذه الواجهة REST بإضافة **مرشح تواريخ** إلى ورقة عمل Excel.

**المتطلبات المسبقة:** يجب أن يكون لديك رمز JWT صالح، وأن يكون الملف المطلوب موجودًا مسبقًا في موقع التخزين المحدّد. لا تتطلب الطلب إرسال جسم JSON.

## واجهة PutWorksheetDateFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة باستخدام رمز JWT</a>.

### معلمات الطلب


| اسم المعلمة             | النوع    | الموقع | الوصف                                                                                                                                                     |
| ------------------------ | ------- | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                 | string  | Path     | اسم ملف العمل.                                                                                                                                              |
| **sheetName**            | string  | Path     | اسم ورقة العمل.                                                                                                                                             |
| **range**                | string  | Query    | نطاق Excel الذي سيُطبّق عليه المرشح (مثل `A1:B1`).                                                                                                     |
| **fieldIndex**           | integer | Query    | المؤشر الصفري-الأساسي للعمود المراد ترشيحه.                                                                                                                       |
| **dateTimeGroupingType** | string  | Query    | نوع التجميع لمرشح التاريخ/الوقت. القيم المسموح بها هي `Day` و `Hour` و `Minute` و `Month` و `Second` و `Year`. القيم حساسة لحالة الأحرف؛ والقيمة الافتراضية هي `Day`. |
| **year**                 | integer | Query    | مكوّن السنة في قيمة المرشح.                                                                                                                             |
| **month**                | integer | Query    | مكوّن الشهر في قيمة المرشح.                                                                                                                            |
| **day**                  | integer | Query    | مكوّن اليوم في قيمة المرشح.                                                                                                                              |
| **hour**                 | integer | Query    | مكوّن الساعة في قيمة المرشح.                                                                                                                             |
| **minute**               | integer | Query    | مكوّن الدقيقة في قيمة المرشح.                                                                                                                           |
| **second**               | integer | Query    | مكوّن الثانية في قيمة المرشح.                                                                                                                           |
| **matchBlanks**          | boolean | Query    | تضمين الخلايا الفارغة (`true` أو `false`).                                                                                                                        |
| **refresh**              | boolean | Query    | تحديث المرشح بعد التطبيق (`true` أو `false`).                                                                                                          |
| **folder**               | string  | Query    | مسار المجلد الذي يوجد فيه ملف العمل الأصلي.                                                                                                                           |
| **storageName**          | string  | Query    | اسم خدمة التخزين.                                                                                                                                    |

*لا يتطلب طلب PUT وجود جسم طلب؛ يتم تزويد جميع المعلمات عبر سلسلة الاستعلام.*

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**كود حالات HTTP**

| الكود | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح                          | تم تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صحيح                 | معلمات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مصرّح به                | رمز JWT غير صالح أو مفقود. |
| 413  | حجم الحمولة كبير جدًا           | حجم الملف المرفّع يتجاوز الحد المسموح به. |
| 500  | خطأ داخلي في الخادم       | خطأ غير متوقع في الخادم. |
## كيفية استخدام واجهة PutWorksheetDateFilter API باستخدام SDKs

### مواصفات واجهة PutWorksheetDateFilter API


تُعرّف <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء الاتصال بواجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
-X PUT \
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



### استخدام Aspose.Cells Cloud SDKs

استخدام SDK هو أسرع طريقة للتطوير. تُHANDLE SDK التفاصيل منخفضة المستوى، مما يمكّنك من التركيز على مهام مشروعك. يُرجى زيارة <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للاطّلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}