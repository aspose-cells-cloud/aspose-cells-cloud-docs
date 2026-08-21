---
title: "فرز بيانات النطاق في ورقة عمل Excel"
second_title: "Document"
linktitle: "فرز"
type: docs
url: /worksheets/sort-data/
aliases: [/sort-worksheet-data/]
keywords: "Aspose.Cells Cloud, Excel sort API, worksheet range sorting, REST API, dataSorter"
description: "فرز نطاق معيّن في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API. يشمل ذلك عنوان النهاية، المَعلمات المطلوبة، خطوات المصادقة، معالجة الأخطاء، وأمثلة على SDKs."
weight: 20
---

تقوم واجهة برمجة التطبيقات (REST API) بفرز البيانات داخل نطاق مُحدّد في ورقة عمل Excel.

## واجهة برمجة التطبيقات (REST API)

```shell
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort
```

### مَعلمات الطلب

| اسم المعلمة | النوع   | الموقع | مطلوبة | الوصف                                                           |
|------------|--------|--------|--------|------------------------------------------------------------------|
| name       | string | path   | نعم    | اسم المصنف.                                                     |
| sheetName  | string | path   | نعم    | اسم ورقة العمل.                                                 |
| cellArea   | string | query  | نعم    | نطاق الخلايا المراد فرزه (مثل `A5:A10`).                       |
| dataSorter | object | body   | نعم    | كائن JSON يُعرّف إعدادات الفرز (انظر المخطط أدناه).            |
| folder     | string | query  | لا     | المجلد الذي يحتوي على المصنف.                                  |
| storageName| string | query  | لا     | اسم وحدة التخزين التي يوجد فيها المصنف.                        |

**مخطط كائن `dataSorter`** – يجب أن يحتوي الجسم على كائن JSON يحتوي على الخصائص التالية:

- `CaseSensitive` _(boolean, مطلوب)_ – يحدّد ما إذا كان الفرز حسّاسًا لحالة الأحرف (كبير/صغير).
- `HasHeaders` _(boolean, مطلوب)_ – يشير إلى ما إذا كان النطاق يحتوي على صف رئيسي (Header).
- `KeyList` _(array, مطلوب)_ – مجموعة مفاتيح الفرز. يحتوي كل كائن مفتاح على:
  - `Key` _(integer)_ – مؤشر العمود (بدءًا من الصفر).
  - `SortOrder` _(string)_ – `"ascending"` أو `"descending"`.
- `SortLeftToRight` _(boolean, مطلوب)_ – إذا كانت قيمته `true`، فيتم الفرز من اليسار إلى اليمين؛ وإلا من الأعلى إلى الأسفل.
- (اختياري) يمكن أيضًا توفير خصائص إضافية مثل `CaseOrder`، `SortLeftToRight` وفقًا لمواصفات OpenAPI.

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetRangeSort) واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية إجراء استدعاء إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```shell
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/sort?cellArea=A5:A10" \
  -X POST \
  -d '{"CaseSensitive":false,"HasHeaders":false,"KeyList":[{"Key":0,"SortOrder":"descending"}],"SortLeftToRight":false}' \
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

**معالجة الأخطاء** – يمكن أن تُرجع الواجهة رموز أخطاء HTTP قياسية. من بين الاستجابات الشائعة:

| الحالة (HTTP) | الرمز | الرسالة                                               |
|--------------|------|--------------------------------------------------------|
| 400          | 400  | طلب غير صالح – مَعلمات مفقودة أو غير صحيحة.            |
| 401          | 401  | غير مُصادَق – رمز JWT غير صالح أو مفقود.                |
| 404          | 404  | غير موجود – المصنف أو ورقة العمل غير موجودين.           |
| 500          | 500  | خطأ داخلي في الخادم.                                   |

يكون هيكل جسم الاستجابة في حالات الخطأ على النحو التالي: `{ "Code": <status>, "Message": "<description>", "Status": "Error" }`.

## عائلة SDK للحوسبة السحابية

استخدام SDK هو أسرع طريقة لتطوير التطبيقات. يتعامل SDK مع التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات Aspose.Cells عبر الويب باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostWorksheetRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostWorksheetRangeSort-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-sort_worksheet_range-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SortWorkSheetData.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-SortWorksheetData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-SortWorksheetData-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48dd9dae5e2188a64e2284bb12b9201b" >}}

{{< /tab >}}

{{< /tabs >}}