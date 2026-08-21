---
title: "SearchAllTextItemsInRemoteSpreadsheet"
ArticleTitle: "SearchAllTextItemsInRemoteSpreadsheet – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "وثيقة"
linktype: "SearchAllTextItemsInRemoteSpreadsheet"
type: docs
url: /cells/{name}/search/content/all-textitems
aliases: []
keywords: "بحث، عناصر نصية، Aspose.Cells"
description: "البحث عن جميع العناصر النصية في جدول بيانات بعيد باستخدام Aspose.Cells Cloud."
weight: 100
---

## دالة SearchAllTextItemsInRemoteSpreadsheet في خدمات ويب Aspose.Cells Cloud

تقوم هذه الطريقة بالبحث عن جميع العناصر النصية داخل ملف جدول بيانات بعيد. وتدعم البحث عبر جميع الأوراق والخلايا في المصنف، وتحديد مرات تكرار مصطلح البحث. وتُنفَّذ العملية في السحابة، ولا تتطلب تخزينًا محليًا. تأكد من امتلاك الأذونات الضرورية لقراءة ملف المصدر. وإذا تعذَّر الوصول إلى ملف المصدر أو حدث خطأ أثناء عملية البحث (مثل تنسيق ملف غير مدعوم)، فسيتم رمي استثناء مناسب. وقد تُرجع الطريقة مواقع التطابقات (مثل اسم الورقة وإحداثيات الخلية) حسب تفاصيل التنفيذ.

### نقطة نهاية واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة قائمة على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|-------------|-------|--------------------------------------|--------|
| name | string | المسار | اسم ملف المصنف. |
| folder | string | استعلام | مسار المجلد حيث يتم تخزين المصنف. |
| storageName | string | استعلام | (اختياري) اسم وحدة التخزين إذا كنت تستخدم تخزينًا سحابيًا مخصصًا. استخدم وحدة التخزين الافتراضية إذا حُذف. |
| region | string | استعلام | إعداد منطقة/لغة جدول البيانات (مثل `en-US`، `fr-FR`). يؤثر على تنسيق الأرقام، وتفسير التواريخ، والسلوك الخاص باللغة المحلية. |
| password | string | استعلام | كلمة المرور لفتح ملف جدول البيانات. |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
| -------------- | ---- | ----------- |
| [TBD] | | [TBD] |

### **الاستجابة**

```json
{
  "TextItems": [
    {
      "SheetName": "string",
      "CellAddress": "string",
      "Text": "string"
    }
  ],
  "TotalCount": 0
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|------|--------|--------|
| 200 | ناجح | نجح الطلب وتحتوي الاستجابة على جميع العناصر النصية الموجودة في جدول البيانات. |
| 400 | طلب غير صالح | عنوان URL أو معاملات طلب غير صحيحة. |
| 401 | غير مصرّح | فشلت المصادقة أو لم تُقدَّم بيانات اعتماد. |
| 404 | غير موجود | ملف المصدر غير قابل للوصول. |
| 413 | حملة البيانات كبيرة جدًا | تجاوز حجم حملة الطلب الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | واجه جدول البيانات خللًا في استرداد البيانات. |

## كيفية استخدام SearchAllTextItemsInRemoteSpreadsheet مع حزم تطوير البرمجيات (SDKs)

### مواصفات SearchAllTextItemsInRemoteSpreadsheet

تُعرِّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchAllTextItemsInRemoteSpreadsheet" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات SearchAllTextItemsInRemoteSpreadsheet</a> واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# استخدام HTTPS لتوصيل آمن
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "TextItems": [
    {
      "SheetName": "Sheet1",
      "CellAddress": "A1",
      "Text": "Sample text"
    }
  ],
  "TotalCount": 1
}
```

{< /tab >}

{< /tabs >}

### استخدام حزم تطوير البرمجيات (SDKs) لـ Aspose Cells Cloud

يُعد استخدام حزمة تطوير البرمجيات (SDK) الطريقة الأسرع لتسريع عملية التطوير. فحزم تطوير البرمجيات (SDKs) تُجرِّد التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بحزم تطوير البرمجيات (SDKs) لـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose Cells Cloud باستخدام حزم تطوير البرمجيات (SDKs) المختلفة:
`[TBD]`
---