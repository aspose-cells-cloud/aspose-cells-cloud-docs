---
title: "إزالة الأحرف من جدول بيانات عن بُعد"
ArticleTitle: "إزالة الأحرف من جدول بيانات عن بُعد – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktype: "remove-characters-in-remote-spreadsheet"
type: docs
url: /cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
aliases: []
keywords: "Aspose.Cells, إزالة الأحرف, معالجة النصوص"
description: "يحذف الأحرف المُعرَّفة من قِبل المستخدم، أو مجموعات الرموز المُحدَّدة مسبقًا، أو أي سلسلة فرعية من كل خلية في النطاق المختار، مع الحفاظ على الصيغ والتنسيق وتحقق البيانات لجدول البيانات عن بُعد."
weight: 100
---

## إزالة الأحرف من جدول بيانات عن بُعد عبر خدمات Aspose.Cells Cloud Web

يحذف الأحرف المُعرَّفة من قِبل المستخدم، أو مجموعات الرموز المُحدَّدة مسبقًا، أو أي سلسلة فرعية من كل خلية في النطاق المختار، مع الحفاظ على الصيغ والتنسيق وتحقق البيانات لجدول البيانات عن بُعد.

### نقطة نهاية واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل          | النوع    | المسار / سلسلة الاستعلام / جسم الطلب HTTP | الوصف                                                                                                                                                                      |
|----------------------|----------|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                 | string   | Path                                      | (مطلوب) اسم ملف المصنف المراد استرجاعه.                                                                                                                                   |
| worksheet            | string   | Path                                      | تحديد ورقة العمل في جدول البيانات.                                                                                                                                          |
| range                | string   | Path                                      | تحديد نطاق ورقة العمل في جدول البيانات.                                                                                                                                    |
| removeTextMethod     | string   | Query                                     | تحديد نوع طريقة إزالة النص.                                                                                                                                                 |
| characterSets        | string   | Query                                     | تحديد مجموعات الأحرف.                                                                                                                                                      |
| removeCustomValue    | string   | Query                                     | تحديد القيمة المخصصة المراد إزالتها.                                                                                                                                       |
| caseSensitive        | boolean  | Query                                     | يؤثر على الوضع `Substring` و`CustomChars` عند تفعيله.                                                                                                                       |
| folder               | string   | Query                                     | (اختياري) مسار المجلد الذي يُخزَّن فيه المصنف. القيمة الافتراضية هي null.                                                                                                  |
| storageName          | string   | Query                                     | (اختياري) اسم وحدة التخزين في حال استخدام تخزين سحابي مخصص. تُستخدم وحدة التخزين الافتراضية إذا تم حذف هذا المعامل.                                                        |
| region               | string   | Query                                     | إعدادات إقليم/لغة جدول البيانات (مثل `en-US`، `fr-FR`). تؤثر على تنسيق الأرقام، وتفسير التواريخ، والسلوك الخاص بالمنطقة المحلية.                                         |
| password             | string   | Query                                     | كلمة المرور لفتح ملف جدول البيانات.                                                                                                                                        |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
|-------------|-------|-------|
| *بدون*       | *بدون* | لا يتطلب هذا الإجراء وجود جسم للطلب. |

### **الاستجابة**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "تمت إزالة الأحرف بنجاح.",
  "Data": {
    "RequestId": "string",
    "Workbook": {
      "Name": "string",
      "Path": "string"
    }
  }
}
```

**أكوال حالات الاستجابة**

| الكود | المعنى | الوصف |
|-------|--------|-------|
| 200 | ناجح | تمت إزالة الأحرف بنجاح وتحديث المصنف. |
| 400 | طلب غير صالح | معامل أو أكثر مفقود أو غير صالح. |
| 401 | غير مصرح به | فشلت المصادقة – رمز JWT مفقود أو غير صالح. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم الطلب الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | حدث خطأ غير متوقع في جانب الخادم. |

## كيفية استخدام إزالة الأحرف من جدول بيانات عن بُعد باستخدام مكتبات التطوير (SDKs)

### مواصفات إزالة الأحرف من جدول بيانات عن بُعد

تُعرِّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/RemoveCharactersInRemoteSpreadsheet" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات إزالة الأحرف من جدول بيانات عن بُعد</a> واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# استخدام بروتوكول HTTPS لتوصيل آمن
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters?removeTextMethod={removeTextMethod}&characterSets={characterSets}&removeCustomValue={removeCustomValue}&caseSensitive={caseSensitive}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "تمت إزالة الأحرف بنجاح.",
  "Data": {
    "RequestId": "3f5e2c1a-9b7d-4a6e-8c2f-1d5e9b7a6c4f",
    "Workbook": {
      "Name": "Sample.xlsx",
      "Path": "/documents/Sample.xlsx"
    }
  }
}
```

{< /tab >}

{< /tabs >}

### استخدام مكتبات Aspose Cells Cloud SDKs

استخدام مكتبة التطوير (SDK) هو أسرع طريقة لتسريع عملية التطوير. وتقوم المكتبة بإخفاء التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDKs.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose Cells Cloud عبر واجهة الويب باستخدام مكتبات تطوير مختلفة:
`[TBD]`
---