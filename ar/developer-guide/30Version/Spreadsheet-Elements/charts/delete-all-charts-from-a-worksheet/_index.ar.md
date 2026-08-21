---
title: "حذف جميع المخططات من ورقة عمل"
type: docs
url: /ar/charts/clear/
aliases: [  /ar/delete-all-charts-from-a-worksheet/ ]
weight: 30
keywords: "Aspose.Cells، السحابة، حذف، جميع المخططات، ورقة العمل، واجهة برمجة تطبيقات REST، DELETE، SDK"
description: "تعرّف على كيفية حذف جميع المخططات الموجودة في ورقة عمل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API (الإصدار 3.0). تتضمن النهاية النهائية (endpoint)، المُعاملات، مثال cURL، مقاطع كود SDK، خطوات المصادقة، ومعالجة الأخطاء."
ArticleTitle: "حذف جميع المخططات من ورقة عمل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية REST بحذف جميع المخططات من ورقة العمل المحددة.

**الخلفية** – يُعد حذف جميع المخططات من ورقة العمل مفيدًا عندما تحتاج إلى إعادة ضبط التصميم البصري لورقة العمل، أو استبدال التصورات البصرية القديمة، أو إعداد ملف عمل لإعادة الاستخدام دون الاحتفاظ ببيانات المخططات السابقة.

قبل استدعاء الواجهة البرمجية، تأكد من استيفاء المتطلبات الأساسية التالية:

- توفر رمز JWT صالح للمصادقة.
- وجود ملف العمل في موقع ومسار التخزين المحددين.
- استخدام إصدار الواجهة البرمجية **v3.0**.

## واجهة DeleteWorksheetClearCharts البرمجية

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud مصادقة مبنية على <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">رمز JWT</a>، وهي آمنة.

### مُعاملات الطلب

| اسم المُعامل | النوع | الموقع | الوصف |
| ------------ | ------ | -------- | ------------------------------------ |
| name | string | path | اسم ملف العمل. |
| sheetName | string | path | اسم ورقة العمل. |
| folder | string | query | المجلد الذي يُخزّن فيه ملف العمل. |
| storageName | string | query | اسم مساحة التخزين. |

**رؤوس الطلب**

| الرأس | الوصف |
|---------------|---------------------------------|
| Authorization | Bearer `<jwt token>` |
| Accept | `application/json` |
| Content-Type | `application/json` (لا يوجد جسم للطلب) |

**جسم الطلب**

لا تتطلب عملية DELETE **أي** جسم طلب.

**الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**كود حالات HTTP**

| الكود | المعنى | الوصف |
|------|-----------------------------|--------------------------------------------------|
| 200 | OK (تمت العملية بنجاح) | تم تطبيق الحذف بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request (طلب غير صالح) | مُعاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized (غير مصرّح) | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large (حجم البيانات كبير جدًا) | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500 | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم. |

*أمثلة على استجابات الأخطاء*

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "مُعامل غير صالح: يُطلب 'sheetName'."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "فشلت المصادقة. رمز JWT غير صالح."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "تجاوز حجم بيانات الطلب الحد الأقصى المسموح به."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "حدث خطأ غير متوقع في الخادم."
}
```

## كيفية استخدام واجهة DeleteWorksheetClearCharts البرمجية مع SDKs

### مواصفات واجهة DeleteWorksheetClearCharts البرمجية

تعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetClearCharts) واجهة برمجة تطبيقات متاحة علنًا، وتمكّنك من إجراء تفاعلات REST مباشرة من خلال متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts" \
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

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

يُعد استخدام SDK أفضل طريقة لتسريع عملية التطوير عند الحاجة إلى **حذف جميع المخططات** من ورقة عمل. تهتم SDK بتفاصيل المستوى المنخفض، وتتيح لك التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على القائمة الكاملة لـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح مقاطع الكود التالية كيفية إجراء المكالمات إلى خدمات Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteAllCharts-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetClearCharts-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-clear_the_charts-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteAllChartsFromAWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteAllCharts-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteAllCharts-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1775c5a8985efa819486b7ede2c34bfc" >}}

{{< /tab >}}

{{< /tabs >}}
---