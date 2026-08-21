---
title: "AutoFitterOptions – دليل الخصائص والاستخدام | واجهة برمجة التطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktype: "AutoFitterOptions"
type: docs
url: /ar/auto-fitter-options/
keywords: "AutoFitterOptions، Aspose.Cells، ضبط تلقائي في إكسل، ارتفاع الصفوف، الخلايا المدمجة، واجهة برمجة التطبيقات"
description: "تعلم كيفية التحكم في ضبط ارتفاع الصفوف تلقائيًا، ومعالجة الخلايا المدمجة، والصفوف/الأعمدة المخفية، والإعدادات اللغوية، وخيارات العرض باستخدام كائن AutoFitterOptions في واجهة برمجة التطبيقات Aspose.Cells Cloud."
weight: 79
ArticleTitle: "AutoFitterOptions – دليل الخصائص والاستخدام لـ Aspose.Cells Cloud"
---

# خصائص AutoFitterOptions

يمكنك استخدام كائن `AutoFitterOptions` لضبط ضبط الارتفاع التلقائي للصفوف الذي تنفذه خدمة Aspose.Cells Cloud بدقة. ويكون هذا الكائن مفيدًا عندما تحتاج إلى تحكم دقيق في معالجة الخلايا المدمجة، أو الصفوف/الأعمدة المخفية، أو التنسيق المتعلق باللغة، أو السلوك المُرتبط بالعرض.

**المتطلبات المسبقة** – لاستخدام هذه الخيارات، يجب أن تكون مُصادَقًا باستخدام رمز وصول OAuth 2.0 صالح يحتوي على النطاق **Cells.ReadWrite**. ويعمل الطلب مع أي إصدار من SDKs التي تدعم واجهة API الإصدار 3.0.

| الاسم                        | النوع         | الوصف                                                                                              | الملاحظات                                                                                                           |
| ---------------------------- | ------------- | --------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **AutoFitMergedCellsType**   | **string**    | يحدد طريقة ضبط الخلايا المدمجة تلقائيًا.                                                            | القيم المسموح بها: `All`، `First`، `None`. القيمة الافتراضية: `All`. مثال على JSON: `"AutoFitMergedCellsType":"All"`  |
| **IgnoreHidden**             | **boolean**   | إذا كانت القيمة **true**، يتم تجاهل الصفوف والأعمدة المخفية أثناء عملية الضبط التلقائي.              | القيمة الافتراضية: `false`. مثال على JSON: `"IgnoreHidden":false`                                                   |
| **OnlyAuto**                 | **boolean**   | يشير إلى ما إذا كان سيتم ضبط الارتفاع تلقائيًا للصفوف التي لم يُعد تعديل ارتفاعها يدويًا فقط.       | القيمة الافتراضية: `false`. مثال على JSON: `"OnlyAuto":false`                                                       |
| **DefaultEditLanguage**      | **string**    | يضبط اللغة الافتراضية للتحرير في كتاب العمل.                                                       | القيمة الافتراضية: لغة النظام (مثل `"en-US"`). مثال على JSON: `"DefaultEditLanguage":"en-US"`                        |
| **MaxRowHeight**             | **double**    | أقصى ارتفاع مسموح به للصف (بالنقاط) عند الضبط التلقائي. وتُعتبر القيمة **0** أنه لا يوجد حد أقصى. | القيمة الافتراضية: `0`. مثال على JSON: `"MaxRowHeight":0`                                                           |
| **AutoFitWrappedTextType**   | **string**    | يتحكم في طريقة الضبط التلقائي للنصوص المُلتفة داخل الخلايا.                                        | القيم المسموح بها: `All`، `OnlyWrapped`، `None`. القيمة الافتراضية: `All`. مثال على JSON: `"AutoFitWrappedTextType":"All"` |
| **FormatStrategy**           | **string**    | يحدد استراتيجية التنسيق المستخدمة أثناء عملية الضبط التلقائي.                                      | القيم الشائعة: `AutoFit`، `PreserveExisting`. القيمة الافتراضية: `AutoFit`. مثال على JSON: `"FormatStrategy":"AutoFit"` |
| **ForRendering**             | **string**    | يشير إلى ما إذا كان يجب تنفيذ الضبط التلقائي لأغراض العرض (مثل PDF أو صورة).                       | القيم المسموح بها: `True`، `False`. القيمة الافتراضية: `False`. مثال على JSON: `"ForRendering":"False"`             |

فيما يلي مثال نموذجي لحمولة JSON يمكن إرسالها إلى واجهة API عند تكوين `AutoFitterOptions`.

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

مثال على طلب `cURL` يطبّق هذه الخيارات على كتاب عمل:

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/workbook/autoFitter" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json" \
  -d @autoFitterOptions.json
```

**مرجع نقطة النهاية (Endpoint)**

| الطريقة | URL | المعلمات المطلوبة | الوصف |
|--------|-----|------------------|-------|
| PUT    | `/cells/workbook/autoFitter` | `autoFitterOptions` (حمولة JSON) | يطبّق إعدادات `AutoFitterOptions` المحددة على كتاب العمل المستهدف. |
| GET    | `/cells/workbook/autoFitter` | *لا توجد* | يسترِج إعدادات `AutoFitterOptions` الحالية لكتاب العمل. |

**معلمات الطلب لنقطة النهاية PUT**

| المعلمة                  | النوع    | مطلوب | الوصف |
|--------------------------|----------|-------|-------|
| AutoFitMergedCellsType   | string   | نعم   | طريقة ضبط الخلايا المدمجة تلقائيًا (`All`، `First`، `None`). |
| IgnoreHidden             | boolean  | لا    | ما إذا كان سيتم تجاهل الصفوف/الأعمدة المخفية. |
| OnlyAuto                 | boolean  | لا    | ضبط ارتفاع الصفوف التي لا تحتوي على إعدادات ارتفاع يدوية فقط. |
| DefaultEditLanguage      | string   | لا    | لغة التحرير (مثل `en-US`). |
| MaxRowHeight             | double   | لا    | أقصى ارتفاع للصف بالنقاط؛ `0` = بدون حد أقصى. |
| AutoFitWrappedTextType   | string   | لا    | كيفية معالجة النصوص المُلتفة (`All`، `OnlyWrapped`، `None`). |
| FormatStrategy           | string   | لا    | استراتيجية التنسيق (`AutoFit`، `PreserveExisting`). |
| ForRendering             | string   | لا    | تطبيق الضبط التلقائي لأغراض العرض (`True`، `False`). |

رموز الاستجابة الشائعة:

- **200 OK** – تمت العملية بنجاح.  
- **400 Bad Request** – حُمِّلت بيانات JSON غير صالحة أو قيمة غير مدعومة.  
- **401 Unauthorized** – رمز مصادقة مفقود أو غير صالح.  
- **500 Internal Server Error** – خطأ غير متوقع في الخادم.

**مثال على استجابة GET**

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

تُظهر الأمثلة السابقة كيفية تكوين واستدعاء نموذج `AutoFitterOptions` داخل واجهة برمجة التطبيقات Aspose.Cells Cloud.
---