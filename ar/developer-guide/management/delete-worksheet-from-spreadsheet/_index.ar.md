---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud لحذف ورقة عمل Excel - إزالة الأوراق من ملفات العمل برمجيًا"
second_title: "مستند"
ArticleTitle: "كيف تحذف ورقات عمل من ملفات Excel - إزالة الأوراق من ملفات العمل"
linktitle: "حذف ورقة عمل من جدول بيانات"
type: docs
url: /ar/delete-worksheet-from-spreadsheet/
keywords: "Aspose Cells، واجهة برمجة تطبيقات حذف ورقة العمل، إزالة ورقة Excel، جدول بيانات سحابي، واجهة برمجة تطبيقات REST"
description: "تعرّف على كيفية حذف ورقة عمل من ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. يتضمن نقطة النهاية (endpoint)، والمتغيرات المطلوبة، وأمثلة باستخدام cURL، وأمثلة باستخدام مكتبات SDK."
weight: 100
---

احذف ورقات عمل من ملفات Excel برمجيًا باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. أزل ورقة واحدة أو عدة أوراق بأمان، ونظّف هيكل ملف العمل، وقم بأتمتة تحسين الجداول البيانات. واجهة برمجة تطبيقات REST مُصممة لإدارة ملفات Excel وسير عمل معالجة المستندات على مستوى المؤسسات.

## واجهة برمجة تطبيقات حذف ورقة عمل من جدول بيانات

### واجهة برمجة التطبيقات عبر الويب

```http
PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName={sheetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}"
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة قائمة على رمز JWT</a>.

### المتغيرات المطلوبة في الطلب:

| اسم المتغير | النوع | الموقع | الوصف                                                                                                                                                                                                        |
| :----------- | :----- | :------ | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet  | ملف   | FormData | **إجباري.** ملف Excel الأصلي (مثل: .xlsx أو .xls) الذي سيتم إزالة ورقة عمل منه.                                                                                                                           |
| sheetName    | نص (String) | Query  | **إجباري.** الاسم الدقيق لورقة العمل المراد حذفها (مثل: `Sheet1`، `TemporaryData`).                                                                                                                        |
| outPath      | نص (String) | Query  | **اختياري.** مسار المجلد المستهدف في التخزين السحابي حيث سيتم حفظ ملف العمل المعدّل. إذا تُرك فارغًا أو أُعطي قيمة `null`، سيُحفظ الملف في نفس الموقع الأصلي أو مسار افتراضي.                               |
| outStorageName | نص (String) | Query  | **اختياري.** مُعرّف خدمة التخزين السحابي (مثل: `ProjectStorage`) التي سيتم كتابة الملف الناتج فيها. إذا لم يُحدّد، سيُستخدم التخزين الافتراضي.                                                                  |
| region       | نص (String) | Query  | **اختياري.** إعداد المنطقة (مثل: `it-IT`) الذي قد يؤثر على الصيغ أو البيانات الخاصة بالمنطقة أثناء عملية الحفظ.                                                                                          |
| password     | نص (String) | Query  | **اختياري.** كلمة المرور المطلوبة لفتح وتعديل جدول بيانات مُحمي بكلمة مرور. اتركه فارغًا إذا لم يكن الملف مشفرًا.                                                                                          |

### الاستجابة

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**رموز حالة HTTP**

| الرمز | المعنى                   | الوصف                                                         |
| ---- | ------------------------ | -------------------------------------------------------------- |
| 200  | نجح (OK)                 | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صحيح (Bad Request) | مُعطيات مفقودة أو غير صحيحة (مثل: نوع ملف غير مدعوم).        |
| 401  | غير مُصادق عليه (Unauthorized) | رمز JWT غير صحيح أو مفقود.                                     |
| 413  | حجم البيانات كبير جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح.                         |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                      |

## أين يجب استخدام واجهة برمجة تطبيقات حذف ورقة عمل من جدول بيانات؟

- **المعالجة اللاحقة للتبليغات تلقائيًا** – بعد إنشاء التقرير المالي النهائي، أزل ورقات العمل الوسيطة المستخدمة في الحسابات المؤقتة تلقائيًا، ليبقى الملف النهائي نظيفًا واحترافيًا.
- **التنظيف الديناميكي لملفات القوالب** – عند إنشاء المستخدمين لمستندات مخصصة (مثل: عروض الأسعار) من قالب، احذف الصفحات الاختيارية التي لم تُحدّد.
- **تحسين أرشفة سير العمل** – بعد انتهاء المشروع أو التدقيق، احذف ورقات العمل المسودة أو المستخدمة في التعاون، واحتفظ بالإصدار النهائي فقط للأرشفة والامتثال.

## لماذا يجب استخدام واجهة برمجة تطبيقات حذف ورقة عمل من جدول بيانات؟

- **مُصممة للمطورين** – توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، مما يمكّن من تطوير سريع ويقدّم وثائق شاملة.
- **خفض تكاليف العمالة** – يلغي الحاجة إلى موظفين مخصصين لدمج المستندات يدويًا.
- **دفع مقابل الاستخدام فقط** – لا حاجة لاستثمار أولي؛ تدفع فقط مقابل طلبات واجهة برمجة التطبيقات التي تستخدمها فعليًا.
- **لا تكاليف صيانة** – لا خوادم لصيانتها، ولا تحديثات برمجية، ولا قلق حول التوافق.

## كيف تستخدم واجهة برمجة تطبيقات حذف ورقة عمل من جدول بيانات باستخدام مكتبات SDK

### مُستند واجهة برمجة تطبيقات حذف ورقة عمل من جدول بيانات

يُعرّف <a href="https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet" rel="noopener noreferrer">مستند واجهة برمجة تطبيقات حذف ورقة عمل من جدول بيانات</a> واجهة برمجة تطبيقات قابلة للوصول علنًا، مما يمكّنك من إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (مشفرة بـ Base64)",
  "contentType": "نوع MIME",
  "fileDownloadName": "اسم ملف اختياري"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أسرع طريقة للتطوير، لأنها تُجرّدك من تفاصيل المستوى المنخفض وتُمكّنك من حذف ورقة عمل باستخدام كود محدود. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK متنوعة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}