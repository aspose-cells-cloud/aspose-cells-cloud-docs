---
title: "البحث عن الروابط التالفة في ورقة عمل عن بُعد"
ArticleTitle: "البحث عن الروابط التالفة في ورقة عمل عن بُعد – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "وثيقة"
linktype: "SearchBrokenLinksInRemoteWorksheet"
type: docs
url: /cells/{name}/worksheets/{worksheet}/search/broken-links
aliases: []
keywords: "Aspose.Cells، البحث عن الروابط التالفة، ورقة عمل عن بُعد"
description: "البحث عن الروابط التالفة في ورقة عمل لملف جدول بيانات مخزن في تخزين سحابي عن بُعد."
weight: 100
---

## البحث عن الروابط التالفة في ورقة عمل عن بُعد ضمن خدمات الويب Aspose.Cells Cloud

تقوم هذه الطريقة بالبحث عن الروابط التالفة داخل ورقة عمل لملف جدول بيانات مخزن في تخزين سحابي عن بُعد. وتقوم بمسح جميع الأوراق والخلايا لتحديد الروابط التشعبية التي لم تعد تشير إلى وجهات صالحة، مثل عناوين URL غير النشطة أو المراجع الخارجية المفقودة. ويتم تنفيذ العملية عن بُعد داخل بيئة السحابة، دون الحاجة إلى تنزيل الملف إلى الجهاز المحلي.

### نقطة نهاية واجهة برمجة التطبيقات على الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **الأمان والمصادقة**

واجهات برمجة التطبيقات (APIs) الخاصة بـ Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|-------------|------|-----------------------------------|--------|
| name | string | Path | اسم ملف مصنف الجداول الذي سيتم البحث فيه. |
| worksheet | string | Path | تحديد ورقة العمل التي سيتم إجراء البحث فيها. |
| folder | string | Query | مسار المجلد الذي يخزن فيه مصنف الجداول. (اختياري) |
| storageName | string | Query | (اختياري) اسم وحدة التخزين عند استخدام تخزين سحابي مخصص. ويُستخدم تخزين افتراضي عند حذف القيمة. |
| region | string | Query | إعداد منطقة/لغة جدول البيانات (مثل `en-US` أو `fr-FR`). يؤثر على تنسيق الأرقام، وتفسير التواريخ، والسلوك الخاص باللغة والمحلية. |
| password | string | Query | كلمة المرور لفتح ملف جدول البيانات. |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
| -------------- | ---- | ----------- |
| — | — | لا يتطلب هذا الإجراء وجود جسم طلب. |

### **الاستجابة**

```json
{
  "Links": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|------|---------|--------|
| 200 | OK | تم استرجاع قائمة الروابط التالفة بنجاح. |
| 400 | Bad Request | معاملات طلب غير صالحة أو عنوان URL غير مُنسَّق بشكل صحيح. |
| 401 | Unauthorized | فشلت عملية المصادقة، أو لم يتم تقديم بيانات اعتماد. |
| 404 | Not Found | لم يكن الملف المصدر متاحًا. |
| 413 | Payload Too Large | جسم الطلب كبير جدًا. |
| 500 | Internal Server Error | واجه جدول البيانات خطأً أثناء استرجاع البيانات. |

## كيفية استخدام خدمة البحث عن الروابط التالفة في ورقة عمل عن بُعد باستخدام SDKs

### مواصفات البحث عن الروابط التالفة في ورقة عمل عن بُعد

تُعرّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteWorksheet" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات البحث عن الروابط التالفة في ورقة عمل عن بُعد</a> واجهة برمجة تطبيقات عامة قابلة للوصول وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# استخدام بروتوكول HTTPS لإنشاء اتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Links": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

{< /tab >}

{< /tabs >}

### استخدام SDKs الخاصة بـ Aspose Cells Cloud

استخدام SDKs هو أسرع طريقة لتسريع عملية التطوير. وتقوم SDKs بإخفاء التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose Cells Cloud باستخدام مكتبات SDK مختلفة:
`[TBD]`
---