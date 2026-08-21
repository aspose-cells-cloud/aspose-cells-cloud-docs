---
title: "إضافة مخطط إلى ورقة عمل"
type: docs
url: /ar/charts/add/
aliases: [  /ar/add-a-chart-in-a-worksheet/ ]
weight: 20
description: "تعرّف على كيفية إضافة مخطط إلى ورقة عمل إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud الإصدار 3.0. تتضمن الواجهة، المَعلمات، مثالًا باستخدام cURL، ومقتطفات من كود SDKs."
keywords:
  - "إضافة مخطط Aspose.Cells"
  - "واجهة برمجة تطبيقات إضافة مخطط Aspose.Cells"
  - "واجهة مخططات REST"
  - "أمثلة SDKs لـ Aspose.Cells"
ArticleTitle: "إضافة مخطط إلى ورقة عمل – دليل واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة REST بإضافة مخطط جديد إلى ورقة عمل.

**المتطلبات المسبقة**  
قبل استدعاء هذه العملية، احصل على رمز وصول JWT صالح، وتأكد من أن ملف المصنف المستهدف مخزن في المجلد المحدد أو موقع التخزين.

## PutWorksheetAddChart API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### مَعلمات الطلب

| اسم المعلمة            | النوع   | الموقع | الوصف                                                                                                                                                                              |
| ----------------------- | ------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                | نص      | المسار | اسم ملف المصنف.                                                                                                                                                                     |
| **sheetName**           | نص      | المسار | اسم ورقة العمل.                                                                                                                                                                     |
| **chartType**           | نص      | الاستعلام | نوع المخطط (انظر خاصية **Type** في مورد المخطط). تشمل أنواع المخططات المدعومة: **Bar** (عمودي)، **Column** (عمود)، **Line** (خط)، **Pie** (دائري)، **Scatter** (نقطي)، **Area** (منطقة)، **Doughnut** (حلقي)، **Radar** (رادار)، إلخ. |
| **upperLeftRow**        | عدد صحيح | الاستعلام | فهرس الصف الأيسر العلوي لمنطقة المخطط (العد يبدأ من الصفر).                                                                                                                        |
| **upperLeftColumn**     | عدد صحيح | الاستعلام | فهرس العمود الأيسر العلوي لمنطقة المخطط (العد يبدأ من الصفر).                                                                                                                      |
| **lowerRightRow**       | عدد صحيح | الاستعلام | فهرس الصف الأيمن السفلي لمنطقة المخطط (العد يبدأ من الصفر).                                                                                                                        |
| **lowerRightColumn**    | عدد صحيح | الاستعلام | فهرس العمود الأيمن السفلي لمنطقة المخطط (العد يبدأ من الصفر).                                                                                                                      |
| **area**                | نص      | الاستعلام | النطاق الذي يوفّر القيم المراد تمثيلها (مثلًا: `A1:B5`).                                                                                                                           |
| **isVertical**          | منطقي   | الاستعلام | يُشير إلى ما إذا كانت توجيه المخطط عموديًا.                                                                                                                                       |
| **categoryData**        | نص      | الاستعلام | نطاق قيم محور الفئات (مثلًا: `D1:E10`).                                                                                                                                           |
| **isAutoGetSerialName** | منطقي   | الاستعلام | إذا كانت القيمة **true**، تُولّد أسماء المتسلسلات تلقائيًا.                                                                                                                        |
| **title**               | نص      | الاستعلام | عنوان المخطط.                                                                                                                                                                       |
| **folder**              | نص      | الاستعلام | المجلد الذي يحتوي على ملف المصنف.                                                                                                                                                  |
| **storageName**         | نص      | الاستعلام | اسم موقع التخزين.                                                                                                                                                                   |
| **dataLabels**          | منطقي   | الاستعلام | إظهار تسميات البيانات عند القيمة **true**.                                                                                                                                         |
| **dataLabelsPosition**  | نص      | الاستعلام | موقع تسميات البيانات (مثلًا: `Above`).                                                                                                                                             |
| **pivotTableSheet**     | نص      | الاستعلام | اسم ورقة العمل التي تحتوي على الجدول المحوري.                                                                                                                                      |
| **pivotTableName**      | نص      | الاستعلام | اسم الجدول المحوري.                                                                                                                                                                 |

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**رموز حالات HTTP**

| الرمز | المعنى                     | الوصف                                                                 |
|------|-----------------------------|------------------------------------------------------------------------|
| 200  | ناجح (OK)                  | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.         |
| 400  | طلب غير صالح (Bad Request) | مَعلمات مفقودة أو غير صالحة (مثلًا: نوع ملف غير مدعوم).             |
| 401  | غير مصادق عليه (Unauthorized) | رمز JWT غير صالح أو مفقود.                                          |
| 413  | حجم البيانات كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به.                           |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                            |

## كيفية استخدام PutWorksheetAddChart API باستخدام SDKs

### مواصفات PutWorksheetAddChart API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart) واجهة برمجة تطبيقات قابلة للوصول بشكل عام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء مكالمة إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
# لا يتطلب هذا الإجراء جسم طلب
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فالـ SDK يُجرّد التفاصيل من المستوى المنخفض ويسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات لخدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}