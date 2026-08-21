---
title: "إضافة عامل تصفية لأعلى 10 عناصر في ورقة عمل إكسل (Aspose.Cells Cloud)"
ArticleTitle: "إضافة عامل تصفية لأعلى 10 عناصر في ورقة عمل إكسل – Aspose.Cells Cloud"
second_title: "وثيقة"
linktype: "docs"
url: /ar/autofilter/add-top-10-filter/
aliases:
  [/ar/filter-the-top-10-items-in-the-list/, /ar/autofilter/add-a-top-10-filter/]
keywords: "Aspose.Cells, عامل تصفية تلقائي، عامل تصفية لأعلى 10 عناصر، واجهة برمجة تطبيقات إكسل"
description: "تعرّف على كيفية تطبيق عامل تصفية تلقائي لأعلى 10 عناصر في ورقة عمل إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يتضمن النهاية (endpoint)، المُعطَلات (parameters)، مثال cURL باستخدام HTTPS، تفاصيل المصادقة، معالجة الأخطاء، وأجزاء من كود SDK لـ C#، Java، Python، والمزيد."
weight: 65
---

تقوم هذه الواجهة REST بتصفية **أعلى 10 عناصر** في قائمة.

> **المتطلبات الأساسية**  
> • احصل على رمز JWT صالح باستخدام مصادقة Aspose.Cells Cloud.  
> • رفع ملف مصنف إكسل إلى مساحة التخزين الخاصة بك في Aspose Cloud (أو حدد مساحة التخزين/المجلد الذي يوجد فيه الملف).  
> • اعرف اسم ورقة العمل ونطاق الخلية الذي تريد تطبيق التصفية عليه.

## PutWorksheetFilterTop10 API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filterTop10
```

### **الأمان والمصادقة**

واجهات برمجة التطبيقات الخاصة بـ Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### مُعطَلات الطلب

| اسم المُعطَل  | النوع    | الموقع | إجباري | القيمة الافتراضية | الوصف                                                                 |
| --------------- | ------- | -------- | -------- | ------- | --------------------------------------------------------------------------- |
| **name**        | string  | path     | نعم      | —       | اسم ملف إكسل.                                                 |
| **sheetName**   | string  | path     | نعم      | —       | اسم ورقة العمل التي تحتوي على البيانات.                           |
| **range**       | string  | query    | نعم      | —       | نطاق الخلايا الذي سيتم تطبيق التصفية عليه (مثال: `A1:B10`).             |
| **fieldIndex**  | integer | query    | نعم      | —       | المؤشر المبني على الصفر لعمود تطبيق التصفية عليه.              |
| **isTop**       | boolean | query    | نعم      | `true`  | `true` لتصفية العناصر العلوية؛ `false` للعناصر السفلية.                   |
| **isPercent**   | boolean | query    | لا       | `false` | `true` لاعتبار `itemCount` نسبة مئوية؛ `false` للعدد المطلق. |
| **itemCount**   | integer | query    | لا       | `10`    | عدد العناصر التي يجب تضمينها في عامل التصفية.                                   |
| **matchBlanks** | boolean | query    | لا       | `false` | `true` لتضمين الخلايا الفارغة في نتائج عامل التصفية.                        |
| **refresh**     | boolean | query    | لا       | `false` | `true` لتحديث عامل التصفية بعد تطبيقه.                             |
| **folder**      | string  | query    | لا       | —       | المجلد في التخزين حيث يوجد ملف إكسل.                      |
| **storageName** | string  | query    | لا       | —       | اسم مساحة تخزين Aspose Cloud.                                       |

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**استجابات الخطأ النموذجية**

```json
{
    "Code":400,
    "Message":"طلب غير صحيح – مُعطَلات مفقودة أو غير صالحة."
}
```

```json
{
    "Code":401,
    "Message":"غير مصرّح – رمز JWT غير صالح أو مفقود."
}
```

```json
{
    "Code":413,
    "Message":"حمولة كبيرة جدًا – حجم الملف المرفوع يتجاوز الحد المسموح به."
}
```

```json
{
    "Code":500,
    "Message":"خطأ داخلي في الخادم – حالة غير متوقعة في الخادم."
}
```

**رموز حالة HTTP**

| الكود | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | نجاح (OK)                          | تمت تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صحيح (Bad Request)                 | مُعطَلات مفقودة أو غير صالحة (مثال: نوع ملف غير مدعوم). |
| 401  | غير مصرّح (Unauthorized)                | رمز JWT غير صالح أو مفقود. |
| 413  | حمولة كبيرة جدًا (Payload Too Large)           | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500  | خطأ داخلي في الخادم (Internal Server Error)       | خطأ غير متوقع في الخادم. |
## كيفية استخدام PutWorksheetFilterTop10 API باستخدام مكتبات SDK

### مواصفات PutWorksheetFilterTop10 API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilterTop10) واجهة برمجة تطبيقات قابلة للوصول العام، وتمكّنك من إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية استدعاء الواجهة باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filterTop10?range=A1:B10&fieldIndex=0&isTop=true&itemCount=10" \
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

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أسرع طريقة للتطوير. فتتولى مكتبات SDK معالجة التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام مكتبات SDK المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilterTop10.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilterTop10.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilterTop10.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilterTop10.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilterTop10.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilterTop10.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilterTop10.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilterTop10.go" >}}

{{< /tab >}}

{{< /tabs >}}