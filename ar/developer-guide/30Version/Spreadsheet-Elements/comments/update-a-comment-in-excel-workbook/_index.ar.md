---
title: "تحديث تعليق خلية في ورقة عمل"
type: docs
url: /comments/update/
aliases: [/update-a-comment-in-excel-workbook/]
keywords: "Aspose.Cells Cloud, REST API, Excel, ورقة عمل, تعليق خلية, تحديث تعليق ورقة العمل, كائن التعليق"
description: "استخدم واجهة Aspose.Cells Cloud REST API لتحديث تعليق خلية في ورقة عمل ضمن ملف Excel، بما في ذلك تفاصيل الطلب، رموز الاستجابة، وأمثلة لSDKs."
weight: 30
ArticleTitle: "تحديث تعليق خلية في ورقة العمل – واجهة Aspose.Cells Cloud API"
---

تقوم هذه الواجهة REST بتحديث تعليق على خلية في ورقة عمل. استخدم هذه النقطة النهائية لتحديث **تعليق ورقة عمل** في ملف Excel.

**المتطلبات المسبقة:**
- يجب تضمين رمز وصول OAuth/JWT صالح في رأس `Authorization`.
- يجب تخزين ملف Workbook في موقع داعم لخدمة التخزين السحابي (حدد `folder` واختياريًا `storageName`).

## واجهة PostWorksheetComment

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **الأمان والمصادقة**

تُعتبر واجهات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع   | الموقع | الوصف                                                                |
|-------------|---------|--------|-----------------------------------------------------------------------|
| name        | string  | path   | اسم مستند Excel.                                                     |
| sheetName   | string  | path   | اسم ورقة العمل التي تحتوي على الخلية.                                |
| cellName    | string  | path   | عنوان الخلية (مثل **A1**).                                           |
| comment     | object  | body   | كائن **Comment** يُعرّف التعليق المراد إضافته أو تحديثه.             |
| folder      | string  | query  | المجلد الذي يتم فيه تخزين المستند.                                  |
| storageName | string  | query  | اسم خدمة التخزين.                                                    |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment) واجهة برمجة تطبيقات متاحة علنًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء مكالمة إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "a1",
        "Author": "test",
        "HtmlNote": "string",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10
      }'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

رموز حالات الاستجابة المحتملة:

| الرمز | الوصف                                             |
|-------|----------------------------------------------------|
| 200   | تم تحديث التعليق بنجاح.                          |
| 400   | طلب غير صالح – معاملات مفقودة أو غير صحيحة.     |
| 401   | غير مصرّح به – فشلت المصادقة.                     |
| 404   | غير موجود – ملف Workbook أو ورقة العمل أو التعليق غير موجود. |
| 500   | خطأ داخلي في الخادم.                             |

**ملاحظات / نصائح:**
- أقصى طول للتعليق هو 1024 حرفًا.
- الأحرف المدعومة هي UTF‑8؛ يُفضَّل تجنّب الأحرف التحكمية.

## عائلة SDK السحابية

استخدام SDK هو أسرع طريقة لتطوير التطبيقات مع Aspose.Cells Cloud. يتعامل SDK مع التفاصيل منخفضة المستوى، مما يمكّنك من التركيز على مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر الأمثلة التالية كيفية استدعاء خدمات Aspose.Cells عبر واجهات SDK المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetComment.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetComment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetComment.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetComment.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetComment.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetComment.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetComment.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetComment.go" >}}

{{< /tab >}}

{{< /tabs >}}

العمليات ذات الصلة:
- [الحصول على تعليق ورقة العمل](/comments/get/)
- [إضافة تعليق ورقة عمل](/comments/add/)
- [حذف تعليق ورقة العمل](/comments/delete/)