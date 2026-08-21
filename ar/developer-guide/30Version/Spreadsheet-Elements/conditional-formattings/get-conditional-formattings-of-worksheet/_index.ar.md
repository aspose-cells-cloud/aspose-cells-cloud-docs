---
title: "الحصول على قواعد التنسيق الشرطي"
type: docs
url: /ar/conditional-formattings/get-all/
aliases: [  /ar/get-conditional-formattings-of-worksheet/ ]
keywords: "Aspose.Cells Cloud، واجهة برمجة التطبيقات REST، إكسل، التنسيق الشرطي، ورقة العمل، واجهة برمجة تطبيقات التنسيق الشرطي"
description: "استرجاع جميع قواعد التنسيق الشرطي المطبقة على ورقة عمل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يتضمن بناء جملة الطلب، خطوات المصادقة، المعلمات، أمثلة موجزة للاستجابة، والتعامل مع الأخطاء."
weight: 20
---

تسترجع هذه الواجهة البرمجية REST قواعد التنسيق الشرطي المطبقة على ورقة عمل.

## الأمان والمصادقة
تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة برمجة التطبيقات REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### معلمات الطلب

| اسم المعلمة | النوع | الموقع | الوصف |
|--------------|--------|--------|--------------------------------------------------|
| name | سلسلة نصية | المسار | اسم ملف إكسل. |
| sheetName | سلسلة نصية | المسار | اسم ورقة العمل. |
| folder | سلسلة نصية | استعلام | مسار المجلد الذي يُخزَّن فيه الملف. |
| storageName | سلسلة نصية | استعلام | اسم خدمة التخزين (اختياري). |

### استجابات الأخطاء

| رمز HTTP | السبب | مثال على جسم الاستجابة |
|----------|--------|---------------------------------------------|
| **400** | طلب غير صالح – معلمات مفقودة أو غير صالحة. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | غير مصرّح به – رمز JWT مفقود أو غير صالح. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | غير موجود – ملف العمل أو ورقة العمل غير موجودين. | `{ "Code":"404", "Message":"File not found." }` |
| **500** | خطأ داخلي في الخادم – فشل غير متوقع في الخادم. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

تُعرِّف <a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings" target="_blank">مواصفات OpenAPI</a> واجهة برمجة تطبيقات متاحة علنًا وتتيح لك إجراء تفاعلات REST مباشرةً من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر `cURL` للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمة إلى واجهة برمجة التطبيقات السحابية باستخدام `cURL`.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "OK",
  "ConditionalFormattings": {
    "Count": 1,
    "ConditionalFormattingList": [
      {
        "sqref": "A1:B10",
        "FormatConditions": [
          {
            "Priority": 1,
            "Type": "CellValue",
            "Operator": "GreaterThan",
            "Formula1": "100",
            "Style": {
              "Font": {
                "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                "IsBold": true
              }
            }
          }
        ]
      }
    ]
  }
}
```

_يعرض المثال أعلاه فقط أبرز الحقول ذات الصلة للحفاظ على اختصار حمل البيانات._

**معلمات الاستجابة**

| المعلمة | النوع | الوصف |
|---------|--------|--------|
| Status | سلسلة نصية | حالة نتيجة الطلب (مثل **OK**). |
| ConditionalFormattings | كائن | حاوية لبيانات التنسيق الشرطي. |
| ConditionalFormattings.Count | عدد صحيح | عدد قواعد التنسيق الشرطي المسترجعة. |
| ConditionalFormattings.ConditionalFormattingList | مصفوفة | قائمة كائنات التنسيق الشرطي. |
| ConditionalFormattingList[].sqref | سلسلة نصية | نطاق الخلايا الذي يُطبَّق عليه التنسيق (مثل **A1:B10**). |
| ConditionalFormattingList[].FormatConditions | مصفوفة | مجموعة كائنات شروط التنسيق الخاصة بالنطاق. |
| FormatConditions[].Priority | عدد صحيح | أولوية تقييم الشرط. |
| FormatConditions[].Type | سلسلة نصية | نوع الشرط (مثل **CellValue**). |
| FormatConditions[].Operator | سلسلة نصية | العامل المستخدم في الشرط (مثل **GreaterThan**). |
| FormatConditions[].Formula1 | سلسلة نصية | الصيغة أو القيمة الأولى للشرط. |
| FormatConditions[].Style | كائن | التنسيق المطبّق عند استيفاء الشرط. |
| Style.Font.Color | كائن | تعريف اللون RGBA لخط النص. |
| Style.Font.IsBold | منطقي | يُشير إلى ما إذا كان الخط عريضًا أم لا. |

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|------|------------------------|--------------------------------------------------|
| 200 | OK | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500 | Internal Server Error | خطأ غير متوقع في الخادم. |

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فهو يتعامل مع التفاصيل منخفضة المستوى، مما يمكّنك من التركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-GetWorksheetConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-get-conditional-formatting-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-get_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-GetWorksheetConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-GetWorksheetConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b2a10009556f14d1f939a8433925c5f6" >}}

{{< /tab >}}

{{< /tabs >}}