---
title: "استرجاع عناصر نصية من ملف عمل Excel"
ArticleTitle: "استرجاع عناصر نصية من ملف عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktype: "docs"
url: /workbook/get-text-items/
aliases: [/get-text-items-from-a-workbook/]
weight: 10
keywords: "Excel، Aspose.Cells Cloud، واجهة برمجة تطبيقات REST، جدول بيانات، استرجاع عناصر نصية، ملف عمل"
description: "استرجاع عناصر نصية من ملف عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. متاح عبر حزم تطوير برمجيات (SDKs) لـ C#، Java، Python، PHP، Ruby، Go، Node.js، Perl، و Swift."
---


## واجهة برمجة تطبيقات REST

تقوم هذه واجهة برمجة تطبيقات REST بقراءة **عناصر النص** في ملف Excel.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/textItems
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.


### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
| ------------ | ------ | -------- | ------------------------------------------------------ |
| name | string | path | اسم ملف ملف العمل. |
| folder | string | query | مسار المجلد في التخزين حيث يقع ملف العمل. |
| storageName | string | query | اسم خدمة التخزين. |

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

| الرمز | المعنى | الوصف |
|------|-----------------------------|--------------------------------------------------|
| 200 | ناجح | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصدق | رمز JWT غير صالح أو مفقود. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة برمجة تطبيقات GetWorkbookTextItems مع حزم تطوير البرمجيات (SDKs)

### مواصفات واجهة برمجة تطبيقات GetWorkbookTextItems

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookTextItems) واجهة برمجة تطبيقات قابلة للوصول بشكل عام وتسمح لك بإجراء تفاعلات REST مباشرة من خلال متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء استدعاء لواجهة برمجة تطبيقات السحابة باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/textItems" -H "accept: application/json"
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

رموز الحالة الشائعة للاستجابة:

| الرمز | الوصف |
|------|---------------------------------------------|
| 200 | نجح الطلب؛ يتم إرجاع عناصر النص. |
| 401 | غير مصدق – رمز مفقود أو غير صالح. |
| 403 | ممنوع – صلاحيات غير كافية. |
| 404 | غير موجود – ملف العمل أو المورد غير موجود. |
| 500 | خطأ داخلي في الخادم – فشل غير متوقع. |

### استخدام حزم تطوير البرمجيات الخاصة بـ Aspose.Cells Cloud

يستخدم هذا المثال إصدار واجهة برمجة التطبيقات **v3.0**؛ راجع سجل التغييرات للحصول على الإصدارات الأحدث. استخدام حزمة تطوير البرمجيات (SDK) هو أفضل طريقة لتسريع عملية التطوير، حيث تتعامل الحزمة مع التفاصيل منخفضة المستوى وتركّز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرمجيات الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام حزم تطوير برمجيات مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}