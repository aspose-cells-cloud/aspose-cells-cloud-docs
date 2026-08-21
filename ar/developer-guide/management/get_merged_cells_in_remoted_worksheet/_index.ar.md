---
title: "GetMergedCellsInRemotedWorksheet"
ArticleTitle: "الحصول على الخلايا المدمجة في ورقة عمل عن بُعد – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktype: "docs"
url: /cells/mergedcells/get
aliases: []
keywords: "Aspose Cells، الحصول على الخلايا المدمجة، ورقة عمل عن بُعد، واجهة برمجة التطبيقات"
description: "يسترجع جميع مناطق الخلايا المدمجة من ورقة عمل عن بُعد في ملف جدول بيانات."
weight: 10
---

## خدمة GetMergedCellsInRemotedWorksheet في Aspose.Cells Cloud Web Services

تحصل على جميع مناطق الخلايا المدمجة من ورقة عمل في ملف جدول بيانات مخزن عن بُعد.

### نقطة نهاية واجهة برمجة التطبيقات للويب

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells
```

### **الأمان والمصادقة**

تُعد واجهات برمجة التطبيقات في Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|-------------|-------|--------------------------------------|--------|
| name | string | Path | اسم ملف جدول البيانات |
| worksheet | string | Path | اسم ورقة العمل |
| folder | string | Query | مسار مساحة التخزين السحابية لملف جدول البيانات |
| storageName | string | Query | (اختياري) اسم مساحة التخزين عند استخدام مساحة تخزين سحابية مخصصة. يُستخدم مساحة التخزين الافتراضية في حال تجاهُل هذا المعامل |
| region | string | Query | إعدادات الإقليم/اللغة لملف جدول البيانات (مثل `en-US`، `fr-FR`). يؤثر على تنسيق الأرقام، وتفسير التواريخ، والسلوك المرتبط بالإعدادات المحلية |
| password | string | Query | كلمة المرور لفتح ملف جدول البيانات |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
|-------------|-------|--------|
| — | — | *لا يوجد* |

### **الاستجابة**

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|-------|---------|--------|
| 200 | OK | نجح الطلب وتم إرجاع قائمة بمناطق الخلايا المدمجة |
| 400 | Bad Request | عنوان URL غير صالح أو معاملات طلب غير مهيأة بشكل صحيح |
| 401 | Unauthorized | فشلت المصادقة أو لم تُوفَّر أي بيانات اعتماد |
| 413 | Payload Too Large | حجم حمل الطلب يتجاوز الحد المسموح به |
| 500 | Internal Server Error | حدث خطأ غير متوقع في ملف جدول البيانات أثناء محاولة استرجاع البيانات |

## كيفية استخدام GetMergedCellsInRemotedWorksheet باستخدام مكتبات التطوير (SDKs)

### مواصفات GetMergedCellsInRemotedWorksheet

تُعرّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInRemotedWorksheet" rel="noopener noreferrer">مواصفات واجهة برمجة التطبيقات GetMergedCellsInRemotedWorksheet</a> واجهة برمجة تطبيقات عامة قابلة للاسترجاع، وتمكنك من إجراء تفاعلات REST مباشرة من خلال متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء استدعاءات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# استخدام HTTPS لضمان اتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/Sample.xlsx/worksheets/Sheet1/mergedcells?folder=MyFolder&storageName=MyStorage&region=en-US&password=1234" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات Aspose Cells Cloud SDKs

استخدام مكتبات التطوير (SDKs) هو أسرع طريقة لتسريع عملية التطوير. فالمكتبات تُجرّدك من التفاصيل التقنية منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDKs.

توضح أمثلة الكود التالية كيفية استدعاء خدمات الويب Aspose Cells Cloud باستخدام مكتبات مختلفة:
`[TBD]`
---