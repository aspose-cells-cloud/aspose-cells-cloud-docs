---
title: "واجهة برمجة تطبيقات Aspose.Cells لقص المحتوى – إزالة المسافات وفواصل الأسطر من ملفات Excel"
second_title: "مستند"
linktype: "قص المحتوى"
type: docs
url: /ar/spreadsheet-trim-content/
keywords: "Aspose.Cells، واجهة برمجة تطبيقات قص المحتوى، تنظيف بيانات Excel، إزالة المسافات من Excel، إزالة فواصل الأسطر، تنظيف بيانات الجداول"
description: "استخدم واجهة برمجة تطبيقات PostTrimContent في Aspose.Cells Cloud لتنظيف المسافات الإضافية وفواصل الأسطر والأحرف غير المرغوب فيها من خلايا Excel تلقائيًا. اعرف عن النهاية (Endpoint)، وتنسيق الطلب، وعينات الكود، ومعالجة الأخطاء."
weight: 100
---

## **واجهة برمجة تطبيقات Excel عبر الويب: PostTrimContent**

تُعالِج واجهة **PostTrimContent** برمجيًا وتقصّ المحتوى داخل نطاق مُحدّد في جدول بيانات. وتُزيل المسافات الإضافية وفواصل الأسطر وغيرها من الأحرف غير الضرورية من محتوى الخلايا المُحددة، ما يجعلها مفيدة في تنظيف إدخالات البيانات وضمان تنسيق مُوحّد للجداول.

```http
POST https://api.aspose.cloud/v3.0/cells/trimcontent
```

### **الأمان والمصادقة**

تُقدِّم واجهات برمجة تطبيقات Aspose.Cells Cloud أمانًا عاليًا وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة مبنية على رمز JWT</a>.

### **وصف الوظيفة**

- **الكفاءة** – تقصّ المحتوى داخل النطاق المُحدّد فقط، ما يوفر الوقت والموارد بتجنب العمليات غير الضرورية على ورقة العمل بأكملها.
- **المرونة** – تسمح للمستخدمين بتحديد النطاق الدقيق للخلايا المراد معالجتها، مما يلبي متطلبات وأحجام مجموعات البيانات المتنوعة.
- **سلامة البيانات** – تزيل المسافات الإضافية وفواصل الأسطر، مما يساعد على الحفاظ على بيانات متسقة وموثوقة لغرض التحليل والتقارير.
- **سهولة الاستخدام** – تتكامل ببساطة مع الحد الأدنى من الإعدادات، مما يجعلها مناسبة للمطورين ومستخدمي نهاية المطاف على حد سواء.

### **مُعاملات الطلب**

| اسم المُعامل          | النوع   | الموقع | الوصف                                                                 |
|----------------------|---------|--------|------------------------------------------------------------------------|
| trimContentOptions   | كلاس    | الجسم | خيارات تحدّد كيفية قص المحتوى (مثل النطاق المستهدف، وضع القص).         |

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

| الرمز | المعنى                       | الوصف                                                                   |
|-------|------------------------------|--------------------------------------------------------------------------|
| 200   | ناجح (OK)                    | تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.                 |
| 400   | طلب غير صالح (Bad Request)   | مُعاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم).                   |
| 401   | غير مصرّح (Unauthorized)     | رمز JWT غير صالح أو مفقود.                                              |
| 413   | حملة البيانات كبيرة جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح.                                |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                              |

## كيفية استخدام واجهة PostRemoveCharacters API باستخدام SDKs

### مواصفات واجهة PostRemoveCharacters API

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/TextProcessingController/PostTrimContent) واجهة برمجة تطبيقات متاحة علنًا وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

### استخدام SDKs لـ Aspose.Cells Cloud

استخدام SDKs هو أفضل طريقة لتسريع عملية التطوير. فتتولى SDKs تفاصيل المستوى المنخفض تلقائيًا، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK متنوعة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostTrimContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostTrimContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostTrimContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostTrimContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostTrimContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostTrimContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostTrimContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostTrimContent.go" >}}
{{</ tab>}}
{{< /tabs >}}

_آخر تحديث: 2026-03-30_