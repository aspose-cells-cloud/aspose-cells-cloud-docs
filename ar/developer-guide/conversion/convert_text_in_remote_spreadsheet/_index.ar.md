---
title: "تحويل النص في جدول بيانات عن بُعد"
ArticleTitle: "تحويل النص في جدول بيانات عن بُعد – Aspose.Cells Cloud"
second_title: "وثيقة"
linktype: "تحويل النص في جدول بيانات عن بُعد"
type: docs
url: /cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
aliases: []
keywords: "Aspose.Cells, تحويل النص, API"
description: "يُحوّل النص في النطاق المحدّد من ورقة العمل، بما في ذلك تحويل الأرقام، واستبدال الأحرف، ومعالجة فواصل الأسطر، وتوحيد الأحرف المُعلّمة."
weight: 1000
---

## خدمة تحويل النص في جدول بيانات عن بُعد من Aspose.Cells Cloud

تُشير إلى تحويل الأرقام المخزَّنة على هيئة نصوص إلى تنسيق الأرقام الصحيح، واستبدال الأحرف غير المرغوب فيها وفواصل الأسطر بأحرف مُحدَّدة، وتحويل الأحرف المُعلّمة إلى أحرف مكافئة غير مُعلّمة.

### نقطة نهاية واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
```

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud مصادقة <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">تعتمد على رمز JWT</a> وتوفّر أمانًا عاليًا.

### معاملات الطلب

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم الطلب HTTP | الوصف |
|-------------|-------|-------------------------------------------|--------|
| name | string | Path | (إجباري) اسم ملف المصنف المطلوب استرجاعه. |
| worksheet | string | Path | تحديد ورقة العمل في جدول البيانات. |
| range | string | Path | تحديد نطاق ورقة العمل في جدول البيانات. |
| convertTextType | string | Query | نوع التحويل المطلوب للنص. (إجباري) |
| sourceCharacters | string | Query | الأحرف المصدر. (اختياري) |
| targetCharacters | string | Query | الأحرف الهدف. (اختياري) |
| folder | string | Query | (اختياري) مسار المجلد الذي يحتوي على المصنف. القيمة الافتراضية هي null. |
| storageName | string | Query | (اختياري) اسم وحدة التخزين عند استخدام خدمة تخزين سحابية مخصصة. يُستخدم التخزين الافتراضي إذا لم يُحدَّد. |
| region | string | Query | إعدادات الإقليم/اللغة لجدول البيانات (مثل `en-US`, `fr-FR`). تؤثر على تنسيق الأرقام، وتحليل التواريخ، والسلوك المُتعلّق باللغة المحلية. (اختياري) |
| password | string | Query | كلمة المرور لفتح ملف جدول البيانات. (اختياري) |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
|------------|-------|-------|
| - | - | - |

### **الاستجابة**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "اكتمل تحويل النص بنجاح.",
  "Data": {
    // يمكن إضافة تفاصيل نتيجة التحويل هنا، مثل عدد الخلايا المُحدَّثة.
  }
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|-------|--------|-------|
| 200 | OK | اكتمل عملية تحويل النص بنجاح. |
| 400 | Bad Request | كان الطلب غير مكوّن بشكل صحيح أو ناقص المعاملات الإجبارية. |
| 401 | Unauthorized | فشلت المصادقة أو أن رمز JWT مفقود/غير صالح. |
| 413 | Payload Too Large | تجاوز حجم حمل الطلب الحد المسموح به. |
| 500 | Internal Server Error | حدث خطأ غير متوقع في الخادم. |

## كيفية استخدام خدمة تحويل النص في جدول بيانات عن بُعد باستخدام مكتبات SDK

### مواصفات تحويل النص في جدول بيانات عن بُعد

تُعرّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/{ConvertTextInRemoteSpreadsheet}" rel="noopener noreferrer">مواصفات API لتحويل النص في جدول بيانات عن بُعد</a> واجهة برمجة تطبيقات متاحة علنًا وتتيح لك إجراء عمليات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose Cells Cloud. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# استخدم HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text?convertTextType={convertTextType}&sourceCharacters={sourceCharacters}&targetCharacters={targetCharacters}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
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
  "Message": "اكتمل تحويل النص بنجاح.",
  "Data": {
    "UpdatedCellsCount": 124,
    "Details": "تم تحويل الأرقام، واستبدال الأحرف، وتوحيد فواصل الأسطر."
  }
}
```

{< /tab >}

{< /tabs >}

### استخدام مكتبات Aspose Cells Cloud SDK

يُعد استخدام مكتبة SDK أسرع طريقة لتسريع عملية التطوير. إذ تعمل المكتبات على تجريد التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للاطّلاع على القائمة الكاملة لمكتبات Aspose.Cells Cloud SDK.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose Cells Cloud باستخدام مكتبات SDK مختلفة:
 `[TBD]`
---