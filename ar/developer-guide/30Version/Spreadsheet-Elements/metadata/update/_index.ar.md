---
title: "تحديث البيانات الوصفية"
second_title: "مستند"
linktitle: "تحديث بدون استخدام التخزين"
type: docs
url: /ar/metadata/update/
keywords: "البيانات الوصفية، إكسل، Aspose.Cells Cloud، REST API، تحديث، جدول بيانات"
description: "تتيح واجهة Aspose.Cells Cloud REST تحديث البيانات الوصفية في ملفات إكسل. وتدعم مجموعة واسعة من SDKs (C#، Java، Python، Ruby، Go، إلخ) لدمجٍ سلس عبر لغات البرمجة المختلفة."
weight: 35
ArticleTitle: "تحديث البيانات الوصفية – مستندات واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة REST بتحديث **البيانات الوصفية** في ملفات إكسل متعددة.

**المتطلبات المسبقة:** حساب Aspose Cloud نشط، ورمز وصول JWT صالح، وملفات إكسل المراد رفعها.

## واجهة برمجة التطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/update
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل         | النوع   | الموقع          | الوصف                                        |
| ------------------ | ------ | --------------- | --------------------------------------------- |
| file               | ملف    | formData        | ملف إكسل المراد رفعه.                         |
| DocumentProperties | كائن   | جسم الطلب (JSON) | خصائص المستند المراد تعيينها لملف إكسل.     |

**ملاحظات:** يمكن رفع ما يصل إلى 10 ملفات في طلب واحد. التنسيقات المدعومة تشمل `.xlsx` و`.xls` و`.csv`. ولا يجوز أن يتجاوز حجم الطلب الإجمالي 100 ميغابايت.

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/PostMetadata) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/update" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx' \
  -d '[{ "name": "test", "value": "test" }]'
```

يتطلب الطلب رأس **Authorization** يحتوي على رمز Bearer JWT. تأكد من توليد الرمز باستخدام بيانات اعتماد عميل Aspose Cloud الخاصة بك.

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

يُعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. فتتولى SDK معالجة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب Aspose.Cells باستخدام مكتبات SDK متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}

**انظر أيضًا:**  
- [الحصول على البيانات الوصفية](/metadata/get/)  
- [حذف البيانات الوصفية](/metadata/delete/)  
---