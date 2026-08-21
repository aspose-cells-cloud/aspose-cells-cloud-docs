---
title: "إظهار أعمدة مخفية في ورقة عمل Excel"
ArticleTitle: "إظهار أعمدة مخفية في ورقة عمل Excel - واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktype: "إظهار"
type: docs
url: /columns/unhide/
aliases:
  [/unhide-columns-in-an-excel-worksheet/, /unhide-columns-in-excel-worksheet/]
keywords: "Aspose.Cells، واجهة برمجة تطبيقات سحابية، إظهار الأعمدة، Excel، REST، SDK"
description: "تعرّف على كيفية استخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API لإظهار الأعمدة المخفية في ورقة عمل Excel. يشمل التفاصيل الكاملة للطلب، مثالًا باستخدام cURL، وأكواد أمثلة للعديد من لغات البرمجة."
weight: 50
---

تقوم هذه الواجهة البرمجية REST بإظهار الأعمدة المخفية في أوراق العمل.

**المتطلبات المسبقة** – جميع نقاط نهاية Aspose.Cells Cloud تتطلب استخدام بروتوكول HTTPS ورمز وصول OAuth 2.0 صالح. تأكد من امتلاكك لرمز وصول وإدراجه في رأس `Authorization` لطلباتك.

## واجهة PostUnhideWorksheetColumns API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/unhide
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة باستخدام رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع    | الموقع | الوصف                                          |
|------------|---------|--------|------------------------------------------------|
| name       | string  | path   | اسم ملف المصنف.                                |
| sheetName  | string  | path   | اسم ورقة العمل.                                |
| startColumn| integer | query  | فهرس العمود الأول المراد معالجته.              |
| totalColumns| integer| query  | عدد الأعمدة المراد معالجتها.                   |
| width      | number  | query  | العرض المطلوب للأعمدة (الافتراضي = 50.0).     |
| folder     | string  | query  | المجلد الذي يحتوي على المستند.                |
| storageName| string  | query  | اسم خدمة التخزين.                              |

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetColumns" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> تُعرّف واجهة برمجة تطبيقات متاحة للعامة وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات ويب Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/unhide?startColumn=1&totalColumns=1&width=15" -H "accept: application/json"
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

**رموز حالة HTTP الشائعة**

| الرمز | الوصف                                          |
|-------|------------------------------------------------|
| 200   | نجاح – تم إظهار الأعمدة بنجاح.                 |
| 400   | طلب غير صالح – معاملات غير صحيحة.             |
| 401   | غير مُصادق – نقص أو فساد في الرمز.             |
| 404   | غير موجود – لم يتم العثور على المصنف أو ورقة العمل. |
| 500   | خطأ داخلي في الخادم – فشل غير متوقع.           |

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يتعامل SDK مع التفاصيل الدقيقة من المستوى المنخفض حتى تتمكن من التركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
---