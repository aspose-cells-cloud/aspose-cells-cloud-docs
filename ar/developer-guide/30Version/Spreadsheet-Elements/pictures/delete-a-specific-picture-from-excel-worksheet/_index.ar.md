---
title: "حذف صورة من ورقة عمل Excel – واجهة Aspose.Cells Cloud API"
second_title: "مستند"
linktitle: "حذف"
type: docs
url: /ar/pictures/delete/
aliases: [  /ar/delete-a-specific-picture-from-excel-worksheet/ ]
keywords: "Aspose.Cells، واجهة Cloud API، حذف صورة، ورقة عمل Excel، REST"
description: "احذف صورة من ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API. تعرّف على نقطة نهاية DELETE، والمعلمات المطلوبة، والمصادقة، وأكواد الأخطاء، ونماذج الكود."
weight: 50
ArticleTitle: "حذف صورة من ورقة عمل Excel – واجهة Aspose.Cells Cloud API"
---

تقوم هذه الواجهة REST بحذف صورة من ورقة عمل Excel.

### **الأمان والمصادقة**

واجهات Aspose.Cells Cloud API آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

## واجهة REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### معلمات الطلب

| اسم المعلمة | النوع | الموقع | مطلوب | الوصف |
|-------------|-------|--------|--------|--------|
| name | string | path | نعم | اسم ملف المصنف. |
| sheetName | string | path | نعم | اسم ورقة العمل التي تحتوي على الصورة. |
| pictureIndex | integer | path | نعم | الفهرس المبدئي (بدون تحديد) للصورة المراد حذفها. |
| folder | string | query | لا | المجلد الذي يُخزّن فيه المصنف. |
| storageName | string | query | لا | اسم خدمة التخزين (اختياري). |

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية إجراء الطلب باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/0" \
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

**رؤوس استجابة نموذجية**

| الرأس | القيمة |
|--------|--------|
| Content-Type | application/json |
| Content-Length | (يتغير) |
| Date | (تاريخ الخادم) |

{{< /tab >}}

{{< /tabs >}}

### معالجة الأخطاء

| رمز HTTP | المعنى | نموذج حمولة الخطأ |
|----------|---------|-------------------|
| 200 | تمت عملية حذف الصورة بنجاح. | `{ "Code": 200, "Status": "OK" }` |
| 400 | طلب غير صالح – معلمات غير صحيحة. | `{ "Code": 400, "Message": "فهرس الصورة غير صالح." }` |
| 401 | غير مُصرّح – رمز مفقود أو غير صالح. | `{ "Code": 401, "Message": "رمز الوصول مفقود أو غير صالح." }` |
| 404 | غير موجود – المصنف أو ورقة العمل أو الصورة غير موجودة. | `{ "Code": 404, "Message": "المورد غير موجود." }` |
| 500 | خطأ داخلي في الخادم. | `{ "Code": 500, "Message": "خطأ غير متوقع في الخادم." }` |

## مجموعة أدوات SDK للسحابة

استخدام SDK هو أسرع طريقة للتطوير. تُدار التفاصيل منخفضة المستوى بواسطة SDK، مما يتيح لك التركيز على مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

توضح الأمثلة التالية كيفية استدعاء خدمات Aspose.Cells عبر واجهة REST باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}