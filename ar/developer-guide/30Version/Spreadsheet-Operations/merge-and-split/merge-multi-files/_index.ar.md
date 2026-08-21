---
title: "دمج ملفات إكسل متعددة في ملف عمل واحد"
second_title: "مستند"
linktitle: "دمج ملفات إكسل متعددة"
type: docs
url: /ar/merge-multi-files-into-excel/
aliases: [  /ar/merge/multi-files/ ]
keywords: "Aspose.Cells Cloud، دمج ملفات إكسل متعددة، واجهة برمجة تطبيقات REST، دمج جداول البيانات، حزمة تطويرات سحابية"
description: "تعرّف على كيفية دمج ملفات عمل إكسل متعددة في ملف واحد باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST (الإصدار 3.0). يتضمن عنوان HTTPS، أمر cURL، أمثلة SDK، المعلمات المطلوبة، وتفاصيل معالجة الأخطاء."
weight: 32
---

## واجهة برمجة تطبيقات REST

تقوم هذه واجهة برمجة تطبيقات REST بدمج ملفات إكسل متعددة في ملف عمل إكسل واحد.

```bash
POST https://api.aspose.cloud/v3.0/cells/merge
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.


### المعلمات المطلوبة في الطلب

| اسم المعلمة  | النوع    | الموقع | الوصف                                                                       | مطلوبة |
| --------------- | ------- | -------- | --------------------------------------------------------------------------------- | -------- |
| files[]         | ملف    | formData | ملف عمل إكسل واحد أو أكثر ليتم دمجها. استخدم `file1`، `file2`، … في الطلب. | نعم      |
| format          | سلسلة نصية  | query    | التنسيق المطلوب للملف الناتج (مثل `xlsx`).                                             | نعم      |
| mergeToOneSheet | منطقي | query    | عدّلها إلى `true` لدمج كل أوراق العمل في ورقة واحدة؛ القيمة الافتراضية هي `false`.  | لا       |

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

**رموز حالات HTTP**

| الرمز | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح                          | تمت تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح                 | معلمات ناقصة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مصرّح به                | رمز JWT غير صالح أو ناقص. |
| 413  | حمل البيانات كبير جدًا           | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500  | خطأ داخلي في الخادم       | خطأ غير متوقع في الخادم. |
## كيفية استخدام واجهة PostMerge API باستخدام حزم تطوير البرامج (SDKs)

### مواصفات واجهة PostMerge API

تُعرّف <a href="https://apireference.aspose.cloud/cells/#/LightCells/PostMerge" rel="noopener noreferrer">مواصفة OpenAPI</a> واجهة برمجة تطبيقات قابلة للوصول العام، وتسمح لك بإجراء تفاعلات REST مباشرة من خلال متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء استدعاءات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file1=@file1.xlsx" \
  -F "file2=@file2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  {
    "Filename": "file1.xlsx",
    "FileSize": 274022,
    "FileContent": "-----Base64String--------"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام حزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud

يُعد استخدام حزمة تطوير البرامج (SDK) أفضل طريقة لتسريع عملية التطوير. فحزم التطوير تتعامل مع التفاصيل الدقيقة من المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للاطّلاع على قائمة كاملة بحزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات الويب Aspose.Cells باستخدام حزم تطوير مختلفة:

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}

---