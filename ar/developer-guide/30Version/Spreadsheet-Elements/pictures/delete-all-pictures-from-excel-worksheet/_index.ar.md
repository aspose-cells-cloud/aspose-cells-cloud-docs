---
title: "حذف جميع الصور في ورقة عمل Excel"
second_title: "مستند"
linktitle: "مسح"
type: docs
url: /pictures/clear/
aliases: [/delete-all-pictures-from-excel-worksheet/]
keywords: "Aspose.Cells Cloud، Excel، حذف جميع الصور، ورقة عمل، REST API، مسح الصور"
description: "تعرّف على كيفية حذف جميع الصور من ورقة عمل Excel باستخدام Aspose.Cells Cloud REST API مع أمثلة لـ cURL وSDKs."
weight: 60
ArticleTitle: "كيفية حذف جميع الصور في ورقة عمل Excel باستخدام Aspose.Cells Cloud"
---

يقوم هذا الـ REST API بحذف **جميع** الصور في ورقة عمل.

**المتطلبات المسبقة**  
- حساب نشط على Aspose.Cells Cloud مع رمز وصول OAuth 2.0 ساري المفعول.  
- يتطلب إصدار API 3.0 (أو أحدث)، أما الإصدارات الأقدم فهي مُهمَلة.  
- يجب تخزين ملف Excel المستهدف في موقع تخزين مدعوم (افتراضي أو مخصص).

**توافق الإصدار**  
يتبع هذا الـ endpoint مواصفات Cells Cloud 3.0 API. تأكد من أن مكتبات العميل وعناوين URL للطلبات تستهدف `api.aspose.cloud/v3.0`.

## DeleteWorksheetPictures API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة التطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معلمات الطلب**

| اسم المعلمة | النوع   | الموقع | الوصف                                     |
|-------------|---------|--------|--------------------------------------------|
| name        | string  | Path   | اسم ملف Excel.                            |
| sheetName   | string  | Path   | اسم ورقة العمل التي تحتوي على الصور.      |
| folder      | string  | Query  | المجلد الذي يُخزَّن فيه الملف.            |
| storageName | string  | Query  | اسم خدمة التخزين.                          |

### استجابات الخطأ

| رمز HTTP | الوصف                                                                 |
|----------|------------------------------------------------------------------------|
| 401      | غير مُصادَق – نقصان أو عدم صلاحية الرمز.                              |
| 404      | غير موجود – الملف أو ورقة العمل أو فهرس كسر الصفحة المحددة غير موجود. |
| 400      | طلب غير صالح – تركيب جملة الطلب أو المعلمات غير صحيحة.                |
| 500      | خطأ داخلي في الخادم – تم مواجهة شرط غير متوقع.                       |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/DeleteWorksheetPictures) واجهة برمجة تطبيقات قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية استدعاء الـ API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/pictures" \
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

استخدام SDK هو أسرع طريقة للتطوير. يتعامل الـ SDK مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق أعمالك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPictures.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPictures.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPictures.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPictures.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPictures.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPictures.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPictures.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPictures.go" >}}

{{< /tab >}}

{{< /tabs >}}

**ملاحظات:** لا يدعم إجراء DELETE الترقيم (pagination)، ويخضع لقيود معدل الطلبات القياسية لـ Aspose.Cells Cloud API (افتراضيًا 100 طلب في الدقيقة). قم بتعديل منطق العميل وفقًا لذلك.

**انظر أيضًا**:  
- [/pictures/delete/](../delete/) – حذف صورة محددة من ورقة عمل.  
- [/pictures/add/](../add/) – إضافة صورة إلى ورقة عمل.  
---