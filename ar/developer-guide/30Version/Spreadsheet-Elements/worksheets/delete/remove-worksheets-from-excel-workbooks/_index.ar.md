---
title: "حذف ورقة عمل"
second_title: "مستند"
linktype: "ورقة عمل واحدة"
type: docs
url: /worksheets/delete-worksheet/
aliases: [/remove-worksheets-from-excel-workbooks/]
keywords: "Aspose.Cells Cloud، حذف ورقة عمل، Excel، Spreadsheet، REST API"
description: "احذف ورقة عمل من ملف عمل Excel باستخدام REST API الخاص بـ Aspose.Cells Cloud. يدعم SDKs لـ C#، Java، PHP، Ruby، Node.js، Python، Perl، Go وcURL."
weight: 20
ArticleTitle: "حذف ورقة عمل – واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية لـ REST بحذف ورقة عمل.  
المتطلبات الأساسية: لاستدعاء هذه الواجهة، يجب أن تقدّم رمز مصادقة JWT صالحًا في رأس **Authorization**، ولديك صلاحيات الوصول إلى موقع التخزين الذي يوجد فيه ملف العمل.

## واجهة برمجة التطبيقات (REST API)

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

*ملاحظة: تستخدم الواجهة الإصدار **v3.0**، وهو الإصدار المستقر الحالي. سيتم الإعلان عن أي تغييرات في الإصدارات مستقبلًا في ملاحظات الإصدار.*

### **مُعلمات الطلب**

| اسم المُعلمة | النوع | الموقع | الوصف |
| ------------ | ------ | -------- | ------------------- |
| name | string | path | اسم المستند. |
| sheetName | string | path | اسم ورقة العمل. |
| folder | string | query | مجلد المستند. |
| storageName | string | query | اسم التخزين. |

ردود HTTP المحتملة:

| رمز الحالة | الوصف |
| ----------- | ----------- |
| 200 OK | تم حذف ورقة العمل بنجاح. |
| 400 Bad Request | مُعلمات طلب غير صالحة. |
| 401 Unauthorized | فشلت المصادقة أو نقص الرمز المميز. |
| 404 Not Found | ملف العمل أو ورقة العمل المحددة غير موجودة. |
| 500 Internal Server Error | خطأ غير متوقع في الخادم. |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheet) واجهة برمجة قابلة للوصول بشكل عام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الرد" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet3" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*يجب إجراء جميع الطلبات عبر بروتوكول HTTPS؛ الواجهة لا تدعم الاتصالات غير المشفرة (TLS).*

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

## عائلة SDK للخدمات السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يتعامل SDK مع التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}