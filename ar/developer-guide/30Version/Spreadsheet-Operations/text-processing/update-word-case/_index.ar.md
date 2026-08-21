---
title: "Aspose.Cells – واجهة برمجة التطبيقات لتحديث حالة الكلمات"
second_title: "مستند"
linktitle: "حالة الكلمة"
type: docs
url: /ar/post-update-word-case/
keywords: "Aspose.Cells، واجهة برمجة التطبيقات لتحديث حالة الكلمات، تحويل حالة النص، إكسل، CSV، جداول بيانات Google، واجهة برمجة التطبيقات REST"
description: "حوّل حالة النص في ملفات إكسل أو CSV أو جداول بيانات Google باستخدام واجهة برمجة التطبيقات PostUpdateWordCase في Aspose.Cells Cloud. تدعم التحويل إلى أحرف كبيرة أو صغيرة أو حالة العنوان أو تكبير الحرف الأول فقط."
weight: 100
ArticleTitle: "Aspose.Cells – وثائق واجهة برمجة التطبيقات لتحديث حالة الكلمات"
---

**إصدار الواجهة البرمجية:** 3.0

قد يؤدي وجود نصوص غير متسقة في حالة الأحرف (أحرف كبيرة أو صغيرة) داخل الجداول المكتبية (مثل إكسل، جداول بيانات Google، CSV) إلى إحداث إحباط، خاصةً عند التعامل مع مجموعات بيانات كبيرة. وتُعد **واجهة PostUpdateWordCase Web API** أداةً تلقائيةً لتحويل حالات النص، مما يضمن جودة نظيفة وموحّدة للبيانات مع أقل جهد ممكن.

## **واجهة برمجة التطبيقات عبر الويب للجداول المكتبية – واجهة برمجة التطبيقات لتحديث حالة الكلمات**

```http
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```

### **الأمان والمصادقة**

تُعتبر واجهات برمجة التطبيقات في Aspose.Cells Cloud آمنة، وتشترط <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة باستخدام رمز JWT</a>.

### **وصف الوظيفة**

تُعنى واجهة برمجة التطبيقات PostUpdateWordCase بحلّ مشكلة شائعة تتمثل في عدم اتساق حالة الأحرف في الجداول المكتبية، وهو ما قد يؤثر بشكل كبير على تحليل البيانات ومعالجتها. وتُحقّق هذه الواجهة البرمجية التحويل التلقائي لحالات الأحرف، مما يضمن أن تكون بياناتك نظيفة ومُوحّدة وجاهزة لأي تعديل أو تحليل لاحق.

- **تحويل تلقائي لحالة الأحرف**
  - **تحويل الأحرف الكبيرة إلى صغيرة** – تحويل جميع الأحرف الكبيرة إلى صغيرة.
  - **تحويل الأحرف الصغيرة إلى كبيرة** – تحويل جميع الأحرف الصغيرة إلى كبيرة.
  - **تكبير الحرف الأول فقط** – تكبير الحرف الأول من كل كلمة.
  - **حالة العنوان (Title Case)** – تحويل النص إلى حالة العنوان، حيث يُكبّر الحرف الأول من كل كلمة رئيسية.

- **دعم تنسيقات متعددة** – تعمل الواجهة البرمجية مع مجموعة واسعة من تنسيقات الجداول المكتبية، بما في ذلك إكسل، OpenOffice، JSON، CSV، وغيرها. ويجعل هذا التنوّع منها أداةً مناسبة لمختلف احتياجات معالجة البيانات.

### **معلمات الطلب**

| اسم المعلَمة       | النوع   | الموقع         | الوصف                                                                                                               |
| ----------------- | ------ | ------------ | ------------------------------------------------------------------------------------------------------------------------- |
| `wordCaseOptions` | كائن   | جسم الطلب     | خيارات تُعرّف عملية التحويل المطلوبة لحالة الأحرف، مثل النطاق المصدر ونوع الحالة المستهدفة والإعدادات الإضافية. |

**هيكل `wordCaseOptions`**

```json
{
  "Range": "A1:B10", // النطاق بالصيغة المعتادة في إكسل للمعالجة (إجباري)
  "CaseType": "Upper", // القيم المسموح بها: Upper، Lower، Capitalize، Title (إجباري)
  "IgnoreBlank": true // قيمة منطقية، اختيارية – عند التعيين إلى true، تُترك الخلايا الفارغة دون تغيير
}
```

**مثال على جسم الطلب**

```json
{
  "Range": "A1:B10",
  "CaseType": "Upper",
  "IgnoreBlank": true
}
```

- **النطاق (Range)** – النطاق الخلوية الذي سيتم تطبيق عملية تحويل حالة الأحرف عليه (مثل `A1:C5`).
- **نوع الحالة (CaseType)** – نوع عملية التحويل. القيم المسموح بها هي: `Upper` (كبير)، `Lower` (صغير)، `Capitalize` (تكبير الحرف الأول فقط)، و`Title` (حالة العنوان).
- **تجاهل الفارغة (IgnoreBlank)** – إذا كانت القيمة `true`، تُتجاهل الخلايا الفارغة؛ القيمة الافتراضية هي `false`.

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

- **Filename** – اسم الملف الذي تم معالجته.
- **FileSize** – حجم الملف بالبايت.
- **FileContent** – محتوى الملف بعد التحويل، مشفرًا بتقنية Base64.

**رموز حالة HTTP**

| الرمز | المعنى                       | الوصف                                                |
|------|-----------------------------|------------------------------------------------------|
| 200  | ناجح (OK)                   | تم تطبيق التصفية بنجاح؛ وتحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request)  | معلمات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مُصادق عليه (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413  | حمل البيانات كبير جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة برمجة التطبيقات PostUpdateWordCase باستخدام مكتبات SDK

### مواصفات واجهة برمجة التطبيقات PostUpdateWordCase

تُعرّف <a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات عامة قابلة للوصول وتسمح لك بإجراء تفاعلات REST مباشرة من خلال متصفح الويب.

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

يعتبر استخدام مكتبات SDK أفضل طريقة لتسريع عملية التطوير. فالمكتبات تتعامل مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة مُكتملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر الأمثلة التالية كيفية استدعاء خدمات Aspose.Cells عبر الإنترنت باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostUpdateWordCase.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostUpdateWordCase.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostUpdateWordCase.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostUpdateWordCase.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostUpdateWordCase.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostUpdateWordCase.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostUpdateWordCase.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostUpdateWordCase.go" >}}
{{</ tab>}}
{{</ tabs >}}
---