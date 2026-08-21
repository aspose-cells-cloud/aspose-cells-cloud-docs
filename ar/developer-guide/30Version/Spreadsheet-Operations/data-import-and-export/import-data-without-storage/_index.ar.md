---
title: "استيراد البيانات دون استخدام التخزين – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "المستند"
linktitle: "استيراد البيانات دون استخدام التخزين"
type: docs
url: /ar/import/without-using-storage/
aliases: [  /ar/import-data-in-excel-worksheet-without-using-storage/ ]
keywords: "Aspose.Cells، واجهة برمجة تطبيقات السحابة، استيراد البيانات دون استخدام التخزين، واجهة برمجة تطبيقات استيراد Excel، استيراد REST"
description: "تعلم كيفية استيراد البيانات دون استخدام التخزين في ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. يتضمن تنسيق الطلب، المعلّمات، مثال cURL، كود SDK، ومعالجة الأخطاء."
weight: 10
ArticleTitle: "استيراد البيانات دون استخدام التخزين – واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

يمكن أن يكون استيراد بيانات Excel معقدًا نظرًا لتأثير العديد من العوامل على النتيجة. ويجب أخذ جميع هذه العوامل بعين الاعتبار أثناء عملية **الاستيراد**. وتُبسّط Aspose.Cells Cloud عملية استيراد تنسيقات وأنواع بيانات متنوعة إلى ملف Excel بجودة احترافية.

تقوم هذه الواجهة البرمجية REST باستيراد **البيانات** إلى ملف Excel.

## واجهة PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **الأمان والمصادقة**

تعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **مُعلّمات الطلب:**

| اسم المعلّمة | النوع          | الموقع  | الوصف                                                                                                                                     |
| ------------ | ------------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| file         | ملف           | formData | ملف Excel المرفوع.                                                                                                                         |
| ImportOption | ImportOption  | جسم JSON | كائن JSON يُعرّف البيانات المراد استيرادها، ونوعها (مثل `IntArray` أو `DoubleArray` أو `StringArray`)، وموقعها داخل ورقة العمل. |

تُوصَف مُعلّمات **ImportOption** في **مرجع خيار استيراد البيانات** [/cells/import/#import-data-option-parameter](/cells/import/#import-data-option-parameter).

**المتطلبات المسبقة:**  
يجب إنشاء رمز JWT صالح مسبقًا، ولا يجوز أن يتجاوز حجم الملف الحد الأقصى للخدمة (عادةً 100 ميغابايت). وتشمل تنسيقات الملفات المدعومة XLS وXLSX وCSV وODS. وتأكد من تثبيت SDK المناسب إذا كنت تفضّل الوصول البرمجي.

### الاستجابة

```json
{
  "Status":"OK",
  "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                                                 |
|-------|-----------------------------|------------------------------------------------------------------------|
| 200   | ناجح (OK)                   | تم تطبيق العامل بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.             |
| 400   | طلب غير صالح (Bad Request)  | مُعلّمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).                 |
| 401   | غير مُصادَق (Unauthorized)   | رمز JWT غير صالح أو مفقود.                                             |
| 413   | حمل البيانات كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به.                             |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                              |

**ملاحظات:**  
عند إرسال الطلب، يتم تعيين رأس `Content-Type: multipart/form-data` تلقائيًا بواسطة العلامة `-F`. وللحملات الكبيرة، فكّر في ضغط البيانات قبل الاستيراد وتطبيق منطق إعادة المحاولة للأخطاء المؤقتة.

## كيفية استخدام واجهة PostImportData API باستخدام حزم تطوير البرامج (SDKs)

###仕様 واجهة PostImportData API

يُعرّف [仕様 OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) واجهة برمجة تطبيقات متاحة علنًا ويسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة تطبيقات السحابة باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/import" \
  -X POST \
  -H "Authorization: Bearer <jwt_token>" \
  -F "file=@file.xlsx" \
  -F "ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"ImportDataType\":\"IntArray\"}"
```

*تقوم العلامة `-F` بتعيين `Content-Type: multipart/form-data` تلقائيًا.*  

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status":"OK",
  "Code":200
}
```

{{< /tab >}}

{{< /tabs >}}


### استخدام حزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولّى SDK تفاصيل المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر الأمثلة التالية كيفية استدعاء خدمات الويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostImportData.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostImportData.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostImportData.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostImportData.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostImportData.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostImportData.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostImportData.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostImportData.go" >}}

{{< /tab >}}

{{< /tabs >}}
---