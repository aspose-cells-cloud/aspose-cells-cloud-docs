---
title: "GetSpreadsheetStructure"
ArticleTitle: "GetSpreadsheetStructure – Aspose.Cells Cloud"
second_title: "Document"
linktype: "GetSpreadsheetStructure"
type: docs
url: /cells/spreadsheet/structure
aliases: []
keywords: "Aspose.Cells, هيكل جدول البيانات, API"
description: "تحويل هيكل البيانات الأساسية، وورقات العمل، والجداول، وجداول البيانات المحورية، والمخططات، والأشكال، ومعلومات أخرى من ملف Excel إلى كائن JSON من نوع JObject."
weight: 1000
---

## GetSpreadsheetStructure في خدمات Aspose.Cells Cloud عبر الويب

تحويل هيكل البيانات الأساسية، وورقات العمل، والجداول، وجداول البيانات المحورية، والمخططات، والأشكال، ومعلومات أخرى من ملف Excel إلى كائن JSON من نوع JObject، وذلك لحالات الاستخدام مثل تصدير البيانات، واستجابات واجهات برمجة التطبيقات، وتسجيل السجلات.

### نقطة نهاية واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/structure
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم الطلب HTTP | الوصف |
|-------------|-------|------------------------------------------|--------|
| Spreadsheet | ملف | FormData (body) | رفع ملف جدول البيانات. |
| region | نص | سلسلة الاستعلام | إعداد منطقة/لغة جدول البيانات (مثل `en-US`، `fr-FR`)، وتؤثر على تنسيق الأرقام، وتحليل التواريخ، والسلوك الخاص بالمنطقة المحلية. |
| password | نص | سلسلة الاستعلام | كلمة المرور لفتح ملف جدول البيانات. |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
|-------------|-------|-------|
| Spreadsheet | ملف | رفع ملف جدول البيانات. |

### **الاستجابة**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|-------|--------|-------|
| 200 | نجاح | تم استرجاع هيكل جدول البيانات بنجاح. |
| 400 | طلب غير صالح | معاملات طلب غير صالحة أو تنسيق ملف غير صحيح. |
| 401 | غير مُصادَق | فشلت المصادقة أو نقص رمز JWT. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | حدث خطأ غير متوقع في الخادم. |

## كيفية استخدام GetSpreadsheetStructure باستخدام حزم تطوير البرمجيات (SDKs)

### مواصفات GetSpreadsheetStructure

تُعرّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetSpreadsheetStructure" rel="noopener noreferrer">مواصفات واجهة برمجة التطبيقات GetSpreadsheetStructure</a> واجهة برمجة تطبيقات قابلة للوصول بشكل عام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells Cloud. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
# استخدام بروتوكول HTTPS لتوصيل آمن
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/structure?region=en-US&password=yourPassword" \
  -X PUT \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام حزم تطوير البرمجيات (SDKs) الخاصة بـ Aspose.Cells Cloud

يُعد استخدام حزمة تطوير البرمجيات (SDK) أسرع طريقة لتسريع عملية التطوير. فهي تُجرّدك من التفاصيل التقنية منخفضة المستوى، وتتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بحزم تطوير البرمجيات الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells Cloud باستخدام حزم تطوير البرمجيات المختلفة:
`[TBD]`
---