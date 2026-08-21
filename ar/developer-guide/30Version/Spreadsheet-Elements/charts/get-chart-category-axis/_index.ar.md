---
title: "احصل على محور الفئات للرسم البياني"
type: docs
url: /charts/category-axis/get/
weight: 60
keywords: "Aspose.Cells, محور الفئات للرسم البياني, Excel, REST API, Cloud Storage, OAuth2, وثائق API"
description: "يُعيد محور الفئات لرسم بياني موجود في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API."
ArticleTitle: "احصل على محور الفئات للرسم البياني – وثائق API لـ Aspose.Cells Cloud"
---

تسترجع هذه الواجهة **محور الفئات** لرسم بياني.  
لاستدعاء هذه الواجهة، يجب أن تقدّم رمز وصول JWT OAuth 2.0 صالحًا، ويجب أن يكون ملف المصنف مخزّنًا في مساحة التخزين السحابية لـ Aspose Cloud.

**المتطلبات الأساسية**  
قبل استخدام هذه الواجهة، تأكّد من وجود ما يلي:  

- رمز وصول JWT OAuth 2.0 تم الحصول عليه وهو ساري المفعول لخدمات Aspose Cloud.  
- ملف المصنف مُحمّل في مساحة التخزين السحابية لـ Aspose Cloud (الافتراضية أو مجلد محدّد).  
- تستخدم إصدار الواجهة **v3.0** كما هو مبيّن في عنوان URL للطلب.  
- لدى التطبيق الذي يُجري الطلب صلاحية قراءة ملف المصنف والوصول إلى أوراق عمل المصنف.

## واجهة GetChartCategoryAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

**الخلفية** – إن إزالة جميع الرسوم البيانية من ورقة العمل مفيد عندما تحتاج إلى إعادة ضبط التخطيط البصري لورقة العمل، أو استبدال التصورات القديمة، أو إعداد المصنف لإعادة الاستخدام دون الاحتفاظ ببيانات الرسوم البيانية السابقة.

### **الأمان والمصادقة**

واجهات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع   | الموقع   | الوصف                                              |
|------------|---------|----------|-----------------------------------------------------|
| name       | string  | path     | اسم ملف المصنف.                                     |
| sheetName  | string  | path     | اسم ورقة العمل التي تحتوي على الرسم البياني.       |
| chartIndex | integer | path     | المؤشر الصفري (zero-based) للرسم البياني المطلوب محوره. |
| folder     | string  | query    | مسار المجلد في مساحة التخزين حيث يقع المصنف.       |
| storageName| string  | query    | اسم خدمة التخزين (إذا لم يكن الاسم الافتراضي).     |

### **الاستجابة**

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

**رموز حالة HTTP**

| الرمز | المعنى                        | الوصف                                               |
|-------|-------------------------------|------------------------------------------------------|
| 200   | OK (تم بنجاح)                 | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request (طلب غير صالح)   | معاملات مفقودة أو غير صالحة (مثل: نوع ملف غير مدعوم). |
| 401   | Unauthorized (غير مُصادَق)    | رمز JWT غير صالح أو مفقود.                          |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | ملف مُحمّل يتجاوز الحد الأقصى للحجم.             |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                          |

## كيفية استخدام واجهة GetChartCategoryAxis API باستخدام مكتبات SDK

### مواصفات واجهة GetChartCategoryAxis API

تعرّف <a href="https://apireference.aspose.cloud/cells/#/Charts/GetChartCategoryAxis" rel="noopener noreferrer">مواصفة OpenAPI</a> واجهة برمجة تطبيقات قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفّح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية إجراء استدعاء إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis" \
-X GET \
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
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات Aspose.Cells Cloud SDK

استخدام مكتبة SDK هو أفضل طريقة لتسريع عملية التطوير. فالمكتبة SDK تتعامل مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDK.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر الويب باستخدام مكتبات SDK المختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# example placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java example placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP example placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby example placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python example placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartCategoryAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android example placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl example placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go example placeholder -->

{{< /tab >}}

{{< /tabs >}}