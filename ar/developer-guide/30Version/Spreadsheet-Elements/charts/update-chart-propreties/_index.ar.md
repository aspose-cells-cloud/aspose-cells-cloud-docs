---
title: "تحديث خصائص الرسم البياني"
type: docs
url: /charts/properties/update/
aliases: [/update-chart-properties/]
weight: 160
keywords: "Aspose.Cells, رسم بياني, تحديث, Excel, REST API, SDK"
description: "تعلم كيفية تحديث خصائص الرسم البياني (النوع، العنوان، الأسطورة، إلخ) في ملف Excel باستخدام Aspose.Cells Cloud REST API (الإصدار 3.0). يتضمن_endpoint_، المعاملات، مثال cURL، وأجزاء أكواد SDK لـ C#، Java، PHP، Ruby، Node.js، Perl، و Go."
ArticleTitle: "تحديث خصائص الرسم البياني – Aspose.Cells Cloud REST API"
---

تقوم هذه الـ REST API بتحديث خصائص الرسم البياني.

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

## واجهة PostWorksheetChart API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### معاملات الطلب

| اسم المعاملة | النوع   | المسار/سلسلة الاستعلام/جسم الطلب | الوصف                                                       |
|--------------|---------|----------------------------------|-------------------------------------------------------------|
| name         | string  | path                             | اسم ملف Excel.                                              |
| sheetName    | string  | path                             | اسم ورقة العمل التي يحتوي عليها الرسم البياني.             |
| chartIndex   | integer | path                             | المؤشر صفر-الأساسي للرسم البياني المراد تحديثه.            |
| chart        | object  | body                             | كائن JSON يُعرّف خصائص الرسم البياني التي يجب تعديلها.     |
| folder       | string  | query                            | المجلد في التخزين حيث يوجد الملف.                           |
| storageName  | string  | query                            | اسم خدمة التخزين.                                           |

### مخطط جسم الطلب

يحتوي كائن **`chart`** على الخصائص التي يمكنك تعديلها. فيما يلي مثال تمثيلي بتنسيق JSON يشمل عدة حقول شائعة الاستخدام:

```json
{
  "Title": {
    "Text": "المبيعات الفصلية"
  },
  "ShowLegend": true,
  "Type": "Line",
  "DataLabels": {
    "ShowValue": true,
    "ShowPercentage": false
  },
  "ChartArea": {
    "BorderColor": "Blue",
    "FillColor": "White"
  }
}
```

> **ملاحظة:** يجب تزويد الحقول التي تحتاج فقط إلى تغييرها. تحتفظ الخصائص المُهملة بقيمها الحالية.

تُعرّف <a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات متاحة علنًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يُظهر المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" \
-d '{"Type": "line"}' \
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

## الاستجابة

ترجع الواجهة كائن JSON يُشير إلى نتيجة العملية. وتُظهر التحديثات الناجحة ما يلي:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**رموز حالة النجاح**

| حالة HTTP | الوصف                                             |
|-----------|---------------------------------------------------|
| 200       | OK – تم تحديث خصائص الرسم البياني بنجاح.         |

**رؤوس الاستجابة**

| الرأس | الوصف                                                     |
|-------|-----------------------------------------------------------|
| `Content-Type` | `application/json` – يشير إلى أن جسم الاستجابة مُنسّق بتنسيق JSON. |
| `X-RequestId`  | مُعرّف فريد للطلب (مفيد في حل المشاكل).                   |

تشمل استجابات الخطأ المحتملة ما يلي:

| حالة HTTP | الوصف                                               |
|-----------|-----------------------------------------------------|
| 400       | Bad Request – معاملات أو جسم غير صالح.              |
| 401       | Unauthorized – رمز مفقود أو غير صالح.               |
| 404       | Not Found – ملف أو ورقة عمل أو رسم بياني غير موجود.  |
| 500       | Internal Server Error                               |

للحصول على عمليات أخرى مرتبطة بالرسوم البيانية، راجع المواضيع ذات الصلة مثل [تحديث عنوان الرسم البياني](/charts/title/update/) و[تحديث أسطورة الرسم البياني](/charts/legend/update/).

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}