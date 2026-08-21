---
title: "ضبط تلقائي لأعمدة متعددة في ورقة عمل Excel"
second_title: "مستند"
linktitle: "أعمدة"
type: docs
url: /worksheets/autofit/columns/
aliases: [/autofit-multiple-columns-of-worksheet/]
keywords: "Aspose.Cells, ضبط تلقائي للأعمدة, واجهة برمجة تطبيقات Excel, جدول بيانات سحابي, REST"
description: "تعلم كيفية ضبط الأعمدة المتعددة تلقائيًا في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 3.0). يتضمن النقطة النهائية (Endpoint)، المعاملات، مثال cURL، معالجة الأخطاء، ومقتطفات رمزية لـ SDKs مثل C# وJava وPython وما إلى ذلك."
weight: 20
---

تقوم هذه الواجهة البرمجية REST بضبط **أعمدة متعددة** تلقائيًا في ورقة عمل Excel.

## واجهة REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### **معاملات الطلب**

| اسم المعاملة         | النوع     | الموقع   | الوصف                                                                                                                                     |
| ------------------- | --------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| name                | string    | path     | اسم الملف.                                                                                                                                  |
| sheetName           | string    | path     | اسم ورقة العمل.                                                                                                                             |
| firstColumn         | integer   | query    | فهرس العمود الابتدائي.                                                                                                                      |
| lastColumn          | integer   | query    | فهرس العمود النهائي.                                                                                                                        |
| autoFitterOptions\* | object    | body     | خيارات الضبط التلقائي (انظر [خيارات الضبط التلقائي](/cells/auto-fitter-options/)). تشمل: `AutoFitMergedCells`، `IgnoreHidden`، و`OnlyAuto`.    |
| firstRow            | integer   | query    | فهرس الصف الابتدائي للضبط التلقائي (**اختياري**).                                                                                           |
| lastRow             | integer   | query    | فهرس الصف النهائي للضبط التلقائي (**اختياري**).                                                                                             |
| folder              | string    | query    | مسار المجلد في التخزين (**اختياري**).                                                                                                       |
| storageName         | string    | query    | اسم التخزين (**اختياري**).                                                                                                                  |

\*يُعرض اسم المعاملة كرابط إلى الوثائق ذات الصلة.

تعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) على واجهة برمجة تطبيقات عامة قابلة للوصول، وتمكّنك من إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=5&firstColumn=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير، حيث تُعالِج SDK التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الرمز التالية كيفية إجراء المكالمات إلى خدمات Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}