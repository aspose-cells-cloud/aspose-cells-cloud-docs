---
title: "إلغاء تجميع الصفوف في ورقة عمل Excel"
second_title: "مستند"
linktitle: "إلغاء التجميع"
type: docs
url: /rows/ungroup/
aliases: [/ungroup-rows-in-excel-worksheet/]
keywords: "إلغاء تجميع الصفوف، Excel، Aspose.Cells Cloud، REST API، SDK، جدول بيانات"
description: "تعلم كيفية إلغاء تجميع الصفوف في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API وSDKs للغات البرمجة المختلفة."
weight: 70
---

تقوم هذه الواجهة البرمجية REST بإلغاء تجميع الصفوف في ورقة عمل Excel.

## واجهة برمجة التطبيقات REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/ungroup
```

### **معاملات الطلب**

| اسم المعامل | النوع    | الموقع | الوصف                                                                 |
|-------------|----------|--------|------------------------------------------------------------------------|
| name        | string   | path   | اسم ملف العمل (Workbook).                                              |
| sheetName   | string   | path   | اسم ورقة العمل.                                                        |
| firstIndex  | integer  | query  | الفهرس الصفر-based للصف الأول المراد إلغاء تجميعه.                    |
| lastIndex   | integer  | query  | الفهرس الصفر-based للصف الأخير المراد إلغاء تجميعه.                   |
| isAll       | boolean  | query  | إذا كانت القيمة **true**، سيتم إلغاء تجميع جميع الصفوف في النطاق المحدد. |
| folder      | string   | query  | المجلد الذي يحتوي على ملف العمل.                                      |
| storageName | string   | query  | اسم وحدة التخزين التي يقع فيها ملف العمل.                             |

تعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetRows) على واجهة برمجة تطبيقات متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/ungroup?firstIndex=1&lastIndex=5&isAll=true" \
 -X POST \
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

يُعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يتعامل SDK مع التفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

يوضح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUngroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUngroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUngroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUngroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUngroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUngroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUngroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUngroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}