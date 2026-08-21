---
title: "حذف جميع الأشكال في ورقة عمل Excel"
ArticleTitle: "حذف جميع الأشكال في ورقة عمل Excel – واجهة Aspose.Cells Cloud API"
second_title: "وثيقة"
linktitle: "مسح"
type: docs
url: /ar/shapes/clear/
aliases: [  /ar/delete-all-shapes-inside-the-worksheet/ ]
keywords: "Aspose.Cells Cloud، حذف جميع الأشكال، ورقة عمل Excel، واجهة REST API، حزمة تطوير البرامج (SDK)، cURL، .NET، Java، PHP، Ruby، Node.js، Python، Perl، Go، Android، Swift"
description: "احذف جميع الأشكال من ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API. تتوفر هذه العملية عبر cURL ومجموعة واسعة من حزم تطوير البرامج (SDKs) (C#، Java، PHP، Ruby، Node.js، Python، Perl، Go، Android، Swift)."
weight: 40
---

تحذف هذه الواجهة البرمجية (REST API) جميع الأشكال الموجودة في ورقة عمل Excel.

**المتطلبات المسبقة:** يلزم وجود رمز وصول JWT صالح. احصل عليه عبر تدفق Aspose Cloud OAuth2 وأدجه في رأس `Authorization` كما هو موضح في المثال التالي.

## DeleteWorksheetShapes API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **الأمان والمصادقة**

تتطلب واجهات Aspose.Cells Cloud API <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **مُعاملات الطلب**

| اسم المُعامل      | النوع   | الموقع   | الوصف                                             |
| ---------------- | ------- | -------- | -------------------------------------------------- |
| name             | string  | path     | اسم ملف Excel.                                     |
| sheetName        | string  | path     | اسم ورقة العمل.                                    |
| folder           | string  | query    | المجلد الذي يحتوي على المستند.                     |
| storageName      | string  | query    | اسم وحدة التخزين التي يوجد فيها المستند.            |

يُعرّف <a href="https://apireference.aspose.cloud/cells/#/Shapes/DeleteWorksheetShapes" rel="noopener noreferrer">مواصفة OpenAPI</a> واجهة برمجة تطبيقات عامة قابلة للوصول، وتمكّنك من إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء استدعاء إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes" \
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

## عائلة حزم تطوير البرامج (SDKs) للسحابة

استخدام حزمة تطوير البرامج (SDK) هو أفضل طريقة لتسريع عملية التطوير. فتتولى حزمة التطوير إدارة التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام حزم تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}