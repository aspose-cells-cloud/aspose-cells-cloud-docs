---
title: "تحديث محور الفئة في المخطط"
type: docs
url: /ar/charts/category-axis/update/
weight: 160
keywords: "Aspose.Cells, مخطط, محور الفئة, REST API, Excel, Cloud SDK"
description: "تحديث محور الفئة في مخطط داخل ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API."
ArticleTitle: "تحديث محور الفئة في المخطط – واجهة Aspose.Cells Cloud API"
---

تقوم هذه الواجهة بتحديث محور الفئة في مخطط.

## واجهة PostChartCategoryAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
| -------------- | ------- | -------- | ----------- |
| name | string | path | اسم ملف Excel. |
| sheetName | string | path | اسم ورقة العمل التي يحتوي المخطط عليها. |
| chartIndex | integer | path | الفهرس (من الصفر) للمخطط المراد تحديثه. |
| axis | object | body | كائن JSON يُعرّف خصائص محور الفئة. |
| folder | string | query | المجلد في التخزين السحابي حيث يقع الملف (اختياري). |
| storageName | string | query | اسم التخزين (اختياري). |

**مخطط جسم الطلب – كائن `axis`**

| الخاصية | النوع | الوصف |
|----------|--------|-------------|
| IsAutomaticMajorUnit | boolean | تحديد ما إذا كان يتم احتساب الوحدة الرئيسية تلقائيًا. |
| MajorUnit | number | قيمة الوحدة الرئيسية عندما تكون `IsAutomaticMajorUnit` تساوي `false`. |
| IsAutomaticMinorUnit | boolean | تحديد ما إذا كان يتم احتساب الوحدة الثانوية تلقائيًا. |
| MinorUnit | number | قيمة الوحدة الثانوية عندما تكون `IsAutomaticMinorUnit` تساوي `false`. |
| Title | object | إعدادات العنوان للمحور (مثل `Text`، `Font`، `Visible`). |
| TickLabelPosition | string | موقع تسميات العلامات (مثل `Low`، `High`، `NextToAxis`). |
| ... | ... | خصائص المحور الإضافية كما هو مُعرّف في وثيقة API. |

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|------|-----------------------------|--------------------------------------------------|
| 200 | OK (تم بنجاح) | تمت تطبيق الفلتر بنجاح؛ يحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request (طلب خاطئ) | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized (غير مُصرّح) | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large (حمولة كبيرة جدًا) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | Internal Server Error (خطأ داخلي في الخادم) | حدث خطأ غير متوقع في الخادم. |

**المتطلبات المسبقة / المصادقة**

لاستدعاء هذه النقطة النهائية، يجب عليك الحصول على رمز وصول JWT من خدمة مصادقة Aspose.Cells Cloud (`/connect/token`)، ثم تضمين الرمز في رأس `Authorization` كما هو موضح في المثال أدناه.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "axis": {
          "IsAutomaticMajorUnit": true,
          "IsAutomaticMinorUnit": true,
          "Title": {
            "Text": "Category Axis",
            "Visible": true
          }
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**مثال على الاستجابة**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

تُعرّف [仕様 OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartCategoryAxis) واجهة برمجة تطبيقات عامة قابلة للاستخدام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

### ملاحظات

* النقطة النهائية تتطلب استخدام HTTPS؛ استخدام HTTP قد يؤدي إلى ظهور تحذيرات محتوى مختلط في المتصفحات.
* يجب استبدال جميع القيم العينية (placeholders) (`{name}`، `{sheetName}`، `{chartIndex}`، `{folder}`، `{storageName}`) بمعرفات فعلية.
* أنواع المخططات المدعومة لتحديث محور الفئة مذكورة في مرجع API.

## عائلة SDK السحابية

استخدام SDK يُعدّ أفضل طريقة لتسريع عملية التطوير، إذ يتولى SDK إدارة التفاصيل منخفضة المستوى ويسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء المكالمات إلى خدمات الويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartCategoryAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< /tab >}}

{{< /tabs >}}