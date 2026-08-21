---
title: "الحصول على محور القيمة الثاني للرسم البياني"
type: docs
url: /charts/second-value-axis/get/
weight: 60
keywords: Aspose.Cells, محور القيمة الثاني للرسم البياني, Excel, واجهة برمجة تطبيقات REST, سحابة, واجهة برمجة تطبيقات, محور الرسم البياني في Excel
description: استرداد المحور الثاني للقيمة لرسم بياني محدّد في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST.
ArticleTitle: "الحصول على المحور الثاني للقيمة للرسم البياني – واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تسترجع واجهة برمجة تطبيقات GetChartSecondValueAxis المحور الثاني للقيمة لرسم بياني.

## واجهة برمجة تطبيقات GetChartSecondValueAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **الأمان والمصادقة**

تُعتبر واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل      | النوع    | الموقع   | الوصف                                              |
|------------------|----------|----------|-----------------------------------------------------|
| name             | string   | path     | اسم ملف Excel.                                     |
| sheetName        | string   | path     | اسم ورقة العمل التي يحتوي عليها الرسم البياني.    |
| chartIndex       | integer  | path     | المؤشر الصفري للرسم البياني.                       |
| folder           | string   | query    | المجلد الذي يُخزَّن فيه الملف.                     |
| storageName      | string   | query    | اسم مساحة التخزين في Aspose Cloud.                 |

**المتطلبات المسبقة**: يجب تزويد رمز وصول JWT صالح تم الحصول عليه عبر تدفق Aspose Cloud OAuth2 في رأس `Authorization` لكل طلب.

يُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondValueAxis) واجهة برمجة تطبيقات قابلة للوصول بشكل عام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يُظهر المثال التالي كيفية إجراء استدعاء إلى واجهة برمجة التطبيقات السحابية باستخدام cURL. جميع نقاط نهاية Aspose Cloud تتطلب استخدام HTTPS.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
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
  "Axis": {
    "AxisId": 1,
    "IsVisible": true,
    "MinimumScale": 0,
    "MaximumScale": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "المحور الثاني للقيمة"
  }
}
```

**حقول الاستجابة**

- **Code** – رمز حالة HTTP لعملية الطلب (مثل `200` للنجاح).  
- **Status** – وصف نصي للحالة (`"OK"` للنجاح).  
- **Axis** – كائن يحتوي على تفاصيل المحور الثاني للقيمة:  
  - **AxisId** – مُعرِّف المحور.  
  - **IsVisible** – قيمة منطقية تُشير إلى ما إذا كان المحور ظاهرًا.  
  - **MinimumScale** – القيمة الدنيا المعروضة على المحور.  
  - **MaximumScale** – القيمة القصوى المعروضة على المحور.  
  - **MajorUnit** – الفاصل بين علامات التجزئة الرئيسية.  
  - **MinorUnit** – الفاصل بين علامات التجزئة الثانوية.  
  - **Title** – نص عنوان المحور.

**استجابات الأخطاء** (غير 200)

- `400 Bad Request` – معاملات غير صالحة أو طلب مُشكَّل بشكل خاطئ.  
- `401 Unauthorized` – رمز JWT مفقود أو غير صالح.  
- `404 Not Found` – الملف أو ورقة العمل أو الرسم البياني المحدّد غير موجود.  
- `500 Internal Server Error` – خطأ غير متوقع في الخادم.

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى SDK التعامل مع التفاصيل من المستوى المنخفض وتركز أنت على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء استدعاءات إلى خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondValueAxis.js" >}}
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