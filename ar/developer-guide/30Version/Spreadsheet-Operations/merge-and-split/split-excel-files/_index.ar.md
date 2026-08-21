---
title: "تقسيم ملف Excel إلى ملفات متعددة"
ArticleTitle: "كيفية تقسيم ملف Excel إلى ملفات متعددة باستخدام واجهة Aspose.Cells Cloud API"
second_title: "المستند"
linktype: "تقسيم ملف Excel"
type: docs
url: /ar/split-multi-excel-files/
aliases: [  /ar/split/multi-files/ ]
keywords: "Excel، Aspose.Cells Cloud، REST API، تقسيم المصنف، ملفات متعددة، JPEG، PNG، PDF، CSV، JSON"
description: "تتيح واجهة Aspose.Cells Cloud REST API تقسيم ملف Excel (المصنف) إلى ملفات متعددة بصيغ مختلفة. توفر هذه الوثائق معلمات الطلب، ومثالًا باستخدام cURL، وأكواد أمثلة لعدة لغات برمجة مثل C#، Java، PHP، Ruby، Node.js، Python، Perl، و Go."
weight: 130
---

تقوم هذه الواجهة (REST API) بتقسيم **مصنف Excel** إلى ملفات متعددة بصيغ مختلفة.

> **المتطلبات الأساسية** – لاستخدام هذه الواجهة، يجب الحصول على رمز JWT صالح، والتأكد من استخدام إصدار مدعوم من SDK، وتحقق من أن مصنفك مخزن في موقع تخزين مدعوم. كما تفرض الواجهة حدودًا لحجم الملفات مُوثَّقة في إرشادات المنصة.

## واجهة PostWorkbookSplit

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/split
```

### **الأمان والمصادقة**

تُعتبر واجهات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات الطلب

| اسم المعلمة         | النوع     | الموقع       | الوصف                                                                                         | إلزامي |
| -------------------- | -------- | ------------ | ---------------------------------------------------------------------------------------------- | ------ |
| files[]              | ملف      | formData     | ملف Excel واحد أو أكثر لـ **تقسيمه**. استخدم `file1`, `file2`, … في الطلب.                   | نعم    |
| format               | سلسلة   | Query        | الصيغة المطلوبة للملفات الناتجة بعد التقسيم.                                                 | لا     |
| from                 | عدد صحيح | Query        | فهرس ورقة العمل الابتدائي.                                                                    | لا     |
| to                   | عدد صحيح | Query        | فهرس ورقة العمل النهائي.                                                                      | لا     |
| horizontalResolution | عدد صحيح | Query        | الدقة الأفقية للصورة.                                                                         | لا     |
| verticalResolution   | عدد صحيح | Query        | الدقة العمودية للصورة.                                                                        | لا     |
| outFolder            | سلسلة   | Query        | المجلد الذي ستُخزَّن فيه الملفات المُقسَّمة.                                                 | لا     |
| splitNameRule        | سلسلة   | Query        | قاعدة تسمية الملفات المُقسَّمة.                                                               | لا     |
| folder               | سلسلة   | Query        | المجلد الذي يحتوي على المصنف الأصلي.                                                          | لا     |
| storageName          | سلسلة   | Query        | اسم مساحة التخزين المراد استخدامها.                                                           | لا     |

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200,
    "Files": [
      {
        "Filename" : "[اسم الملف1]",
        "Filesize" : [حجم الملف],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[اسم الملف2]",
        "Filesize" : [حجم الملف],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[اسم الملف3]",
        "Filesize" : [حجم الملف],
        "FileContent" : "[Base64String]"
      }
    ]
}
```

**رموز حالة HTTP**

| الكود | المعنى                      | الوصف                                               |
|------|-----------------------------|------------------------------------------------------|
| 200  | ناجح (OK)                  | تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request) | معلمات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم).    |
| 401  | غير مصرّح (Unauthorized)    | رمز JWT غير صالح أو مفقود.                            |
| 413  | حمل البيانات كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به.            |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                            |

## كيفية استخدام واجهة PostWorkbookSplit باستخدام SDKs

### مواصفات واجهة PostWorkbookSplit

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات لواجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Result": {
    "Documents": [
      {
        "Id": 1,
        "link": {
          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",
          "Rel": null,
          "Title": null,
          "Type": null
        }
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

يُعد استخدام SDKs أفضل طريقة لتسريع عملية التطوير، إذ تقوم SDKs بإدارة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات لخدمات Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}