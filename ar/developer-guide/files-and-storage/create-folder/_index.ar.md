---
title: "إنشاء مجلد – واجهة برمجة تطبيقات Aspose.Cells السحابية | إدارة التخزين في Excel"
second_title: "وثيقة"
ArticleTitle: "إنشاء مجلد – واجهة برمجة تطبيقات Aspose.Cells السحابية"
linktitle: "إنشاء مجلد"
type: docs
url: /ar/create-folder/
keywords: "Aspose.Cells، واجهة برمجة تطبيقات سحابية، إنشاء مجلد، إدارة التخزين، Excel"
description: "قم بإنشاء مجلد جديد في مساحة التخزين السحابية الخاصة بـ Aspose.Cells باستخدام طلب PUT بسيط. راجع تنسيق الطلب، المعلمات، والاستجابة وطريقة التعامل مع الأخطاء."
weight: 100
---

تشغيلة **createFolder** تقوم بإنشاء مجلد جديد في الموقع المحدّد ضمن مساحة التخزين السحابية المستخدمة من قِبل واجهة برمجة تطبيقات Excel. وتُعد هذه الوظيفة ضرورية لتنظيم الملفات وضمان هيكلية منظمة للمجلدات.

## **واجهة برمجة تطبيقات Excel: إنشاء مجلد**

### واجهة الويب (Web API)

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **الأمان والمصادقة**

تعمل واجهات برمجة تطبيقات Aspose.Cells السحابية بأمان وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات طلب واجهة **createFolder**

| اسم المعلمة | النوع   | الموقع | الإلزام | القيمة المبدئية | الوصف                                                                 |
| ------------ | ------ | -------- | -------- | ------- | --------------------------------------------------------------------------- |
| `path`         | نص (String) | مسار (Path) | نعم      | –       | مسار المجلد المراد إنشاؤه (مثال: `myFolder/subFolder`).                 |
| `storageName`  | نص (String) | استعلام (Query) | لا       | –       | اسم مساحة التخزين المراد استخدامها. إذا لم تُحدَّد، تُطبَّق مساحة التخزين الافتراضية. |

### وصف الاستجابة

```json
{}
```

تُعيد العملية محتوى فارغًا في حالة النجاح. وأكواد الحالة (HTTP Status Codes) الشائعة هي:

**أكواد الحالة (HTTP Status Codes)**

| كود HTTP | حالة HTTP           | الوصف                                                       |
| --------- | --------------------- | ----------------------------------------------------------------- |
| 200       | OK (نجاح)            | تم استدعاء واجهة الويب بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400       | Bad Request (طلب غير صحيح) | معلمات مفقودة أو غير صالحة (مثل: نوع ملف غير مدعوم).      |
| 401       | Unauthorized (غير مصرّح) | رمز JWT غير صالح أو مفقود.                                     |
| 413       | Payload Too Large (حجم البيانات كبير جدًا) | تجاوز حجم الملف المرفوع الحد المسموح.                                 |
| 500       | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                                          |

## مواصفات OpenAPI

تُعرِّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) واجهة برمجة تطبيقات متاحة عمومًا، وتتيح لك إجراء تفاعلات REST مباشرةً من خلال متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء استدعاءات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام حزم تطوير البرمجيات (SDKs) الخاصة بـ Aspose.Cells Cloud

استخدام حزمة تطوير البرمجيات (SDK) هو أفضل طريقة لتسريع عملية التطوير، إذ تُدير هذه الحزم التفاصيل منخفضة المستوى وتسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للاطّلاع على قائمة كاملة بحزم تطوير البرمجيات الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء استدعاءات إلى خدمات Aspose.Cells باستخدام حزم تطوير البرمجيات (SDKs) المختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{</tab>}}
{{< /tabs >}}