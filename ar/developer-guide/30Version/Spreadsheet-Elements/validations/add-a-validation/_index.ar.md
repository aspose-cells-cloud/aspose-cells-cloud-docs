---
title: "إضافة تحقق من صحة ورقة عمل إلى ورقة عمل Excel"
second_title: "Document"
linktitle: "Add"
type: docs
url: /ar/validations/add/
keywords: "إضافة تحقق من صحة ورقة عمل، Excel، Aspose.Cells Cloud، REST API، Spreadsheet، Validation rule"
description: "استخدم واجهة Aspose.Cells Cloud REST API لإضافة تحقق من صحة ورقة عمل إلى ملف Excel. توفر SDKs لغات البرمجة التالية: C#، Java، PHP، Ruby، Node.js، Python، Perl، Go، وSwift."
weight: 10
---

تقوم هذه الواجهة البرمجية REST بإضافة تحقق من صحة ورقة عمل إلى ورقة عمل Excel.

## واجهة REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **مُعلَمات الطلب**

| اسم المُعلَمة | النوع | الموقع | الوصف |
| -------------- | ------ | -------- | ---------------------------------------------------------- |
| name | string | path | اسم مستند Excel. |
| sheetName | string | path | اسم ورقة العمل. |
| range | string | query | نطاق الخلايا الذي ينطبق عليه التحقق (مثال: A1:B10). |
| validation | object | body | تعريف قاعدة التحقق. |
| folder | string | query | المجلد الذي يحتوي على المستند. |
| storageName | string | query | اسم خدمة التخزين. |

يُعرِّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/PutWorksheetValidation) واجهة برمجة تطبيقات متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية إجراء مكالمات لواجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X PUT \
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

## عائلة SDK للحوسبة السحابية

يُعد استخدام مكتبة SDK (Software Development Kit) أفضل طريقة لتسريع عملية التطوير. فالمكتبة تُدير التفاصيل من المستوى المنخفض وتسمح لك بالتركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر واجهات برمجة التطبيقات باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}