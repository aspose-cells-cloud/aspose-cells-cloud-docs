---
title: "إعداد صفحة ورقة العمل"
second_title: "الوثيقة"
linktitle: "إعداد الصفحة"
type: docs
url: /page-setup/
keywords: "Aspose.Cells, pageSetup, worksheet, print settings, margins, orientation, paper size, header, footer, scaling"
description: "تعرّف على كيفية تهيئة تنسيق طباعة ورقة عمل Excel باستخدام كائن PageSetup في Aspose.Cells Cloud. يشمل قائمة الخصائص، والقيم الافتراضية، وال نطاقات، وأمثلة على الأكواد بلغات C# وJava وPython."
weight: 20
ArticleTitle: "إعداد صفحة ورقة العمل – تهيئة تنسيق الطباعة باستخدام Aspose.Cells Cloud"
---

# **PageSetup**

إعدادات صفحة طباعة Excel

## نظرة عامة

يُعرّف كائن **PageSetup** خيارات تنسيق الطباعة لورقة عمل Excel، مثل الهوامش، والتوجيه، والتصغير، والرؤوس، والتذييلات، وغير ذلك من إعدادات الطباعة. يتيح ضبط هذه الخصائص للمطورين إنشاء أوراق عمل قابلة للطباعة تطابق المظهر والتقسيم المرغوبين.

يُظهر المقتطف التالي مثالًا قصيرًا بلغة C# لكيفية ضبط خصائص شائعة لإعداد الصفحة باستخدام SDK الخاص بـ Aspose.Cells Cloud:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// تهيئة عميل واجهة API (استبدل بمعلومات الاعتماد الخاصة بك)
var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// تعريف إعدادات PageSetup
var pageSetup = new PageSetup()
{
    Orientation = "Landscape",
    PaperSize = "A4",
    CenterHorizontally = true,
    CenterVertically = true,
    Zoom = 100
};

// تطبيق الإعدادات على ورقة العمل الأولى في المصنف
apiInstance.PutWorksheetPageSetup("Sample.xlsx", "Sheet1", pageSetup);
```

يضبط هذا المقتطف توجيه الورقة على أنه أفقي (Landscape)، ويستخدم حجم الورقة A4، ويُوسط المحتوى أفقيًا ورأسيًا، ويُطبّق عامل تكبير بنسبة 100%.

## الخصائص

| اسم الخصائص        | نوع الخصائص | يمكن أن تكون فارغة | للقراءة فقط | القيمة الافتراضية | الوصف |
| ------------------ | ----------- | ----------------- | ---------- | ---------------- | ----- |
| BlackAndWhite      | bool        | false             | false      | false            | يطبع ورقة العمل باللونين الأسود والأبيض فقط. |
| BottomMargin       | float       | true              | false      | 2.54 سم          | حجم الهامش السفلي بالسنتيمترات. |
| CenterHorizontally | bool        | false             | false      | false            | يُوسط الورقة أفقيًا عند الطباعة. |
| CenterVertically   | bool        | false             | false      | false            | يُوسط الورقة رأسيًا عند الطباعة. |
| FirstPageNumber    | int         | true              | false      | 1                | رقم الصفحة الأول المستخدم عند طباعة الورقة. |
| FitToPagesTall     | int         | false             | false      | 1                | عدد الصفحات عموديًا التي سيتم تصغير حجم الورقة لملءها. |
| FitToPagesWide     | int         | false             | false      | 1                | عدد الصفحات أفقيًا التي سيتم تصغير حجم الورقة لملءها. |
| FooterMargin       | float       | true              | false      | 2.54 سم          | المسافة من أسفل الصفحة إلى التذييل، بالسنتيمترات. |
| HeaderMargin       | float       | true              | false      | 2.54 سم          | المسافة من أعلى الصفحة إلى الرأس، بالسنتيمترات. |
| IsAutoFirstPageNumber | bool     | false             | false      | false            | يُعيّن رقم الصفحة الأول تلقائيًا. |
| IsHFAlignMargins   | bool        | false             | false      | true             | إذا كانت القيمة true، تتطابق هوامش الرأس والتذييل مع هوامش الصفحة. |
| IsHFDiffFirst      | bool        | false             | false      | false            | يشير إلى أن الرأس أو التذييل في الصفحة الأولى يختلف عن باقي الصفحات. |
| IsHFDiffOddEven    | bool        | false             | false      | false            | يشير إلى أن الرأس أو التذييل في الصفحات الفردية يختلف عن الصفحات الزوجية. |
| IsHFScaleWithDoc   | bool        | false             | false      | false            | يُصغّر الرأس والتذييل مع الوثيقة (في إصدارات Excel 2007 وما بعدها). |
| IsPercentScale     | bool        | false             | false      | true             | عندما تكون القيمة false، تتحكم `FitToPagesWide` و`FitToPagesTall` في التصغير. |
| LeftMargin         | float       | true              | false      | 2.54 سم          | حجم الهامش الأيسر بالسنتيمترات. |
| Order              | string      | true              | false      | "DownThenOver"   | الترتيب الذي يستخدمه Excel لترقيم الصفحات عند طباعة ورقة عمل كبيرة. |
| Orientation        | string      | false             | false      | "Portrait"       | توجيه الصفحة: **Landscape** أو **Portrait**. |
| PaperSize          | string      | true              | false      | "A4"             | حجم الورقة المستخدم للطباعة. |
| PrintArea          | string      | true              | false      | (لا شيء)         | نطاق الخلايا المراد طباعتها (مثال: `"A1:D20"`). |
| PrintComments      | string      | true              | false      | "NoComments"     | طريقة طباعة التعليقات مع الورقة. |
| PrintCopies        | int         | true              | false      | 1                | عدد النسخ المطلوب طباعتها. |
| PrintDraft         | bool        | false             | false      | false            | يطبع ورقة العمل في الوضع المسود (بدون رسومات). |
| PrintErrors        | string      | true              | false      | "Display"        | نوع خطأ الطباعة المعروض. |
| PrintGridlines     | bool        | false             | false      | false            | يطبع خطوط الشبكة للخلايا. |
| PrintHeadings      | bool        | false             | false      | false            | يطبع عناوين الصفوف والأعمدة. |
| PrintQuality       | int         | true              | false      | 600              | إعداد جودة الطباعة (نقطة في البوصة). |
| PrintTitleColumns  | string      | true              | false      | (لا شيء)         | الأعمدة المكررة على الجانب الأيسر من كل صفحة مطبوعة. |
| PrintTitleRows     | string      | true              | false      | (لا شيء)         | الصفوف المكررة في أعلى كل صفحة مطبوعة. |
| RightMargin        | float       | true              | false      | 2.54 سم          | حجم الهامش الأيمن بالسنتيمترات. |
| TopMargin          | float       | true              | false      | 2.54 سم          | حجم الهامش العلوي بالسنتيمترات. |
| Zoom               | int         | false             | false      | 100              | عامل التصغير كنسبة مئوية (10–400%). |
| Header             | object      | true              | false      | (لا شيء)         | إعدادات الرأس. |
| Footer             | object      | true              | false      | (لا شيء)         | إعدادات التذييل. |

## الكائنات ذات الصلة

- **Header** – يهيّئ الرأس لورقة العمل.  
- **Footer** – يهيّئ التذييل لورقة العمل.  
- **PrintOptions** – إعدادات إضافية مرتبطة بالطباعة مثل فواصل الصفحات ومنطقة الطباعة.  
---