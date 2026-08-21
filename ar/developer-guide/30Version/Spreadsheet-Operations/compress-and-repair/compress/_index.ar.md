---
title: "ضغط البيانات في ملف إكسل"
ArticleTitle: "ضغط البيانات في ملف إكسل – واجهة Aspose.Cells Cloud API"
second_title: "مستند"
linktitle: "ضغط ملفات إكسل"
type: docs
url: /ar/compress-excel-files/
aliases: [  /ar/compress/ ]
keywords: "ضغط ملف إكسل، aspose cells cloud، ضغط إكسل، ضغط جداول البيانات، واجهة rest api، ضغط الملفات"
description: "اضغط ملفات إكسل (XLS و XLSX و XLSM و XLSB و ODS) باستخدام واجهة Aspose.Cells Cloud REST API. اضبط مستوى الضغط، وتعامل مع ملفات متعددة، وادمج عبر SDKs."
weight: 39
---

## واجهة PostCompress API لخدمات الويب Aspose.Cells Cloud

**المتطلبات الأساسية:**  
- مطلوب رمز JWT صالح للمصادقة.  
- تنسيقات الملفات المدعومة هي: XLS و XLSX و XLSM و XLSB و ODS.  
- أقصى حجم مسموح به للملف هو 500 ميغابايت لكل طلب (يخضع لقيود الخدمة).

تقوم هذه الواجهة REST بضغط بيانات ملف إكسل.

- ضغط ملفات XLS و XLSX و XLSM و XLSB و ODS  
- ضغط سريع لعدة ملفات جداول بيانات إكسل  
- اختيار مستوى الضغط  
- دعم ملفات متعددة  

### نقطة نهاية واجهة الويب API

```http
POST https://api.aspose.cloud/v3.0/cells/compress
```

### **الأمان والمصادقة**

تُعد واجهات Aspose.Cells Cloud API آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### مُعَيَّنات الطلب (Request Parameters)

| اسم المُعَيَّن | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|----------------|---------|-----------------------------|------------------------------------------------------------|
| file | ملف | formData | الملف المراد رفعه |
| CompressLevel | عدد صحيح | query | مستوى الضغط (0–100)، وكلما زادت القيمة زادت قوة الضغط |

### مُعَيَّن جسم الطلب (Request Body Parameter)

| اسم المُعَيَّن | النوع | الوصف |
| -------------- | ---- | ---------------------------------------------- |
| data | ملف | المحتوى الثنائي لملف المصنف المراد ضغطه. |

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

*ملاحظة:* يحتوي `FileContent` على المصنف المضغوط مُشفَّرًا كسلسلة Base64. ويعكس طول السلسلة حجم الملف المضغوط؛ يمكنك فك التشفير باستخدام أدوات Base64 القياسية لاسترجاع ملف إكسل ثنائي.

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|------|-----------------------------|--------------------------------------------------|
| 200 | OK (تم بنجاح) | تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | مُعَيَّنات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصادَق | رمز JWT غير صالح أو مفقود. |
| 413 | حمل البيانات كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostCompress API مع SDKs

### مواصفات واجهة PostCompress API

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostCompress) واجهة برمجة تطبيقات قابلة للوصول العام، وتسمح بإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات لواجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
# استخدم HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v3.0/cells/compress?CompressLevel=88" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة لتسريع عملية التطوير. فتقوم SDK بإخفاء التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCompress.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCompress.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCompress.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCompress.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCompress.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCompress.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCompress.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCompress.go" >}}

{{< /tab >}}

{{< /tabs >}}