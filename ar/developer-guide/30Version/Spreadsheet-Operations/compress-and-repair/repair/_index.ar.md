---
title: "إصلاح ملفات إكسل"
second_title: "مستند"
type: docs
linktitle: "إصلاح ملفات إكسل"
url: /repair-excel-files/
keywords: "Aspose Cells, API إصلاح إكسل, ملفات XLSX تالفة, استرداد جداول البيانات, API سحابية"
description: "استخدم واجهة Aspose.Cells Cloud REST API لإصلاح ملفات إكسل التالفة (XLS، XLSX، XLSM، XLSB، ODS). ارفع ملفًا واحدًا أو عدة ملفات، واختر تنسيق الإخراج، واحصل على الملفات المُصلحة بصيغة Base64. لا حاجة لتثبيت أي شيء."
weight: 39
---

تتيح لك هذه الواجهة البرمجية (REST API) **إصلاح** ملفات إكسل.

- إصلاح تنسيقات جداول البيانات مثل XLS وXLSX وXLSM وXLSB وODS وغيرها.  
- يدعم رفع ملفات متعددة في طلب واحد.

تقوم خدمة إصلاح ملفات إكسل من Aspose.Cells Cloud باسترداد البيانات من ملفات إكسل التالفة عبر الإنترنت دون أي تثبيت. تُعد ملفات إكسل التالفة مشكلة لأنها لا يمكن فتحها. يمكنك تجربة تطبيق Aspose.Cells Cloud لإصلاح ملفات إكسل لاسترداد البيانات من هذه الملفات.

## واجهة REST API

يقوم الطرف النهائي **إصلاح ملفات إكسل** بإصلاح ملفات جداول البيانات التالفة وإعادة محتواها المُصلَح.

```bash
POST https://api.aspose.cloud/v3.0/cells/repair
```

### **الأمان والمصادقة**

تُعد واجهات Aspose.Cells Cloud API آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| file | ملف | formData (multipart) | الملف المراد رفعه |
| format | نص | query | تنسيق الإخراج المرغوب. إذا تم حذفه (null)، يصبح تنسيق الإخراج افتراضيًا هو نفس تنسيق الملف المدخل. |

### **الاستجابة**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[اسم الملف المدمج]",
    "Filesize" : [حجم الملف],
    "FileContent" : "[Base64String]"
}
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|--------|--------|
| 200 | ناجح | تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صحيح | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصرّح به | رمز JWT غير صالح أو مفقود. |
| 413 | حمل البيانات كبير جدًا | يتجاوز حجم الملف المرفَع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## كيفية استخدام PostRepair API باستخدام حزم تطوير البرمجيات (SDKs)

### مواصفات PostRepair API

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) واجهة برمجة تطبيقات متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى API السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/repair" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@file1.xlsx' \
  -F 'file2=@file2.xlsx'
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
    },
    {
      "Filename": "file2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

عند النجاح، تُعيد الخدمة كود HTTP 200 مع حمولة JSON تحتوي على مصفوفة `Files`. وفي حالات الخطأ، تستخدم الواجهة رموز الحالة القياسية لـ HTTP:

- **400 Bad Request** – معاملات غير صحيحة أو ملف لا يمكن إصلاحه.  
- **401 Unauthorized** – رمز JWT مفقود أو غير صالح.  
- **413 Payload Too Large** – يتجاوز حجم الملف المرفَع الحد المسموح به.  
- **500 Internal Server Error** – فشل غير متوقع من جانب الخادم.

## عائلة حزم تطوير البرمجيات السحابية

استخدام حزمة تطوير البرمجيات (SDK) هو أفضل طريقة لتسريع عملية التطوير. وتتولى حزمة التطوير معالجة التفاصيل من المستوى المنخفض، وتسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم Aspose.Cells Cloud SDK.

يُظهر أمثلة الرمز التالية كيفية استدعاء خدمات Aspose.Cells عبر حزم تطوير برمجيات متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}