---
title: "إضافة نص إلى ملف إكسل: إدراج البيانات بكفاءة باستخدام واجهة برمجة تطبيقات الجداول الإلكترونية عبر الويب"
second_title: "مستند"
linktype: "إضافة نص"
type: docs
url: /ar/excel-add-text/
keywords: "إكسل، Aspose.Cells، إضافة نص، واجهة برمجة تطبيقات الجداول الإلكترونية، واجهة برمجة تطبيقات REST، Office Cloud، إدراج النص، واجهة برمجة تطبيقات إكسل"
description: "يضيف نصًا إلى موقع محدد في جدول إكسل عبر واجهة برمجة تطبيقات Aspose.Cells Cloud."
weight: 100
---

يضيف محتوى نصي إلى موقع محدد داخل جدول إكسل. يتطلب هذا الأمر كائنًا يُعرّف المحتوى النصي المراد إضافته والموقع الذي يجب إدراجه فيه.

## **واجهة برمجة تطبيقات إكسل: PostAddTextContent**

```
POST http://api.aspose.cloud/v3.0/cells/addtext
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.


### **وصف الوظيفة**

تقوم هذه الطريقة بإضافة نص جديد بأمان إلى الخلايا المحددة، وتدعم عدة أنماط لإدراج النص ومعالجة التنسيقات.

- **إضافة نص إلى بداية الخلايا المحددة**  
  يُضيف النص قبل محتوى جميع الخلايا المحددة، مما يضمن الاتساق في إدخال البيانات. مثالي لإضافة معرّفات أو تسميات مشتركة مثل رموز المنتجات أو الفئات أو البادئات.

- **إدراج أحرف قبل أو بعد نص محدد**  
  يضع أحرفًا قبل أو بعد النص المستهدف في الخلايا المحددة، مما يسمح لك بإنشاء محتوى منظم ومنسق بسهولة.

- **إضافة نفس النص إلى نهاية كل خلية محددة**  
  يضيف نصًا متطابقًا في نهاية عدة خلايا في عملية واحدة، مما يبسّط إدخال البيانات ويضمن مظهرًا موحدًا.

- **إدراج نص قبل أو بعد عدد محدد من الأحرف**  
  يُدرج نصًا بعد عدد معيّن من الأحرف من بداية أو نهاية كل خلية ضمن النطاق المستهدف. من الاستخدامات الشائعة تنسيق الرموز أو الطوابع الزمنية أو محدّدات مخصّصة.

### **معلّمات الطلب**

| اسم المعلّمة | النوع | الموقع | الوصف |
| ------------ | ----- | ------ | --------------------------------------------------------------------------- |
| addTextOptions | فئة | الجسم | يُحدّد محتوى النص والموقع الذي يجب إضافة النص إليه. |

### **الاستجابة**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "محتوى الملف: سلسلة مشفرة بـ base64"
}
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|------|-----------------------------|--------------------------------------------------|
| 200 | ناجح | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصرّح به | رمز JWT غير صالح أو مفقود. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | حدث خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostAddTextContent API باستخدام مكتبات SDK

### مواصفات واجهة PostAddTextContent API

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/TextProcessingController/PostAddTextContent) واجهة برمجة تطبيقات متاحة علنًا وتتيح لك إجراء تفاعلات REST مباشرة من خلال متصفح ويب.

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولّى مكتبة SDK معالجة التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostAddTextContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostAddTextContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostAddTextContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostAddTextContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostAddTextContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostAddTextContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostAddTextContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostAddTextContent.go" >}}
{{</ tab>}}
{{< /tabs >}}

---