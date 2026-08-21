---
title: "إلغاء تجميد المقاطع في ورقة عمل Excel"
second_title: "مستند"
linktitle: "إلغاء التجميد"
type: docs
url: /ar/worksheets/panes/unfreeze/
aliases:
  - /unfreeze-panes-in-excel-worksheet/
  - /worksheets/unfreeze-panes/
keywords: "إلغاء تجميد المقاطع، Excel، Aspose.Cells Cloud، REST API، SDK، C#، Java، PHP، Python، Node.js، Go، Swift، Android، Ruby، Perl"
description: "تعرّف على كيفية إزالة المقاطع المُجمَّدة من ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API (النسخة 3.0). يشمل مثالًا باستخدام cURL ومقتطفات كود SDK بلغات C# وJava وPython وما إلى ذلك."
weight: 200
---

يقوم هذا الاستدعاء لواجهة REST API **بإلغاء تجميد** (أي إزالة المقاطع المُجمَّدة) من ورقة عمل Excel.

## واجهة REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

### **مُعَيَّنات الطلب**

| اسم المُعَيَّن | النوع | الموقع | الوصف |
| -------------- | ------ | -------- | ------------------------------------------------- |
| `name`         | string | path     | اسم ملف Excel.                           |
| `sheetName`    | string | path     | اسم ورقة العمل.                            |
| `folder`       | string | query    | مسار المجلد في التخزين حيث يقع الملف. |
| `storageName`  | string | query    | اسم تخزين Aspose Cloud.                 |

_لا توجد مُعَيَّنات استعلام إضافية (مثل الصف، العمود، frozenRows، أو frozenColumns) مطلوبة لعملية إلغاء التجميد._

يعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetFreezePanes) واجهة برمجة تطبيقات متاحة للعامة وتتيح لك إجراء تفاعلات REST مباشرة من خلال متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

## عائلة SDK للسحابة

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يتعامل الـ SDK مع التفاصيل منخفضة المستوى لتمكينك من التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsDeleteWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnfreezePanes-unfreeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-DeleteWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-unfreeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnfreezePanesInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnfreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnfreezePanes-unfreeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnfreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "23052de16f4f1cd75542ce4ae9b3ada8" >}}

{{< /tab >}}

{{< /tabs >}}