---
title: "حذف التحقق من صحة ورقة العمل – Aspose.Cells Cloud"
second_title: "مستند"
linktitle: "حذف"
type: docs
url: /validations/delete/
keywords: "حذف، التحقق من صحة ورقة العمل، Aspose.Cells Cloud، واجهة برمجة تطبيقات Excel"
description: "تعرّف على كيفية حذف التحقق من صحة ورقة عمل من ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API. يشمل ذلك نقطة النهاية، المُعلَمات، تفاصيل المصادقة، مثال باستخدام cURL، معالجة الأخطاء، ومقتطفات كود SDK."
weight: 10
---

تقوم هذه الواجهة البرمجية لـ REST بحذف التحقق من صحة ورقة العمل بناءً على فهرسه الصفر-based داخل ورقة عمل Excel.

## واجهة برمجة تطبيقات REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **مُعلَمات الطلب**

| اسم المُعلَمة   | النوع    | الموقع | الوصف                                                |
|------------------|----------|--------|------------------------------------------------------|
| name             | string   | path   | اسم ملف Excel.                                       |
| sheetName        | string   | path   | اسم ورقة العمل.                                      |
| validationIndex  | integer  | path   | الفهرس الصفر-based للتحقق من الصحة المراد حذفه.       |
| folder           | string   | query  | المجلد الذي يحتوي على المستند.                       |
| storageName      | string   | query  | اسم خدمة التخزين.                                    |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) واجهة برمجة تطبيقات عامة قابلة للوصول وتتيح لك إجراء تفاعلات REST مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL لاستدعاء خدمة Aspose.Cells الويبية. يُظهر المثال التالي كيفية حذف تحقق من الصحة باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
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

**رموز حالات HTTP**

| الكود | المعنى                      | الوصف                                                       |
|-------|-----------------------------|--------------------------------------------------------------|
| 200   | OK                          | تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.    |
| 400   | Bad Request                 | مُعلَمات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم).        |
| 401   | Unauthorized                | رمز JWT غير صالح أو مفقود.                                   |
| 413   | Payload Too Large           | حجم الملف المرفوع يتجاوز الحد المسموح.                        |
| 500   | Internal Server Error       | خطأ غير متوقع في الخادم.                                      |

## عائلة SDK للسحابة

استخدام SDK هو أسرع طريقة لدمج هذه العملية في تطبيقك. تُدار تفاصيل المستوى المنخفض بواسطة SDKs، مما يتيح لك التركيز على المنطق التجاري. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية حذف التحقق من صحة ورقة العمل باستخدام SDKs متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}