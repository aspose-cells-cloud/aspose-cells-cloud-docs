---
title: "حذف شكل حسب الفهرس على ورقة عمل إكسل"
second_title: "مستند"
linktitle: "حذف"
type: docs
url: /ar/shapes/delete/
aliases: [/ar/delete-a-shape-by-index-inside-the-worksheet/]
keywords: "Aspose.Cells Cloud، حذف شكل، فهرس الشكل، ورقة عمل إكسل، REST API، SDK"
description: "استخدم واجهة Aspose.Cells Cloud REST API لحذف شكل حسب فهرسه على ورقة عمل إكسل. تتوفر الواجهة عبر عدة SDKs (C#، Java، PHP، Ruby، Node.js، Python، Perl، Go)، وتدعم خيارات تخزين متعددة."
weight: 50
---

تقوم هذه الواجهة البرمجية REST بحذف شكل من ورقة عمل إكسل.

## واجهة برمجة التطبيقات REST

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### **مُعلَمات الطلب**

| اسم المُعلَمة | النوع   | الموقع | الوصف                                              |
|--------------|---------|--------|----------------------------------------------------|
| name         | string  | path   | اسم ملف المصنف.                                    |
| sheetName    | string  | path   | اسم ورقة العمل.                                     |
| shapeindex   | integer | path   | فهرس الشكل ضمن مجموعة الأشكال في ورقة العمل.       |
| folder       | string  | query  | المجلد المخزن فيه المصنف.                          |
| storageName  | string  | query  | اسم خدمة التخزين.                                  |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/DeleteWorksheetShape) واجهة برمجة تطبيقات قابلة للوصول العام، وتمكّنك من إجراء تفاعلات REST مباشرةً من خلال متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء نداء إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/1" \
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

يُعد استخدام SDK الطريقة الأسرع لتطوير التطبيقات. فتتولى SDK معالجة التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

يُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}