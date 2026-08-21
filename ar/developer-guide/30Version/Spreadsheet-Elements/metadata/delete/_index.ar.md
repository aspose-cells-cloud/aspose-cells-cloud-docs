---
title: "حذف البيانات الوصفية من ملفات Excel"
second_title: "مستند"
linktitle: "حذف دون استخدام التخزين"
type: docs
url: /ar/metadata/delete/
keywords: "Aspose.Cells, حذف البيانات الوصفية, واجهة برمجة تطبيقات Excel, خصائص المصنف"
description: "احذف البيانات الوصفية للمصنف (المؤلف، العنوان، البيانات المخصصة) عبر واجهة برمجة تطبيقات Aspose.Cells Cloud. يتضمن نقطة النهاية، المصادقة، المُعلمات، وأمثلة لـ cURL وSDK."
weight: 55
ArticleTitle: "حذف البيانات الوصفية من ملفات Excel – مستندات Aspose.Cells Cloud"
---

**نظرة عامة**  
تقوم عملية حذف البيانات الوصفية بإزالة جميع خصائص المصنف (القياسية والمخصصة) بشكل دائم من ملف(ات) Excel المرفوع وتعيد الملف(ات) المعالَج(ة) في الاستجابة.

**المتطلبات المسبقة**  
- رمز JWT صالح لـ Aspose.Cells Cloud (يمكن الحصول عليه عبر تدفق مصادقة OAuth 2.0).  
- إصدار واجهة برمجة التطبيقات **v3.0** (نقطة النهاية المستخدمة في هذا المثال).  
- لاستخدام SDKs، ثبّت SDK المناسب لـ Aspose.Cells Cloud بلغة برمجتك (مثلًا عبر NuGet أو Maven أو npm أو pip أو CPAN أو وحدات Go).

تقوم هذه واجهة برمجة تطبيقات REST بحذف **البيانات الوصفية** من ملف(ات) Excel واحدة أو أكثر. وتزيل خصائص المصنف مثل المؤلف والعنوان والبيانات المخصصة، ثم تعيد الملفات النظيفة.

## واجهة برمجة التطبيقات

```http
POST https://api.aspose.cloud/v3.0/cells/metadata/delete
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة مبنية على رمز JWT</a>.

### **معاملات الطلب**

| اسم المعامل | النوع | الموقع | الوصف |
|------------|-------|--------|--------|
| file | ملف | formData | ملف Excel المراد رفعه لحذف **البيانات الوصفية** |
| type | نص | استعلام | نوع العملية؛ ضعها على **all** لحذف جميع **البيانات الوصفية** |

يُعرّف <a href="https://apireference.aspose.cloud/cells/#/DeleteMetadata" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات قابلة للوصول عامًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/delete?type=all" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file=@file1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

قد تشمل **استجابات الخطأ** ما يلي:

- **400 طلب غير صالح** – ملف مفقود أو قيمة `type` غير صحيحة.
- **401 غير مخوّل** – رمز JWT غير صالح أو مفقود.
- **500 خطأ داخلي في الخادم** – خطأ في معالجة الخادم من الجهة الخلفية.

تعيد واجهة برمجة التطبيقات كائن JSON يحتوي على حقل `Error` يحتوي على التفاصيل لكل حالة.

| الرمز | المعنى | الوصف |
|-------|--------|--------|
| 200 | نجاح | تم حذف البيانات الوصفية، وتم إعادة الملف |
| 400 | طلب غير صالح | ملف مفقود أو `type` غير صالح |
| 401 | غير مخوّل | رمز JWT غير صالح أو مفقود |
| 500 | خطأ داخلي في الخادم | فشل في معالجة الخادم |

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يتعامل SDK مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للاطّلاع على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

توضح أمثلة الرمز التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}