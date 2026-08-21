---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud – إضافة عنوان مخطط في ورقة عمل إكسل"
type: docs
url: /ar/chart/title/add/
aliases: [  /ar/set-chart-title-in-excel-worksheet/ ]
weight: 30
keywords: "Aspose.Cells Cloud، واجهة برمجة تطبيقات عنوان المخطط، عنوان مخطط إكسل، واجهة برمجة التطبيقات REST، أمثلة لواجهات برمجة التطبيقات (SDK)"
description: "تعلّم كيفية إضافة عنوان مخطط أو جعل عنوان موجود مرئيًا في ورقة عمل إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. تتضمن أمثلة لـ cURL وواجهات برمجة التطبيقات (SDK)، والمعلمات المطلوبة، وخطوات المصادقة، ومعالجة الأخطاء."
---

يضيف عنوان مخطط أو يجعل العنوان الحالي مرئيًا.

## واجهة برمجة تطبيقات PutWorksheetChartTitle

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات الطلب

| اسم المعلمة | النوع    | الموقع | الوصف                              |
|------------|---------|--------|-------------------------------------|
| name       | نص (string) | مسار (path) | اسم ملف المصنف.                     |
| sheetName  | نص (string) | مسار (path) | اسم ورقة العمل.                     |
| chartIndex | عدد صحيح (integer) | مسار (path) | فهرس المخطط.                        |
| title      | نص (string) | جسم الطلب (body) | نص عنوان المخطط.                    |
| folder     | نص (string) | استعلام (query) | المجلد الذي يحتوي على المصنف.      |
| storageName| نص (string) | استعلام (query) | اسم وحدة التخزين.                   |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartTitle) واجهة برمجة تطبيقات متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يُظهر المثال التالي كيفية إجراء استدعاء لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -d '{"Text":"Sales Chart"}' \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

**استجابات الأخطاء**

| رمز HTTP | محتوى الاستجابة المثال                                                                 | الوصف                                                     |
|----------|----------------------------------------------------------------------------------------|------------------------------------------------------------|
| 400      | `{ "Code": "400", "Message": "Invalid request payload." }`                            | جسم الطلب معطّل أو تُركت حقول مطلوبة غير مُدخلة.          |
| 401      | `{ "Code": "401", "Message": "Authentication failed. Invalid or expired JWT token." }` | رمزBearer مفقود أو غير صالح أو منتهٍ.                     |
| 404      | `{ "Code": "404", "Message": "Workbook, worksheet, or chart not found." }`            | المورد المحدد غير موجود.                                  |
| 500      | `{ "Code": "500", "Message": "Internal server error." }`                              | حدث خطأ غير متوقع في الخادم.                              |

## عائلة واجهات برمجة التطبيقات (SDK) السحابية

استخدام واجهات برمجة التطبيقات (SDK) هو أسرع طريقة للتطوير. فواجهات برمجة التطبيقات (SDK) تُجرّدك من التفاصيل منخفضة المستوى، مما يمكّنك من التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على قائمة كاملة بواجهات برمجة تطبيقات Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات تطوير مختلفة (SDKs):

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-SetChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetChartTitle.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-SetChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-SetChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "728d523e11f8751f5f601bafb04ab86f" >}}

{{< /tab >}}

{{< /tabs >}}