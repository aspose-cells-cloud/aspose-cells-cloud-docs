---
title: "الحصول على تحقق من صحة ورقة عمل باستخدام الفهرس من ورقة عمل إكسل"
second_title: "Document"
linktitle: "الحصول على"
type: docs
url: /validations/get/
aliases: [/get-validation-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, واجهة برمجة تطبيقات التحقق من صحة ورقة العمل, الحصول على التحقق باستخدام الفهرس, واجهة برمجة تطبيقات إكسل عبر REST, Aspose.Cells SDK"
description: "استرجاع التحقق من صحة ورقة عمل باستخدام فهرسه الصفري (zero‑based) من ملف إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0). يتضمن مثالًا باستخدام cURL، ومخطط الاستجابة، وأكواد الأخطاء، وأجزاء أكواد SDK بلغات C# وJava وPython وغيرهم."
weight: 10
---

تقوم هذه الواجهة البرمجية لواجهة برمجة تطبيقات REST باسترجاع التحقق من صحة ورقة العمل باستخدام فهرسه من ورقة عمل إكسل.  
قبل استدعاء نقطة النهاية (endpoint)، يجب الحصول على رمز JWT عبر نقطة النهاية `/connect/token`، ثم تضمينه في رأس الطلب `Authorization` على الشكل `Bearer <jwt token>`.

## واجهة برمجة تطبيقات REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **معلمات الطلب**

| اسم المعلمة    | النوع    | الموقع  | الوصف                                                     |
| --------------- | ------- | -------- | ---------------------------------------------------------- |
| name            | string  | path     | اسم ملف المصنف (workbook).                               |
| sheetName       | string  | path     | اسم ورقة العمل.                                           |
| validationIndex | integer | path     | الفهرس الصفري (zero‑based) للتحقق المراد استرجاعه.       |
| folder          | string  | query    | المجلد الذي يحتوي على المصنف.                            |
| storageName     | string  | query    | اسم خدمة التخزين.                                         |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidation) واجهة برمجة مفتوحة للبرمجة متاحة عمومًا، ويسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية استدعاء الواجهة باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Validation": {
    "AlertStyle": "Stop",
    "AreaList": [
      {
        "EndColumn": 0,
        "EndRow": 0,
        "StartColumn": 0,
        "StartRow": 0
      },
      {
        "EndColumn": 27,
        "EndRow": 0,
        "StartColumn": 26,
        "StartRow": 0
      }
    ],
    "IgnoreBlank": false,
    "InCellDropDown": false,
    "Operator": "None",
    "ShowError": false,
    "ShowInput": false,
    "Type": "AnyValue",
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/Validations/0",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**مخطط الاستجابة**

| الحقل           | النوع    | الوصف                                                                 |
| --------------- | ------- | ---------------------------------------------------------------------- |
| AlertStyle      | string  | أسلوب التنبيه المعروض للمستخدم (Stop, Warning, Information).           |
| AreaList        | array   | مجموعة من نطاقات الخلايا التي يسري عليها التحقق.                      |
| IgnoreBlank     | boolean | إذا كانت `true`، تُتجاهل الخلايا الفارغة أثناء التحقق.                 |
| InCellDropDown  | boolean | إذا كانت `true`، يُعرض قائمة منسدلة داخل الخلية.                      |
| Operator        | string  | عامل المقارنة المستخدم في التحقق (مثل `None`, `Between`).             |
| ShowError       | boolean | يحدد ما إذا كان سيتم عرض رسالة خطأ عند فشل التحقق.                    |
| ShowInput       | boolean | يحدد ما إذا كان سيتم عرض رسالة إدخال عند تحديد الخلية.               |
| Type            | string  | نوع التحقق (مثل `AnyValue`, `WholeNumber`, `Decimal`, إلخ).           |
| link.Href       | string  | عنوان URL المرجعي الذاتي للمورد الخاص بالتحقق.                         |
| link.Rel        | string  | نوع العلاقة (دائمًا `self`).                                           |

**أكواد الأخطاء الممكنة**

| الحالة HTTP | المعنى                                                                   |
| ----------- | ------------------------------------------------------------------------ |
| 200         | تم استرجاع التحقق بنجاح.                                                 |
| 400         | طلب غير صالح – معلمات مفقودة أو غير صحيحة.                              |
| 401         | غير مُصادَق – رمز JWT غير صالح أو مفقود.                                |
| 404         | غير موجود – المصنف أو ورقة العمل أو فهرس التحقق غير موجود.              |
| 500         | خطأ داخلي في الخادم – حالة غير متوقعة.                                 |

## مجموعة أدوات SDK للحوسبة السحابية

استخدام حزمة تطوير البرامج (SDK) هي أسرع طريقة لتطوير تطبيقات متوافقة مع Aspose.Cells Cloud. فحزمة SDK تُجرّدك من التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على منطق أعمالك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم SDK الخاصة بـ Aspose.Cells Cloud.

توضح الأمثلة التالية كيفية استدعاء خدمات Aspose.Cells باستخدام حزم SDK المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}