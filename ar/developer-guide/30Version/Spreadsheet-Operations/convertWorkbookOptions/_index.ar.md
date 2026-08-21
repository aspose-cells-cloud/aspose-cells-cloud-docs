---
title: "خيارات تحويل مصنف"
second_title: "المستند"
linktitle: "خيارات تحويل مصنف"
type: docs
url: /ar/convert-workbook-options/
keywords: "Aspose.Cells, ConvertWorkbookOptions, تحويل Excel, PDF, CSV, API"
description: "خيارات تحويل مصنف – قم بتهيئة تحويل مصنفات Excel إلى تنسيقات مثل PDF وCSV وHTML وغيرها باستخدام واجهة برمجة التطبيقات (API) الخاصة بـ Aspose.Cells Cloud."
weight: 79
ArticleTitle: "خيارات تحويل مصنف – واجهة برمجة التطبيقات (API) الخاصة بـ Aspose.Cells Cloud"
---

# خصائص ConvertWorkbookOptions

**إصدار واجهة برمجة التطبيقات:** 23.12 (2024‑03)

تُستخدم `ConvertWorkbookOptions` كنموذج طلب تُرسله واجهة برمجة التطبيقات (API) لتحويل ملفات Excel في Aspose.Cells Cloud لتحديد كيفية تحويل مصنف Excel إلى تنسيق آخر (مثل PDF أو CSV أو HTML، إلخ). وتضم هذه النموذج معلومات ملف المصدر والتنسيق الهدف وإعدادات الصفحة وخيارات الحفظ الخاصة بالتنسيق.

| الاسم                               | النوع        | الوصف                                                                                                   | الملاحظات |
| ----------------------------------- | ------------ | ------------------------------------------------------------------------------------------------------------- | --------- |
| **DataSource**                      | **Object**  | مصدر ملف البيانات: `CloudFileSystem` أو `RequestFiles` أو `HttpUri`.                                            |           |
| **[FileInfo](/cells/file-info/)**   | **Object**  | يصف اسم الملف وحجمه ومحتواه المشفر بترميز Base64.                                                   |           |
| **[PageSetup](/cells/page-setup/)** | **Object**  | خصائص إعداد الصفحة مثل الهوامش والتوجيه ونسبة التكبير/التصغير.                                              |           |
| **SaveOptions**                     | **Object**  | حاوية لكائنات خيارات الحفظ الخاصة بالتنسيق (مثل `PdfSaveOptions` أو `HtmlSaveOptions`).                |           |
| **ConvertFormat**                   | **string**  | تنسيق الملف الهدف (مثل **PDF** أو **CSV** أو **HTML** أو **XLSX** أو **TIFF**، إلخ).                              |           |
| **CheckExcelRestriction**           | **boolean** | تحديد ما إذا كان يجب تطبيق القيود الخاصة بـ Excel (كحد أقصى لعدد الصفوف أو الأعمدة أو طول اسم الورقة، إلخ). |           |

**المتطلبات الأساسية**

- احصل على رمز وصول OAuth 2.0 صالح لـ Aspose.Cells Cloud.  
- تأكد من إمكانية الوصول إلى ملف المصدر عبر أحد أنواع `DataSource` المدعومة.

**مثال سريع**

```json
{
  "DataSource": {
    "FileInfo": {
      "FileName": "Sample.xlsx",
      "FileContent": "<base64‑encoded‑content>"
    }
  },
  "ConvertFormat": "pdf",
  "SaveOptions": {
    "PdfSaveOptions": {
      "CompressImages": true,
      "ImageQuality": 90
    }
  }
}
```

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d @request.json \
     -o Sample.pdf
```

**تفاصيل طلب واجهة برمجة التطبيقات**

يتم تنفيذ عملية التحويل باستخدام طلب **POST** إلى النقطة النهائية التالية:

```
https://api.aspose.cloud/v3.0/cells/convert
```

الرؤوس المطلوبة:

| الرأس                | القيمة                              |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer {access_token}`            |
| `Content-Type`        | `application/json`                |

يجب أن يحتوي نص الطلب على تمثيل JSON للكائن `ConvertWorkbookOptions` (انظر المثال أعلاه). وجميع الخصائص اختيارية ما لم تُطلب بواسطة `ConvertFormat` المحدد.

**استجابة واجهة برمجة التطبيقات**

يُعيد التحويل الناجح كود الحالة **HTTP 200 OK** (أو **202 Accepted** للمعالجة غير المتزامنة) مع تدفق الملف المحول في جسم الاستجابة. وعند تدفق الاستجابة، يحتوي رأس `Content-Disposition` على اسم الملف المقترح.

مثال على استجابة JSON لطلب غير متزامن:

```json
{
  "JobId": "a1b2c3d4e5",
  "Status": "InProgress",
  "ResultUrl": "https://api.aspose.cloud/v3.0/cells/jobs/a1b2c3d4e5/result"
}
```

**كود الحالة**

| الكود | المعنى                                 |
|-------|------------------------------------------|
| 200   | اكتمل التحويل؛ تم إرجاع الملف.     |
| 202   | تم قبول التحويل؛ يمكن الحصول على النتيجة لاحقًا. |
| 400   | طلب غير صالح – معلمات مفقودة أو غير صحيحة. |
| 401   | غير مصرح به – رمز وصول غير صالح أو مفقود. |
| 403   | ممنوع – صلاحيات غير كافية.   |
| 500   | خطأ داخلي في الخادم.                   |

**ملاحظات / قيود**

- تُطبّق علامة `CheckExcelRestriction` قيود Excel مثل الحد الأقصى لعدد الصفوف (1,048,576) والأعمدة (16,384).  
- لا تدعم جميع تنسيقات الوجهة كل خاصية من خصائص `SaveOptions`؛ وتُتجاهل الخيارات غير المدعومة.  
- عند استخدام `HttpUri` كمصدر بيانات، يجب أن يكون عنوان URL قابلاً للوصول إليه علنًا دون مصادقة.  
- تمت إضافة معلومات طريقة واجهة برمجة التطبيقات ونقطة النهاية لتحسين وضوح المطورين وتقليل أخطاء التكامل.  

## خصائص FileSource

| اسم الخاصية  | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                                               |
| -------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------------------- |
| FileSourceType | String        | true     | false    |               | يشير إلى نوع المصدر (`CloudFileSystem` أو `RequestFiles` أو `HttpUri`). |
| FilePath       | String        | true     | false    |               | مسار موقع الملف.                                                       |

## خصائص DbfSaveOptions

| اسم الخاصية             | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ExportAsString            | Boolean       | true     | false    |               | عند **true**، يُصدِر القيم الرقمية كنصوص.  |
| SaveFormat                | String        | true     | false    |               | مُعرّف التنسيق لملفات DBF.               |
| CachedFileFolder          | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.            |
| ClearData                 | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                |
| CreateDirectory           | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا. |
| EnableHttpCompression     | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.         |
| RefreshChartCache         | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.         |
| SortNames                 | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.            |
| MergeAreas                | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.               |
| SortExternalNames         | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.   |

## خصائص DifSaveOptions

| اسم الخاصية             | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SaveFormat                | String        | true     | false    |               | مُعرّف التنسيق لملفات DIF.               |
| CachedFileFolder          | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.            |
| ClearData                 | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                |
| CreateDirectory           | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا. |
| EnableHttpCompression     | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.         |
| RefreshChartCache         | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.         |
| SortNames                 | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.            |
| MergeAreas                | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.               |
| SortExternalNames         | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.   |

## خصائص DocxSaveOptions

| اسم الخاصية                     | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | الخط المستخدم عند عدم توفر خط المصدر.          |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | يتحقق مما إذا تم تطبيق خط الافتراضي للمصنف.  |
| CheckFontCompatibility            | Boolean       | true     | false    |               | يتحقق من توافق الخط مع تنسيق الوجهة.   |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | يتحكم في استبدال الخطوط على مستوى الأحرف.           |
| OnePagePerSheet                   | Boolean       | true     | false    |               | يجبر كل ورقة على الانتقال إلى صفحة منفصلة.               |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | يجعل جميع أعمدة الورقة تتناسب مع صفحة واحدة.            |
| IgnoreError                       | Boolean       | true     | false    |               | يتجاهل الأخطاء غير الحرجة أثناء التحويل.        |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | يولّد صفحة فارغة إذا لم يكن هناك ما يُعرض. |
| PageIndex                         | Integer       | true     | false    |               | فهرس الصفحة الأولى المطلوب تصديرها.                    |
| PageCount                         | Integer       | true     | false    |               | عدد الصفحات المطلوب تصديرها.                            |
| PrintingPageType                  | String        | true     | false    |               | يحدد نوع الصفحة للطباعة.                 |
| GridlineType                      | String        | true     | false    |               | يحدد طريقة عرض خطوط الشبكة.                |
| TextCrossType                     | String        | true     | false    |               | يعرّف نوع العرض المتعدد للنصوص.            |
| DefaultEditLanguage               | String        | true     | false    |               | اللغة الافتراضية لتحرير النصوص.                    |
| EmfRenderSetting                  | String        | true     | false    |               | إعدادات عرض EMF.                           |
| MergeAreas                        | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.                  |
| SortExternalNames                 | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.       |
| SaveFormat                        | String        | true     | false    |               | مُعرّف التنسيق لملفات DOCX.                 |
| CachedFileFolder                  | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.               |
| ClearData                         | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                   |
| CreateDirectory                   | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا.    |
| EnableHttpCompression             | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.           |
| RefreshChartCache                 | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.           |
| SortNames                         | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                   |
| ValidateMergedAreas               | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.              |
| CheckExcelRestriction             | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.    |
| EncryptDocumentProperties          | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.      |

## خصائص HtmlSaveOptions

| اسم الخاصية                   | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                          |
| ------------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportPageHeaders               | Boolean       | true     | false    |               | يتضمن رؤوس الصفحات في إخراج HTML.            |
| ExportPageFooters               | Boolean       | true     | false    |               | يتضمن تذييلات الصفحات في إخراج HTML.            |
| ExportRowColumnHeadings         | Boolean       | true     | false    |               | يصدِر رؤوس الصفوف والأعمدة.                     |
| ShowAllSheets                   | Boolean       | true     | false    |               | يُظهر جميع أوراق العمل في ملف HTML واحد.          |
| ImageOptions                    | Class         | true     | false    |               | إعدادات تحكم في عرض الصور.               |
| SaveAsSingleFile                | Boolean       | true     | false    |               | يحفظ المصنف كاملاً في ملف HTML واحد.          |
| ExportHiddenWorksheet           | Boolean       | true     | false    |               | يتضمن أوراق العمل المخفية في التصدير.            |
| ExportGridLines                 | Boolean       | true     | false    |               | يُظهر خطوط الشبكة في إخراج HTML.               |
| PresentationPreference          | Boolean       | true     | false    |               | يُحسّن HTML لوضع العرض التقديمي.                |
| CellCssPrefix                   | String        | true     | false    |               | البادئة المُضافة إلى أسماء فئات CSS المولّدة للخلايا. |
| TableCssId                      | String        | true     | false    |               | سمة ID للجدول المولّد في HTML.           |
| IsFullPathLink                  | Boolean       | true     | false    |               | يولّد روابط وصلات كاملة للموارد.        |
| ExportWorksheetCSSSeparately    | Boolean       | true     | false    |               | يضع CSS لكل ورقة عمل في ملف منفصل.      |
| ExportSimilarBorderStyle        | Boolean       | true     | false    |               | يدمج أنماط الحدود المتشابهة لتقليل حجم CSS.     |
| MergeEmptyTdForcely             | Boolean       | true     | false    |               | يجبر دمج عناصر `<td>` الفارغة.             |
| ExportCellCoordinate            | Boolean       | true     | false    |               | يتضمن إحداثيات الخلايا (مثل A1) في HTML.    |
| ExportExtraHeadings             | Boolean       | true     | false    |               | يضيف صفوف/أعمدة إضافية للعناوين عند الحاجة.       |
| ExportHeadings                  | Boolean       | true     | false    |               | يصدِر رؤوس الصفوف والأعمدة.                     |
| ExportFormula                   | Boolean       | true     | false    |               | يظهر الصيغ بدلًا من القيم المحسوبة.         |
| AddTooltipText                  | Boolean       | true     | false    |               | يضيف تلميحات تحتوي على تعليقات الخلايا.                   |
| ExportBogusRowData              | Boolean       | true     | false    |               | يتضمن صفوفًا وهمية للبيانات الفارغة.            |
| ExcludeUnusedStyles             | Boolean       | true     | false    |               | يزيل أنماط CSS غير المستخدمة.                |
| ExportDocumentProperties        | Boolean       | true     | false    |               | يكتب خصائص المستند على مستوى المستند إلى وسوم HTML meta.  |
| ExportWorksheetProperties       | Boolean       | true     | false    |               | يكتب خصائص ورقة العمل على مستوى HTML.           |
| ExportWorkbookProperties        | Boolean       | true     | false    |               | يكتب خصائص المصنف على مستوى HTML.            |
| ExportFrameScriptsAndProperties | Boolean       | true     | false    |               | يتضمن السكريبتات والخصائص الخاصة بالإطارات.          |
| AttachedFilesDirectory          | String        | true     | false    |               | مسار دليل الملفات المرفقة.                   |
| AttachedFilesUrlPrefix          | String        | true     | false    |               | بادئة عنوان URL للملفات المرفقة.                       |
| Encoding                        | String        | true     | false    |               | ترميز الأحرف لملف HTML.                |
| ExportActiveWorksheetOnly       | Boolean       | true     | false    |               | يصدِر ورقة العمل النشطة فقط.                   |
| ExportChartImageFormat          | String        | true     | false    |               | تنسيق الصورة المستخدم للمخططات المُضمّنة.               |
| ExportImagesAsBase64            | Boolean       | true     | false    |               | يرمّز الصور كسلاسل Base64.                    |
| HiddenColDisplayType            | String        | true     | false    |               | طريقة عرض الأعمدة المخفية.                    |
| HiddenRowDisplayType            | String        | true     | false    |               | طريقة عرض الصفوف المخفية.                       |
| HtmlCrossStringType             | String        | true     | false    |               | يحدد كيفية عرض البيانات متعددة السلاسل.        |
| IsExpImageToTempDir             | Boolean       | true     | false    |               | يصدِر الصور إلى دليل مؤقت.             |
| PageTitle                       | String        | true     | false    |               | العنوان المستخدم للصفحة HTML المولّدة.              |
| ParseHtmlTagInCell              | Boolean       | true     | false    |               | يحلّل وسوم HTML الموجودة في قيم الخلايا.             |
| CellNameAttribute               | String        | true     | false    |               | اسم السمة التي تحتوي على مرجع الخلية.        |
| SaveFormat                      | String        | true     | false    |               | مُعرّف التنسيق لملفات HTML.                |
| CachedFileFolder                | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.              |
| ClearData                       | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                  |
| CreateDirectory                 | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا.   |
| EnableHttpCompression           | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.           |
| RefreshChartCache               | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.           |
| SortNames                       | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                   |
| ValidateMergedAreas             | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.              |
| MergeAreas                      | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.                 |
| SortExternalNames               | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                     |
| CheckExcelRestriction           | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.    |
| UpdateSmartArt                  | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.      |
| EncryptDocumentProperties       | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.     |

## خصائص ImageSaveOptions

| اسم الخاصية             | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ChartImageType            | String        | true     | false    |               | تنسيق الصورة المستخدم لعرض المخططات.             |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | الاسم المُسنَد إلى الصور المُضمّنة في إخراج SVG.    |
| HorizontalResolution      | Integer       | true     | false    |               | الدقة الأفقية (DPI) للصورة المصدرة.              |
| ImageFormat               | String        | true     | false    |               | تنسيق الصورة الهدف (PNG أو JPG، إلخ).              |
| IsCellAutoFit             | Boolean       | true     | false    |               | يضبط محتويات الخلية تلقائيًا لتناسب حجم الصورة.         |
| OnePagePerSheet           | Boolean       | true     | false    |               | يعرض كل ورقة عمل في صفحة منفصلة.         |
| OnlyArea                  | Boolean       | true     | false    |               | يصدِر المنطقة المحددة فقط من ورقة العمل.    |
| PrintingPage              | String        | true     | false    |               | تخطيط الصفحة المستخدم للطباعة.                     |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | يُظهر مربع حوار الحالة أثناء الطباعة.             |
| Quality                   | Integer       | true     | false    |               | جودة ضغط صور JPEG (0-100).       |
| TiffCompression           | String        | true     | false    |               | نوع الضغط لصور TIFF.                  |
| VerticalResolution        | Integer       | true     | false    |               | الدقة العمودية (DPI) للصورة المصدرة.                |
| SaveFormat                | String        | true     | false    |               | مُعرّف التنسيق لملفات الصور.             |
| CachedFileFolder          | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.            |
| ClearData                 | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                |
| CreateDirectory           | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا. |
| EnableHttpCompression     | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.         |
| RefreshChartCache         | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.         |
| SortNames                 | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.            |
| MergeAreas                | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.               |
| SortExternalNames         | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.   |

## خصائص JsonSaveOptions

| اسم الخاصية             | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| ExportArea                | Class         | true     | false    |               | يُعرّف منطقة ورقة العمل المطلوب تصديرها.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | يشير إلى ما إذا كانت الصف الأول يحتوي على رؤوس أعمدة. |
| ExportAsString            | Boolean       | true     | false    |               | يصدِر جميع القيم كنصوص.                           |
| Indent                    | String        | true     | false    |               | النص المستخدم للمسافة البادئة (مثل مسافتين).          |
| SaveFormat                | String        | true     | false    |               | مُعرّف التنسيق لملفات JSON.                    |
| CachedFileFolder          | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.                  |
| ClearData                 | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                      |
| CreateDirectory           | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.               |
| RefreshChartCache         | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.               |
| SortNames                 | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.                  |
| MergeAreas                | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.                     |
| SortExternalNames         | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.         |

## خصائص MarkdownSaveOptions

| اسم الخاصية             | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                                  |
| ------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------ |
| Encoding                  | String        | true     | false    |               | ترميز الأحرف لملف markdown.                    |
| FormatStrategy            | String        | true     | false    |               | الاستراتيجية المستخدمة لتنسيق markdown (مثل GitHub أو CommonMark). |
| LineSeparator             | String        | true     | false    |               | حرف (أو أحرف) فاصل الأسطر المطلوب استخدامه.                              |
| SaveFormat                | String        | true     | false    |               | مُعرّف التنسيق لملفات markdown.                    |
| CachedFileFolder          | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.                      |
| ClearData                 | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                          |
| CreateDirectory           | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا.           |
| EnableHttpCompression     | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.                   |
| RefreshChartCache         | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.                   |
| SortNames                 | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                           |
| ValidateMergedAreas       | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.                      |
| MergeAreas                | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.                         |
| SortExternalNames         | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                             |
| CheckExcelRestriction     | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.            |
| UpdateSmartArt            | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.              |
| EncryptDocumentProperties | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.             |

## خصائص OoxmlSaveOptions

| اسم الخاصية             | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportCellName            | Boolean       | true     | false    |               | يتضمن أسماء الخلايا في الملف المصدر.            |
| UpdateZoom                | Boolean       | true     | false    |               | يحدّث مستوى التكبير/التصغير في المستند الناتج.       |
| EnableZip64               | Boolean       | true     | false    |               | يُفعّل امتدادات ZIP64 للملفات الكبيرة.            |
| EmbedOoxmlAsOleObject     | Boolean       | true     | false    |               | يُضمّن OOXML ككائن OLE.                       |
| CompressionType           | String        | true     | false    |               | نوع الضغط المطبّق (مثل Normal أو Maximum). |
| SaveFormat                | String        | true     | false    |               | مُعرّف التنسيق لملفات OOXML.               |
| CachedFileFolder          | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.              |
| ClearData                 | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                  |
| CreateDirectory           | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا.   |
| EnableHttpCompression     | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.           |
| RefreshChartCache         | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.           |
| SortNames                 | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                   |
| ValidateMergedAreas       | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.              |
| MergeAreas                | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.                 |
| SortExternalNames         | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                     |
| CheckExcelRestriction     | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.    |
| UpdateSmartArt            | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.      |
| EncryptDocumentProperties | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.     |

## خصائص PclSaveOptions

| اسم الخاصية             | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| fontFullName              | String        | true     | false    |               | الاسم الكامل للخط المطلوب استخدامه.                      |
| fontPclName               | String        | true     | false    |               | اسم الخط المُخصّص لـ PCL.                            |
| SaveFormat                | String        | true     | false    |               | مُعرّف التنسيق لملفات PCL.               |
| CachedFileFolder          | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.            |
| ClearData                 | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                |
| CreateDirectory           | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا. |
| EnableHttpCompression     | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.         |
| RefreshChartCache         | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.         |
| SortNames                 | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.            |
| MergeAreas                | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.               |
| SortExternalNames         | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.   |

## خصائص PDFSaveOptions

| اسم الخاصية             | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| DisplayDocTitle           | Boolean       | true     | false    |               | يستخدم عنوان المستند كعنوان PDF.            |
| ExportDocumentStructure   | Boolean       | true     | false    |               | يحفظ الهيكل المنطقي للمستند.     |
| EmfRenderSetting          | String        | true     | false    |               | إعدادات عرض صور EMF.                   |
| CustomPropertiesExport    | String        | true     | false    |               | يتحكم في تصدير خصائص المستند المخصصة.       |
| OptimizationType          | String        | true     | false    |               | نوع تحسين PDF (مثل Size أو Speed).        |
| Producer                  | String        | true     | false    |               | اسم تطبيق منتج PDF.                |
| PDFCompression            | String        | true     | false    |               | خوارزمية ضغط تدفقات PDF.               |
| FontEncoding              | String        | true     | false    |               | الترميز المستخدم للخطوط المُضمّنة.                    |
| Watermark                 | Class         | true     | false    |               | إعدادات العلامة المائية المطبّقة على PDF.               |
| CalculateFormula          | Boolean       | true     | false    |               | يحسب الصيغ قبل التصدير.                   |
| CheckFontCompatibility    | Boolean       | true     | false    |               | يتحقق من توافق الخط مع عرض PDF.      |
| Compliance                | String        | true     | false    |               | مستوى الامتثال لـ PDF/A أو PDF/X.                     |
| DefaultFont               | String        | true     | false    |               | الخط المستخدم عند عدم توفر خط المصدر.         |
| OnePagePerSheet           | Boolean       | true     | false    |               | يضع كل ورقة عمل في صفحة PDF منفصلة.        |
| PrintingPageType          | String        | true     | false    |               | يحدد نوع الصفحة للطباعة.                |
| SecurityOptions           | Class         | true     | false    |               | إعدادات الأمان مثل كلمات المرور والأذونات. |
| desiredPPI                | Integer       | true     | false    |               | الدقة المطلوبة (بكسل لكل بوصة).                  |
| jpegQuality               | Integer       | true     | false    |               | جودة صورة JPEG (0-100).                          |
| ImageType                 | String        | true     | false    |               | نوع الصورة المستخدم للتحويل إلى صور نقطية.                   |
| SaveFormat                | String        | true     | false    |               | مُعرّف التنسيق لملفات PDF.                 |
| CachedFileFolder          | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.              |
| ClearData                 | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                  |
| CreateDirectory           | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا.   |
| EnableHttpCompression     | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.           |
| RefreshChartCache         | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.           |
| SortNames                 | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                   |
| ValidateMergedAreas       | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.              |
| MergeAreas                | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.                 |
| SortExternalNames         | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                     |
| CheckExcelRestriction     | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.    |
| UpdateSmartArt            | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.      |
| EncryptDocumentProperties | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.     |

## خصائص PptxSaveOptions

| اسم الخاصية                     | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                            |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------ |
| IgnoreHiddenRows                  | Boolean       | true     | false    |               | يتخطى الصفوف المخفية أثناء التصدير.                       |
| AdjustFontSizeForRowType          | String        | true     | false    |               | يتحكم في ضبط حجم الخط بناءً على نوع الصف.       |
| ExportViewType                    | String        | true     | false    |               | يحدد نوع العرض (شريحة أو ملاحظات) المطلوب تصديره.        |
| DefaultFont                       | String        | true     | false    |               | الخط المستخدم عند عدم توفر خط المصدر.           |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | يتحقق مما إذا تم تطبيق خط الافتراضي للمصنف.   |
| CheckFontCompatibility            | Boolean       | true     | false    |               | يتحقق من توافق الخط مع تنسيق الوجهة.    |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | يتحكم في استبدال الخطوط على مستوى الأحرف.            |
| OnePagePerSheet                   | Boolean       | true     | false    |               | يضع كل ورقة عمل في شريحة منفصلة.             |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | يجعل جميع أعمدة الورقة تتناسب مع شريحة واحدة.            |
| IgnoreError                       | Boolean       | true     | false    |               | يتجاهل الأخطاء غير الحرجة أثناء التحويل.         |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | يولّد شريحة فارغة إذا لم يكن هناك ما يُعرض. |
| PageIndex                         | Integer       | true     | false    |               | فهرس الشريحة الأولى المطلوب تصديرها.                    |
| PageCount                         | Integer       | true     | false    |               | عدد الشرائح المطلوب تصديرها.                            |
| PrintingPageType                  | String        | true     | false    |               | يحدد نوع الصفحة للطباعة.                  |
| GridlineType                      | String        | true     | false    |               | يحدد طريقة عرض خطوط الشبكة.                 |
| TextCrossType                     | String        | true     | false    |               | يعرّف نوع العرض المتعدد للنصوص.             |
| DefaultEditLanguage               | String        | true     | false    |               | اللغة الافتراضية لتحرير النصوص.                     |
| EmfRenderSetting                  | String        | true     | false    |               | إعدادات عرض EMF.                            |
| MergeAreas                        | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.                   |
| SortExternalNames                 | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                       |
| UpdateSmartArt                    | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.        |
| SaveFormat                        | String        | true     | false    |               | مُعرّف التنسيق لملفات PPTX.                  |
| CachedFileFolder                  | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.                |
| ClearData                         | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                    |
| CreateDirectory                   | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا.     |
| EnableHttpCompression             | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.             |
| RefreshChartCache                 | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.             |
| SortNames                         | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                     |
| ValidateMergedAreas               | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.                |
| CheckExcelRestriction             | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.      |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.       |

## خصائص SqlScriptSaveOptions

| اسم الخاصية             | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| CheckIfTableExists        | Boolean       | true     | false    |               | يتحقق مما إذا كانت الجدول الهدف موجودًا مسبقًا.          |
| ColumnTypeMap             | String        | true     | false    |               | خريطة تعيين أسماء الأعمدة إلى أنواع بيانات SQL.               |
| CheckAllDataForColumnType | Boolean       | true     | false    |               | يفحص جميع الصفوف لاستنتاج أنواع الأعمدة.                    |
| AddBlankLineBetweenRows   | Boolean       | true     | false    |               | يدرج سطرًا فارغًا بين الصفوف المولّدة.             |
| Separator                 | String        | true     | false    |               | النص المستخدم لفصل الأعمدة (مثل الفاصلة أو علامة التبويب).      |
| OperatorType              | String        | true     | false    |               | عامل SQL المستخدم (INSERT أو UPDATE، إلخ).                |
| PrimaryKey                | Integer       | true     | false    |               | فهرس العمود الذي يعمل كمفتاح أساسي.               |
| CreateTable               | Boolean       | true     | false    |               | يولّد عبارة CREATE TABLE.                      |
| IdName                    | String        | true     | false    |               | اسم عمود المُعرّف.                           |
| StartId                   | Integer       | true     | false    |               | القيمة الابتدائية للمُعرّفات التي تزيد تلقائيًا.                 |
| TableName                 | String        | true     | false    |               | اسم جدول قاعدة البيانات الهدف.                       |
| ExportAsString            | Boolean       | true     | false    |               | يصدِر جميع القيم كنصوص.                           |
| ExportArea                | Class         | true     | false    |               | يُعرّف منطقة ورقة العمل المطلوب تصديرها.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | يشير إلى ما إذا كانت الصف الأول يحتوي على رؤوس أعمدة. |
| SaveFormat                | String        | true     | false    |               | مُعرّف التنسيق لملفات سكريبت SQL.              |
| CachedFileFolder          | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.                  |
| ClearData                 | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                      |
| CreateDirectory           | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.               |
| RefreshChartCache         | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.               |
| SortNames                 | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.                  |
| MergeAreas                | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.                     |
| SortExternalNames         | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.         |

## خصائص SvgSaveOptions

| اسم الخاصية             | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SheetIndex                | Integer       | true     | false    |               | فهرس ورقة العمل المطلوب تصديرها.                  |
| ChartImageType            | String        | true     | false    |               | تنسيق الصورة المستخدم لعرض المخططات.             |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | الاسم المُسنَد إلى الصور المُضمّنة في إخراج SVG.    |
| HorizontalResolution      | Integer       | true     | false    |               | الدقة الأفقية (DPI) لملف SVG المصدر.                |
| ImageFormat               | String        | true     | false    |               | تنسيق الصورة الهدف للعناصر النقطية.           |
| IsCellAutoFit             | Boolean       | true     | false    |               | يضبط محتويات الخلية تلقائيًا لتناسب حجم SVG.           |
| OnePagePerSheet           | Boolean       | true     | false    |               | يعرض كل ورقة عمل في صفحة SVG منفصلة.     |
| OnlyArea                  | Boolean       | true     | false    |               | يصدِر المنطقة المحددة فقط من ورقة العمل.    |
| PrintingPage              | String        | true     | false    |               | تخطيط الصفحة المستخدم للطباعة.                     |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | يُظهر مربع حوار الحالة أثناء الطباعة.             |
| Quality                   | Integer       | true     | false    |               | جودة ضغط الصور النقطية.             |
| TiffCompression           | String        | true     | false    |               | نوع الضغط لصور TIFF المُضمّنة في SVG.  |
| VerticalResolution        | Integer       | true     | false    |               | الدقة العمودية (DPI) لملف SVG المصدر.                  |
| SaveFormat                | String        | true     | false    |               | مُعرّف التنسيق لملفات SVG.               |
| CachedFileFolder          | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.            |
| ClearData                 | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                |
| CreateDirectory           | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا. |
| EnableHttpCompression     | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.         |
| RefreshChartCache         | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.         |
| SortNames                 | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.            |
| MergeAreas                | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.               |
| SortExternalNames         | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.   |

## خصائص TxtSaveOptions

| اسم الخاصية             | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                                             |
| ------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------------------------- |
| QuoteType                 | String        | true     | false    |               | نوع الاقتباس المستخدم (مثل مزدوج أو فردي).                            |
| Separator                 | String        | true     | false    |               | حرف فاصل الأعمدة (مثل الفاصلة أو علامة التبويب).                          |
| SeparatorString           | String        | true     | false    |               | النص الكامل المستخدم كفاصل عند الحاجة لأكثر من حرف واحد. |
| AlwaysQuoted              | Boolean       | true     | false    |               | يجبر جميع الحقول على الاقتباس.                                         |
| SaveFormat                | String        | true     | false    |               | مُعرّف التنسيق لملفات TXT.                                    |
| CachedFileFolder          | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.                                 |
| ClearData                 | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                                     |
| CreateDirectory           | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا.                      |
| EnableHttpCompression     | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.                              |
| RefreshChartCache         | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.                              |
| SortNames                 | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                                      |
| ValidateMergedAreas       | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.                                 |
| MergeAreas                | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.                                    |
| SortExternalNames         | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                                        |
| CheckExcelRestriction     | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.                       |
| UpdateSmartArt            | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.                         |
| EncryptDocumentProperties | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.                        |

## خصائص XlsSaveOptions و XlsbSaveOptions

| اسم الخاصية             | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| MatchColor                | Boolean       | true     | false    |               | يحفظ ألوان الخلايا بالضبط أثناء التصدير.         |
| WpsCompatibility          | Boolean       | true     | false    |               | يُفعّل التوافق مع WPS Office.             |
| SaveFormat                | String        | true     | false    |               | مُعرّف التنسيق لملفات XLS/XLSB.          |
| CachedFileFolder          | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.            |
| ClearData                 | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                |
| CreateDirectory           | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا. |
| EnableHttpCompression     | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.         |
| RefreshChartCache         | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.         |
| SortNames                 | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.            |
| MergeAreas                | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.               |
| SortExternalNames         | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.   |

## خصائص XmlSaveOptions

| اسم الخاصية             | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| SheetIndexes              | Array         | true     | false    |               | قائمة بفهارس أوراق العمل المطلوب تضمينها في التصدير.      |
| ExportArea                | Class         | true     | false    |               | يُعرّف منطقة ورقة العمل المطلوب تصديرها.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | يشير إلى ما إذا كانت الصف الأول يحتوي على رؤوس أعمدة. |
| XmlMapName                | String        | true     | false    |               | اسم خريطة XML المطبّقة على ورقة العمل.            |
| SheetNameAsElementName    | Boolean       | true     | false    |               | يستخدم اسم ورقة العمل كاسم عنصر XML.             |
| DataAsAttribute           | Boolean       | true     | false    |               | يصدِر بيانات الخلية كسمات XML بدلًا من عناصر. |
| SaveFormat                | String        | true     | false    |               | مُعرّف التنسيق لملفات XML.                     |
| CachedFileFolder          | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.                  |
| ClearData                 | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                      |
| CreateDirectory           | String        | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.               |
| RefreshChartCache         | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.               |
| SortNames                 | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.                  |
| MergeAreas                | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.                     |
| SortExternalNames         | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.         |

## خصائص XpsSaveOptions

| اسم الخاصية                     | نوع الخاصية | قابلة للقيمة الفارغة (Nullable) | للقراءة فقط (ReadOnly) | القيمة الافتراضية | الوصف                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | الخط المستخدم عند عدم توفر خط المصدر.          |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | يتحقق مما إذا تم تطبيق خط الافتراضي للمصنف.  |
| CheckFontCompatibility            | Boolean       | true     | false    |               | يتحقق من توافق الخط مع تنسيق الوجهة.   |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | يتحكم في استبدال الخطوط على مستوى الأحرف.           |
| OnePagePerSheet                   | Boolean       | true     | false    |               | يضع كل ورقة عمل في صفحة XPS منفصلة.         |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | يجعل جميع أعمدة الورقة تتناسب مع صفحة واحدة.            |
| IgnoreError                       | Boolean       | true     | false    |               | يتجاهل الأخطاء غير الحرجة أثناء التحويل.        |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | يولّد صفحة فارغة إذا لم يكن هناك ما يُعرض. |
| PageIndex                         | Integer       | true     | false    |               | فهرس الصفحة الأولى المطلوب تصديرها.                    |
| PageCount                         | Integer       | true     | false    |               | عدد الصفحات المطلوب تصديرها.                            |
| PrintingPageType                  | String        | true     | false    |               | يحدد نوع الصفحة للطباعة.                 |
| GridlineType                      | String        | true     | false    |               | يحدد طريقة عرض خطوط الشبكة.                |
| TextCrossType                     | String        | true     | false    |               | يعرّف نوع العرض المتعدد للنصوص.            |
| DefaultEditLanguage               | String        | true     | false    |               | اللغة الافتراضية لتحرير النصوص.                    |
| EmfRenderSetting                  | String        | true     | false    |               | إعدادات عرض EMF.                           |
| MergeAreas                        | Boolean       | true     | false    |               | يدمج الخلايا المجاورة عند الإمكان.                  |
| SortExternalNames                 | Boolean       | true     | false    |               | يرتب المراجع المسماة الخارجية.                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | يحدّث كائنات SmartArt إلى أحدث إصدار.       |
| SaveFormat                        | String        | true     | false    |               | مُعرّف التنسيق لملفات XPS.                  |
| CachedFileFolder                  | String        | true     | false    |               | المجلد المستخدم لملفات التخزين المؤقت المؤقتة.               |
| ClearData                         | Boolean       | true     | false    |               | يمسح البيانات الموجودة قبل الحفظ.                   |
| CreateDirectory                   | Boolean       | true     | false    |               | ينشئ المجلد الهدف إذا لم يكن موجودًا.    |
| EnableHttpCompression             | Boolean       | true     | false    |               | يُفعّل ضغط HTTP للاستجابة.            |
| RefreshChartCache                 | Boolean       | true     | false    |               | يُحدّث بيانات المخططات المخزنة مؤقتًا قبل الحفظ.            |
| SortNames                         | Boolean       | true     | false    |               | يُرتب النطاقات المسماة أبجديًا.                    |
| ValidateMergedAreas               | Boolean       | true     | false    |               | يتحقق من اتساق الخلايا المدمجة.               |
| CheckExcelRestriction             | Boolean       | true     | false    |               | يفرض حدود Excel المحددة أثناء التحويل.     |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | يُشفّر خصائص المستند في الملف الناتج.      |
---