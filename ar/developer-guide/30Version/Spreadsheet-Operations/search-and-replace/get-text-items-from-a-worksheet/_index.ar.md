---
title: "استرجاع عناصر النص من ورقة عمل Excel"
second_title: "مستند"
linktitle: "استرجاع عناصر النص في ورقة العمل"
type: docs
url: /worksheets/get-text-items/
aliases: [/get-text-items-from-a-worksheet/]
weight: 20
keywords: "Aspose.Cells، واجهة برمجة تطبيقات السحابة، Excel، ورقة عمل، عناصر نصية، REST"
description: "استرجاع جميع عناصر النص من ورقة عمل محددة في ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يتضمن أمثلة لـ cURL ورموز SDK، وخطوات المصادقة، ومخطط الاستجابة."
ArticleTitle: "استرجاع عناصر النص من ورقة عمل Excel"
---

## واجهة برمجة تطبيقات REST

تقوم هذه واجهة برمجة تطبيقات REST بقراءة عناصر النص الموجودة في ورقة عمل ضمن ملف Excel.

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{worksheet}/textItems
```

### الأمان والمصادقة
واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### معلمات الطلب


| اسم المعلمة | النوع   | الموقع | الإلزام | الوصف                                    |
| -------------- | ------ | -------- | -------- | ---------------------------------------------- |
| name           | string | path     | نعم      | اسم ملف المصنف.                            |
| sheetName      | string | path     | نعم      | اسم ورقة العمل.                         |
| folder         | string | query    | لا       | المسار إلى المجلد الذي يحتوي على المصنف. |
| storageName    | string | query    | لا       | اسم مساحة التخزين في Aspose Cloud.              |

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
| 200  | OK (تم بنجاح)                          | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | Bad Request (طلب غير صالح)                 | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | Unauthorized (غير مصرّح)                | رمز JWT غير صالح أو مفقود. |
| 413  | Payload Too Large (حمولة كبيرة جدًا)           | حجم الملف المرفّق يتجاوز الحد المسموح به. |
| 500  | Internal Server Error (خطأ داخلي في الخادم)       | خطأ غير متوقع في الخادم. |
## كيفية استخدام واجهة برمجة التطبيقات GetWorksheetTextItems باستخدام SDKs

### مواصفات واجهة برمجة التطبيقات GetWorksheetTextItems

تعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetTextItems){:target="_blank" rel="noopener noreferrer"} واجهة برمجة تطبيقات عامة قابلة للاستخدام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يُظهر المثال التالي كيفية إجراء استدعاءات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/sheet1/textItems" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
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

تبسّط مكتبات SDK (Software Development Kits) عملية الدمج من خلال التعامل مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} للاطّلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الرموز التالية كيفية إجراء استدعاءات لخدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}

---