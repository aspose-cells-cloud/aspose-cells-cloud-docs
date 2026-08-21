---
title: "إضافة صورة خلفية إلى دفتر عمل"
second_title: "مستند"
linktitle: "إضافة"
type: docs
url: /add-background-in-excel-file/
aliases:
  - /add-background-in-workbook/
  - /workbook/add-background/
  - /workbook/background/add/
keywords: "Aspose.Cells, إضافة صورة خلفية, واجهة برمجة تطبيقات Excel, REST, حزمة تطويرات سحابية, cURL, خلفية دفتر العمل"
description: "تعلم كيفية إضافة صورة خلفية إلى دفتر عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يتضمن المعلمات المطلوبة، تفاصيل المصادقة، مثال كامل لـ cURL، ومعلومات معالجة الأخطاء."
weight: 160
---

## واجهة برمجة التطبيقات REST

تقوم هذه واجهة برمجة التطبيقات REST بإضافة **صورة خلفية** إلى دفتر عمل Excel.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.


### معاملات الاستعلام

| اسم المعامل | النوع  | الوصف                                             |
| ------------ | ------ | -------------------------------------------------- |
| `picPath`    | نص     | مسار ملف الصورة المراد استخدامه كخلفية.          |
| `folder`     | نص     | المجلد الذي يحتوي على دفتر العمل الأصلي.         |
| `storageName`| نص     | اسم وحدة التخزين التي يوجد فيها الملف.            |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف                                                       |
| ------------ | ---- | ----------------------------------------------------------- |
| `datafile`   | ملف  | ملف دفتر العمل الذي سيتم تطبيق الخلفية عليه.               |

**معامل المسار** – `{name}` في عنوان URL يمثل **اسم ملف دفتر العمل** (مثلًا: `Book1.xlsx`).


### **الاستجابة**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                              |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح                        | تمت عملية تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح               | معاملات مفقودة أو غير صحيحة (مثلًا: نوع ملف غير مدعوم). |
| 401  | غير مصرّح به                | رمز JWT غير صالح أو مفقود. |
| 413  | حجم الحمولة كبير جدًا       | يتجاوز حجم الملف المرفوع الحد المسموح به. |
| 500  | خطأ داخلي في الخادم         | خطأ غير متوقع في الخادم. |
## كيفية استخدام واجهة PutWorkbookBackground API باستخدام حزم تطويرات البرمجيات (SDKs)

### مواصفات واجهة PutWorkbookBackground API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) واجهة برمجة تطبيقات عامة قابلة للوصول تتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يُظهر المثال التالي طلبًا كاملًا، بما في ذلك علامة تحميل الملف متعدد الأجزاء (multipart file upload) ورأس المصادقة المطلوب.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "datafile=@/path/to/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### استخدام حزم تطويرات Aspose.Cells Cloud SDKs

استخدام حزمة تطوير البرمجيات (SDK) هو أسرع طريقة للتطوير. فحزمة SDK تُجرّدك من التفاصيل منخفضة المستوى، ما يسمح لك بالتركيز على منطق أعمالك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطويرات Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر حزم تطويرات مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}

---