---
title: "تحديث المحور الفئات الثاني للرسم البياني"
type: docs
url: /ar/charts/second-category-axis/update/
weight: 160
keywords: "Aspose.Cells, الرسم البياني, المحور الفئات الثاني, واجهة REST API, تحديث الرسم البياني, Excel, واجهة سحابية"
description: "تعلم كيفية تحديث المحور الفئات الثاني للرسم البياني في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API."
ArticleTitle: "تحديث المحور الفئات الثاني للرسم البياني – واجهة Aspose.Cells Cloud API"
---

تقوم هذه الواجهة POSTChartSecondCategoryAxis API بتحديث المحور الفئات الثاني للرسم البياني.

## واجهة PostChartSecondCategoryAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **الأمان والمصادقة**

تتطلب واجهات Aspose.Cells Cloud API مصادقة <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" dir="ltr">مبنيّة على رمز JWT</a> وتُعدّ آمنة.

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|-------|
| name | سلسلة نصية | في المسار (path) | اسم ملف Excel. |
| sheetName | سلسلة نصية | في المسار (path) | اسم ورقة العمل التي يحتويها الرسم البياني. |
| chartIndex | عدد صحيح | في المسار (path) | الفهرس المبدأ من الصفر للرسم البياني المراد تحديثه. |
| axis | كائن | في الجسم (body) | كائن المحور الفئات الثاني مع الإعدادات الجديدة. |
| folder | سلسلة نصية | في الاستعلام (query) | مسار المجلد الذي يُخزّن فيه الملف. |
| storageName | سلسلة نصية | في الاستعلام (query) | اسم خدمة التخزين. |

**المصادقة** – تتطلب الواجهة رمز وصول OAuth 2.0 صالح. يمكنك إنشاء رمز JWT اتباعًا [إرشادات المصادقة](https://docs.aspose.cloud/cells/authentication/). وينبغي تضمين الرمز في الرأس `Authorization` كما هو مبين في مثال cURL أدناه.

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondCategoryAxis) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ 
        "axis": {
          /* إعدادات المحور، مثال: "Title": "عنوان المحور الجديد"، "IsVisible": true */
        }
      }'
```

*استبدل `{name}` و`{sheetName}` و`{chartIndex}` و`{folder}` و`{storageName}` بقيمك الفعلية. يجب أن يحتوي جسم الطلب على كائن `axis` مع الإعدادات المرغوبة.*

{{< /tab >}}

{{< tab tabNum="2" >}}

**استجابة ناجحة (200)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Id": "chart_1",
    "SecondCategoryAxis": {
      "Title": "عنوان المحور الجديد",
      "IsVisible": true,
      /* خصائص المحور الإضافية */
    }
  }
}
```

**استجابات الأخطاء**  

| رمز الحالة | الوصف |
|-------------|-------|
| 400 | طلب غير صالح – معاملات مفقودة أو غير صحيحة. |
| 401 | غير مصادق عليه – رمز JWT غير صالح أو مفقود. |
| 404 | غير موجود – الملف أو ورقة العمل أو الرسم البياني المحدد غير موجود. |
| 500 | خطأ داخلي في الخادم – شرط غير متوقع حدث في الخادم. |

```json
{
  "Code": 400,
  "Message": "حمولة الطلب غير صالحة."
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK للحاسوب السحابي

تبسّط SDKs عملية التطوير من خلال معالجة التفاصيل منخفضة المستوى وتُمكّنك من التركيز على منطق أعمالك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات Aspose.Cells عبر الويب باستخدام مكتبات SDK مختلفة:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondCategoryAxis.js" >}}
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

**ملاحظات وممارسات مُستحسَنة**

* معامل `chartIndex` يبدأ من الصفر؛ أول رسم بياني في ورقة العمل يحمل الفهرس 0.  
* تدعم الواجهة تنسيقات ملفات المصنف `.xlsx` و`.xls`.  
* اضمّن فقط الخصائص التي تحتاجها في كائن `axis`; ستحتفظ الخصائص غير المحددة بقيمها الحالية.  
* التزم بإرشادات تحديد معدل الطلبات (عادةً 100 طلب في الدقيقة لكل حساب) لتجنّب تقييد الوصول.