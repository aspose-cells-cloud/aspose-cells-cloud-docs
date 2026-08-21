---
title: "الحصول على جميع التحققّات من أوراق العمل في ورقة عمل إكسل"
second_title: "مستند"
linktitle: "الحصول على الكل"
type: docs
url: /ar/validations/get-all/
keywords: "Aspose.Cells Cloud, إكسل, تحققّات من أوراق العمل, واجهة برمجة التطبيقات REST, الحصول على جميع التحققّات, مكتبات تطوير البرمجيات (SDKs)"
description: "استرجاع جميع تحققّات أوراق العمل من ورقة عمل إكسل باستخدام واجهة برمجة التطبيقات REST لـ Aspose.Cells Cloud. يدعم ذلك العديد من مكتبات التطوير (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) للتكامل السريع."
weight: 10
---

تتيح لك تحققّات أوراق العمل تعريف قواعد تقيّد نوع البيانات أو نطاقها الذي يمكن إدخاله في الخلايا. تُستخدم هذه التحققّات عادةً لضمان سلامة البيانات، مثل تقييد الإدخالات إلى قائمة من القيم أو تواريخ ضمن نطاق محدّد أو قيود عددية.

تسترجع هذه الواجهة برمجية (REST API) جميع تحققّات أوراق العمل في ورقة عمل إكسل.

## واجهة برمجة التطبيقات REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **مُعاملات الطلب**

| اسم المُعامل      | النوع   | الموقع  | الوصف                                      |
|------------------|---------|---------|---------------------------------------------|
| name             | string  | path    | اسم مستند إكسل.                            |
| sheetName        | string  | path    | اسم ورقة العمل.                             |
| folder           | string  | query   | مسار المجلد الذي يُخزّن فيه المستند.        |
| storageName      | string  | query   | اسم خدمة التخزين.                           |

**رموز حالة الاستجابة**

| الرمز | الوصف                                      |
|-------|---------------------------------------------|
| 200   | نجح الطلب – قائمة بالتحققّات               |
| 401   | غير مصرّح – رمز JWT غير صالح أو مفقود     |
| 404   | غير موجود – المستند أو ورقة العمل مفقودة  |
| 500   | خطأ داخلي في الخادم                         |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidations) واجهة برمجة تفاعلية متاحة عمومًا، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells Cloud. **الشرط المسبق:** يجب تضمين رمز JWT صالح في رأس `Authorization`.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "validations": [
    {
      "name": "Validation1",
      "type": "WholeNumber",
      "operator": "Between",
      "formula1": "1",
      "formula2": "100",
      "showErrorMessage": true,
      "errorMessage": "يجب أن تكون القيمة بين 1 و 100."
    },
    {
      "name": "Validation2",
      "type": "List",
      "formula1": "\"Option1,Option2,Option3\"",
      "showErrorMessage": true,
      "errorMessage": "اختر قيمة من القائمة."
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة مكتبات تطوير البرمجيات (SDK) للسحابة

استخدام مكتبة تطوير البرمجيات (SDK) هو أفضل طريقة لتسريع عملية التطوير. فتتولى المكتبة معالجة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات تطوير متعددة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}