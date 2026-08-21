---
title: "GetStructureInRemoteSpreadsheet"
ArticleTitle: "استرجاع الهيكل في جدول بيانات بعيد – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "وثيقة"
linktype: "GetStructureInRemoteSpreadsheet"
type: docs
url: /ar/cells/{name}/structure
aliases: []
keywords: "Aspose.Cells, GetStructure, جدول بيانات, هيكل"
description: "استرجاع البيانات الوصفية البنيوية لملف Excel البعيد، بما في ذلك الأوراق، الجداول، جداول Pivot، الرسوم البيانية، الأشكال، وغير ذلك من المعلومات الأساسية."
weight: 100
---

## استرجاع الهيكل في جدول بيانات بعيد لخدمات الويب Aspose.Cells Cloud

تحويل البيانات الوصفية الأساسية، والأوراق، والجداول، وجداول Pivot، والرسوم البيانية، والأشكال، والمعلومات الأخرى لملف Excel إلى كائن JSON من نوع JObject، وذلك لسيناريوهات مثل تصدير البيانات، واستجابات واجهات برمجة التطبيقات، وتسجيل السجلات.

### نقطة نهاية واجهة برمجة تطبيقات الويب

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/structure
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|----------------|------|-----------------------------|-------------|
| name | string | Path | اسم ملف جدول البيانات. |
| folder | string | Query | المجلد الموجود فيه الملف. (اختياري) |
| storageName | string | Query | (اختياري) اسم وحدة التخزين عند استخدام مساحة تخزين سحابية مخصصة. يُستخدم مساحة التخزين الافتراضية عند حذف القيمة. |
| region | string | Query | إعداد منطقة/لغة جدول البيانات (مثل `en-US` أو `fr-FR`). يؤثّر على تنسيق الأرقام، وتفسير التواريخ، والسلوك المتعلق باللغة المحلية. |
| password | string | Query | كلمة المرور لفتح ملف جدول البيانات. |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

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
  "WorkbookProperties": {
    "Author": "string",
    "Created": "string",
    "Version": "string"
  },
  "DocumentProperties": {
    "Title": "string",
    "Subject": "string",
    "Keywords": "string"
  }
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|------|---------|-------------|
| 200 | ناجح | تم استرجاع هيكل الملف بنجاح. |
| 400 | طلب غير صالح | معاملات طلب غير صالحة. |
| 401 | غير مصدق | فشلت المصادقة أو غياب الرمز. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم جسم الطلب الحد المسموح. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## كيفية استخدام استرجاع الهيكل في جدول بيانات بعيد باستخدام SDKs

### مواصفات استرجاع الهيكل في جدول بيانات بعيد

تُعرّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetStructureInRemoteSpreadsheet" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات استرجاع الهيكل في جدول بيانات بعيد</a> واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفّح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
# استخدام HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/structure?folder=myFolder&storageName=MyStorage&region=en-US&password=SecretPwd" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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
  "WorkbookProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z",
    "Version": "16.0"
  },
  "DocumentProperties": {
    "Title": "SalesReport",
    "Subject": "Quarterly Sales",
    "Keywords": "sales,report,2023"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام Aspose Cells Cloud SDKs

استخدام SDKs هو أسرع طريقة لتسريع التطوير. تُجرّد SDKs من التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose Cells Cloud باستخدام مكتبات SDK مختلفة:
`[TBD]`
---