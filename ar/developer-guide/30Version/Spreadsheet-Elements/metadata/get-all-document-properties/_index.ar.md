---
title: "الحصول على جميع خصائص المستند"
second_title: "المستند"
linktitle: "الحصول على الكل"
type: docs
url: /document-properties/get-all/
aliases: [/get-all-document-properties/]
keywords: "الحصول على جميع خصائص المستند، Aspose.Cells Cloud، خصائص مستندات Excel، واجهة برمجة التطبيقات REST، مكتبة أدوات SDK، بيانات التعريف الخاصة بـ Excel"
description: "استرجاع جميع خصائص المستند من ملف Excel باستخدام واجهة برمجة التطبيقات REST الخاصة بـ Aspose.Cells Cloud. تعمل نقطة النهاية هذه مع جميع مكتبات الأدوات SDK المدعومة ولغات البرمجة."
ArticleTitle: "الحصول على جميع خصائص المستند – واجهة برمجة تطبيقات Aspose.Cells Cloud"
weight: 25
---

تقوم هذه الواجهة البرمجية REST بقراءة خصائص المستند.

## واجهة برمجة التطبيقات GetDocumentProperties

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع   | الموقع | الوصف                             |
|-------------|---------|--------|------------------------------------|
| name        | string  | path   | اسم ملف Excel.                    |
| folder      | string  | query  | المجلد الذي يحتوي على الملف.      |
| storageName | string  | query  | اسم خدمة التخزين.                 |

يعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperties) واجهة برمجة تطبيقات متاحة للعامة، ويسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperties": {
    "DocumentPropertyList": [
      {
        "Name": "Title",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Title",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Subject",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Subject",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Author",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Author",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Keywords",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Keywords",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Comments",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Comments",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "LastSavedBy",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/LastSavedBy",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "CreateTime",
        "Value": "6/5/2015 6:17:20 PM",
        "BuiltIn": "True",
        "link": {
          "Href": "/CreateTime",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "LastSavedTime",
        "Value": "9/27/2019 9:09:43 PM",
        "BuiltIn": "True",
        "link": {
          "Href": "/LastSavedTime",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Category",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Category",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "NameOfApplication",
        "Value": "Microsoft Excel",
        "BuiltIn": "True",
        "link": {
          "Href": "/NameOfApplication",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Version",
        "Value": "16.0300",
        "BuiltIn": "True",
        "link": {
          "Href": "/Version",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Security",
        "Value": "0",
        "BuiltIn": "True",
        "link": {
          "Href": "/Security",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "ScaleCrop",
        "Value": "False",
        "BuiltIn": "True",
        "link": {
          "Href": "/ScaleCrop",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Template",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Template",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Manager",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Manager",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Company",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Company",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "LinksUpToDate",
        "Value": "False",
        "BuiltIn": "True",
        "link": {
          "Href": "/LinksUpToDate",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/documentproperties",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                              |
|-------|-----------------------------|-----------------------------------------------------|
| 200   | ناجح (OK)                   | تم تطبيق الفلتر بنجاح؛ يحتوي الاستجابة على تفاصيل العملية. |
| 400   | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401   | غير مصرّح به (Unauthorized) | رمز JWT غير صالح أو مفقود.                         |
| 413   | حجم البيانات كبير جدًا (Payload Too Large) | يتجاوز حجم الملف المرفوع الحد المسموح به.         |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                         |

## عائلة مكتبات أدوات SDK السحابية

استخدام مكتبة أدوات SDK هو أفضل طريقة لتسريع عملية التطوير. تتعامل مكتبة الأدوات SDK مع التفاصيل منخفضة المستوى وتمكنك من التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات أدوات SDK الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر الإنترنت باستخدام مكتبات أدوات SDK المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperties.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperties.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperties.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperties.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperties.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperties.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperties.go" >}}

{{< /tab >}}

{{< /tabs >}}