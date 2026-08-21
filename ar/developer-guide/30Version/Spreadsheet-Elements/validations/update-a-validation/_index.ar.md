---
title: "تحديث تحقق من صحة ورقة عمل في ورقة عمل Excel"
second_title: "مستند"
linktitle: "تحديث"
type: docs
url: /validations/update/
keywords: "Aspose.Cells Cloud, تحديث تحقق من صحة Excel, واجهة برمجة تطبيقات REST, تحقق من صحة ورقة العمل, واجهة برمجة تطبيقات Excel"
description: "كيفية تحديث تحقق من صحة ورقة عمل في ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST، مع أمثلة cURL ومقاطع كود SDK لعدة لغات برمجة."
weight: 10
ArticleTitle: "تحديث تحقق من صحة ورقة العمل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية REST بتحديث تحقق من صحة ورقة العمل حسب فهرسه في ورقة عمل Excel.

قبل استدعاء هذه النقطة النهائية، احصل على رمز وصول JWT مع النطاقات المناسبة (مثل `Cells.ReadWrite`). ضع الرمز في رأس `Authorization` كما هو موضح في الأمثلة.

## واجهة برمجة تطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **مُعلَمات الطلب**

| اسم المُعلَمة     | النوع    | الموقع | الوصف                                                           |
| ------------------ | -------- | ------ | ---------------------------------------------------------------- |
| name               | string   | path   | اسم ملف المصنف.                                                 |
| sheetName          | string   | path   | اسم ورقة العمل التي تحتوي على التحقق من الصحة.                  |
| validationIndex    | integer  | path   | الفهرس المُعدّ من الصفر للتحقق من الصحة المراد تحديثه.           |
| validation         | object   | body   | كائن JSON يُعرّف إعدادات التحقق من الصحة المُحدَّثة.             |
| folder             | string   | query  | المجلد في مساحة التخزين السحابية حيث يوجد المصنف.              |
| storageName        | string   | query  | اسم خدمة التخزين (في حال استخدام تخزين مخصص).                 |

<a href="https://apireference.aspose.cloud/cells/#/WorksheetValidations/PostWorksheetValidation" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> تُعرّف واجهة برمجة تطبيقات مُتاحة للعامة وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL لاستدعاء خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء مكالمة إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ "AlertStyle":"Warning" }'
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

**رموز حالة HTTP الممكنة**

| الرمز | المعنى                                    | الوصف |
|------|-------------------------------------------|-------|
| 200  | OK (تم بنجاح)                             | تم تحديث التحقق من الصحة بنجاح. |
| 400  | Bad Request (طلب غير صالح)               | الطلب غير منسق أو مفقود مُعلَمات إلزامية. |
| 401  | Unauthorized (غير مخوّل)                  | رمز JWT غير صالح أو مفقود. |
| 403  | Forbidden (محظور)                         | لا يحتوي الرمز على نطاقات كافية. |
| 404  | Not Found (غير موجود)                    | المصنف أو ورقة العمل أو فهرس التحقق من الصحة المحدّد غير موجود. |
| 500  | Internal Server Error (خطأ داخلي في الخادم) | حدث خطأ غير متوقع في الخادم. |

لمزيد من التفاصيل حول معالجة الأخطاء، راجع <a href="https://apireference.aspose.cloud/cells/#/Errors" target="_blank" rel="noopener noreferrer">توثيق أخطاء Aspose.Cells Cloud</a>.

قد ترغب أيضًا في استكشاف عمليات ذات صلة مثل إضافة تحقق من صحة جديد أو حذف تحقق موجود:

- [إضافة تحقق من صحة لورقة عمل](https://docs.aspose.cloud/cells/validations/add/)
- [حذف تحقق من صحة لورقة عمل](https://docs.aspose.cloud/cells/validations/delete/)

## عائلة SDK السحابية

استخدام SDK هو أسرع طريقة لتطوير البرمجيات. يُجرّدك SDK من التفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق أعمالك. يُرجى مراجعة <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

تُظهر مقاطع الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}