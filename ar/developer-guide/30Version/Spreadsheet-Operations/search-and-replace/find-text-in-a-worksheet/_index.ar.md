---
title: "العثور على نص في ورقة عمل Excel"
second_title: "مستند"
linktitle: "العثور في ورقة العمل"
type: docs
url: /ar/worksheets/find-text/
aliases: [  /ar/find-text-in-a-worksheet/ ]
weight: 40
keywords: "Excel، Aspose.Cells Cloud، REST API، البحث عن نص، ورقة العمل، جدول البيانات، البحث"
description: "استخدم واجهة برمجة تطبيقات Aspose.Cells Cloud REST API للعثور على نص في ورقة عمل Excel. تتوفر الواجهة عبر مجموعة متنوعة من SDKs ولغات البرمجة."
---

تقوم هذه الواجهة البرمجية (REST API) بالبحث عن نص في ورقة عمل Excel.

## واجهة برمجة التطبيقات REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/findText
```


### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.


### معاملات الطلب

| اسم المُعامل | النوع   | الموقع | الوصف        |
| -------------- | ------ | -------- | ------------------ |
| name           | string | path     | اسم المستند.     |
| sheetName      | string | path     | اسم ورقة العمل.    |
| text           | string | query    | النص المراد البحث عنه.    |
| folder         | string | query    | مجلد المستند. |
| storageName    | string | query    | اسم وحدة التخزين.      |

### **الاستجابة**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح (OK)                          | تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صحيح (Bad Request)                 | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مخوّل (Unauthorized)                | رمز JWT غير صالح أو مفقود. |
| 413  | حجم البيانات كبير جدًا (Payload Too Large)           | حجم الملف المرفّع يتجاوز الحد المسموح به. |
| 500  | خطأ داخلي في الخادم (Internal Server Error)       | خطأ غير متوقع في الخادم. |

## كيفية استخدام PostWorksheetTextSearch API باستخدام SDKs

### مواصفات PostWorksheetTextSearch API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetTextSearch) واجهة برمجة تطبيقات عامة قابلة للوصول وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يُظهر المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/findText?text=a" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة لتطوير التطبيقات. تُجرّدك الـ SDK من التفاصيل التقنية منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetTextSearch.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetTextSearch.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetTextSearch.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetTextSearch.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetTextSearch.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetTextSearch.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetTextSearch.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetTextSearch.go" >}}

{{< /tab >}}

{{< /tabs >}}