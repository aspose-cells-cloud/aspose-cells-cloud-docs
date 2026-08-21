---
title: "GetMergedCellsInWorksheet"
ArticleTitle: "الحصول على الخلايا المدمجة في ورقة العمل – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "وثيقة"
linktype: "docs"
url: /ar/cells/spreadsheet/mergedcells
aliases: []
keywords: "Aspose Cells، الخلايا المدمجة، ورقة العمل، واجهة برمجة التطبيقات"
description: "الحصول على جميع مناطق الخلايا المدمجة من ورقة عمل جدول محلي."
weight: 1000
---

## خدمة Get Merged Cells In Worksheet من Aspose.Cells Cloud

الحصول على جميع مناطق الخلايا المدمجة من ورقة عمل جدول محلي.

### نقطة نهاية واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells
```

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud أمانًا وتستدعي <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة القائمة على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار / سطر الاستعلام / جسم HTTP | الوصف |
|----------------|------|-----------------------------|-------------|
| Spreadsheet | ملف | FormData | رفع ملف جدول. |
| worksheet | نص | سطر الاستعلام | اسم ورقة العمل. |
| region | نص | سطر الاستعلام | إعدادات المنطقة/اللغة للجدول (مثل `en-US`، `fr-FR`). تؤثر هذه الإعدادات على تنسيق الأرقام، وتفسير التواريخ، والسلوك الخاص باللغة والموقع. |
| password | نص | سطر الاستعلام | كلمة المرور لفتح ملف الجدول. |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
| -------------- | ---- | ----------- |
| N/A | N/A | لا تقبل هذه العملية جسم JSON؛ يتم إرسال ملف الجدول عبر `multipart/form-data`. |

### **الاستجابة**

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|------|---------|-------------|
| 200 | ناجح | تم استرداد مناطق الخلايا المدمجة بنجاح. |
| 400 | طلب غير صحيح | أحد معاملات الطلب أو أكثر غير صالح أو مفقود. |
| 401 | غير مُصادَق | فشلت المصادقة – رمز JWT غير صالح أو مفقود. |
| 413 | حجم الحمولة كبير جدًا | حجم ملف الجدول المرفوع يتجاوز الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | حدث خطأ غير متوقع في الخادم. |

## كيفية استخدام Get Merged Cells In Worksheet مع مكتبات التطوير (SDKs)

### مواصفات Get Merged Cells In Worksheet

تعرّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInWorksheet" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات Get Merged Cells In Worksheet</a> على واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# استخدام HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells?worksheet=Sheet1&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

{< /tab >}

{< /tabs >}

### استخدام مكتبات Aspose Cells Cloud SDKs

استخدام مكتبات التطوير (SDKs) هو أسرع طريقة لتسريع عملية التطوير. وتقوم المكتبة بإخفاء التفاصيل من المستوى المنخفض، ما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDKs.

توضح الأمثلة التالية كيفية استدعاء خدمات الويب Aspose Cells Cloud باستخدام مكتبات تطوير مختلفة:
 `[TBD]`
---