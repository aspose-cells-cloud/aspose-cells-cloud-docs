---
title: "تحديث فلتر تلقائي في ورقة عمل إكسل"
second_title: "وثيقة"
linktitle: "تحديث الفلتر التلقائي"
type: docs
url: /ar/autofilter/refresh/
aliases: [  /ar/refresh-an-autofilter/ ]
weight: 100
keywords: "Aspose.Cells, AutoFilter, تحديث, إكسل, API, REST"
description: "تحديث فلتر تلقائي موجود في ورقة عمل إكسل باستخدام واجهة Aspose.Cells Cloud REST API. يشمل أمثلة لـ cURL و SDKات متعددة مثل C#، Java، Python، والمزيد."
ArticleTitle: "تحديث فلتر تلقائي في ورقة عمل إكسل"
---

### ماذا يفعل **التحديث**؟

استدعاء نقطة النهاية هذا يُطبّق معايير التصفية الحالية مجددًا بعد تغيّر بيانات الورقة (مثل إضافة أو حذف صفوف). لا يغيّر هذا الإجراء تعريف الفلتر؛ بل يقوم بتحديث العرض فقط ويُعيد استجابة توضّح الحالة.

### واجهة REST API

تقوم هذه واجهة REST API بتحديث الفلتر التلقائي في ورقة عمل إكسل (إصدار API **v3.0**).

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/refresh
```

### **الأمان والمصادقة**

تُعدّ واجهات Aspose.Cells Cloud API آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                            |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح (OK)                   | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request) | معطيات ناقصة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مصادق عليه (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413  | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

*أمثلة على استجابات الأخطاء*  

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "معطى غير صالح: لم يتم العثور على اسم الورقة (sheetName)."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "فشلت المصادقة. رمز JWT مفقود أو غير صالح."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "تجاوز حجم الملف المرفوع الحد الأقصى المسموح به."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "حدث خطأ غير متوقع في الخادم."
}
```

## كيفية استخدام واجهة PostWorksheetAutoFilterRefresh مع SDKs

###仕様 واجهة PostWorksheetAutoFilterRefresh

يُعرّف <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetAutoFilterRefresh" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات متاحة للعامة وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/refresh" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
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

### استخدام SDKات Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. تُدار التفاصيل منخفضة المستوى بواسطة الـ SDK، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKات Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات الويب الخاصة بـ Aspose.Cells باستخدام SDKات متنوعة:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetAutoFilterRefresh.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetAutoFilterRefresh.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetAutoFilterRefresh.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetAutoFilterRefresh.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetAutoFilterRefresh.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetAutoFilterRefresh.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetAutoFilterRefresh.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetAutoFilterRefresh.go" >}}

{{< /tab >}}

{{< /tabs >}}
---