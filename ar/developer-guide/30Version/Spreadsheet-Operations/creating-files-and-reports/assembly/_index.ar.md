---
title: "تجميع البيانات لإنشاء تقرير Excel"
second_title: "مستند"
linktitle: "تجميع البيانات"
type: docs
url: /assembly-data-for-the-creation-of-an-excel-report/
aliases: [/assembly/]
keywords: "Aspose.Cells، تقرير Excel، تجميع البيانات، واجهة Cloud API، REST، SDK، cURL، PDF، ODS"
description: "تعلم كيفية استخدام واجهة التجميع (Assembly API) في Aspose.Cells Cloud لدمج البيانات في تقارير Excel (XLSX، PDF، ODS). يتضمن النهاية (endpoint)، المعاملات، مثال cURL، كود SDK، دليل المصادقة، ومعالجة الأخطاء."
weight: 40
---

تقوم هذه الواجهة (REST API) بتجميع البيانات **داخل** ملف Excel.

## واجهة REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/assembly
```

### **الأمان والمصادقة**

تُعد واجهات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب


| اسم المعامل | النوع   | الموقع                  | الوصف                                                                |
|------------|--------|-------------------------|----------------------------------------------------------------------|
| file       | ملف    | formData (multipart body) | ملف جدول البيانات المراد رفعه.                                      |
| DataSource | نص     | سلسلة الاستعلام (query string) | مُعرِّف مصدر البيانات الذي يوفّر البيانات للتجميع.                 |
| format     | نص     | سلسلة الاستعلام (query string) | التنسيق المطلوب للإخراج (مثل: `xlsx`، `pdf`).                      |

### **الاستجابة**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[اسم الملف2]",
    "Filesize" : [حجم الملف],
    "FileContent" : "[Base64String]"
}
```

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                              |
|-------|----------------------------|-----------------------------------------------------|
| 200   | ناجح (OK)                  | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صحيحة (مثل: نوع ملف غير مدعوم). |
| 401   | غير مخوّل (Unauthorized)    | رمز JWT غير صالح أو مفقود.                         |
| 413   | حمل البيانات كبير جدًا (Payload Too Large) | حجم ملف التحميل يتجاوز الحد المسموح.                |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                           |

## كيفية استخدام PostAssemble API باستخدام SDKs

### مواصفات PostAssemble API

تُعرِّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostAssemble) واجهة برمجة تطبيقات (API) متاحة علنًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/assembly?DataSource=ds&format=pdf" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'template=@template.xlsx' \
  -F 'data=@data.json'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "report1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "report2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs لـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة للتطوير ضد الواجهة. تُجرّدك SDK من التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على منطق أعمالك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر الإنترنت باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAssemble.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAssemble.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAssemble.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAssemble.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAssemble.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAssemble.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAssemble.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAssemble.go" >}}

{{< /tab >}}

{{< /tabs >}}