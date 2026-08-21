---
title: "استبدال نصوص من ملفات Excel"
second_title: "مستند"
linktitle: "استبدال دون استخدام التخزين"
type: docs
url: /ar/replace/
keywords: "استبدال النصوص في Excel، Aspose.Cells Cloud، REST API، استبدال في جدول البيانات، API، استبدال النصوص في ملف Excel"
description: "استخدم Aspose.Cells Cloud REST API لاستبدال النصوص الموجودة بقيم جديدة في ملفات Excel. يدعم SDKs لكل من C#، Java، Python، Node.js، PHP، Ruby، Go، و Perl."
weight: 80
---

## REST API

يقوم هذا الـ REST API باستبدال البيانات في ملفات Excel.

```bash
POST https://api.aspose.cloud/v3.0/cells/replace
```

### الأمان والمصادقة

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتشترط [المصادقة باستخدام رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### معاملات الطلب

| اسم المعامل | النوع   | الموقع             | الوصف                                   |
|------------|--------|--------------------|------------------------------------------|
| **file**   | ملف    | formData (multipart) | ملف Excel المراد معالجته.                |
| **text**   | نص    | query              | السلسلة النصية المراد استبدالها.         |
| **newtext**| نص    | query              | النص البديل.                             |
| **password**| نص    | query              | كلمة المرور لورقة عمل محمية (اختياري).   |
| **sheetname**| نص   | query              | اسم ورقة العمل المستهدفة (اختياري).      |

### **الاستجابة**

```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename" : "[اسم الملف1]",
      "Filesize" : [حجم الملف],
      "FileContent" : "[Base64String]"
    },
    {
      "Filename" : "[اسم الملف2]",
      "Filesize" : [حجم الملف],
      "FileContent" : "[Base64String]"
    },
    {
      "Filename" : "[اسم الملف3]",
      "Filesize" : [حجم الملف],
      "FileContent" : "[Base64String]"
    }
  ]
}
```

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                            |
|-------|----------------------------|--------------------------------------------------|
| 200   | نجاح (OK)                  | تمت عملية التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401   | غير مُصادَق (Unauthorized)  | رمز JWT غير صالح أو مفقود.                      |
| 413   | حمل البيانات كبير جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                         |

## كيفية استخدام API PostReplace باستخدام حزم التطوير (SDKs)

### مواصفات API PostReplace

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostReplace) واجهة برمجة تطبيقات مُتاحة للعامة وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يُظهر المثال التالي كيفية إجراء مكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/replace?text=1&newtext=aspose.cells.cloud" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxx1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxx2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة حزم التطوير السحابية

استخدام حزمة التطوير (SDK) هو أفضل طريقة لتسريع عملية التطوير. فحزمة التطوير تُعالِج التفاصيل منخفضة المستوى وتركّز أنت على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على قائمة كاملة بحزم تطوير Aspose.Cells Cloud.

يوضح أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات الويب الخاصة بـ Aspose.Cells باستخدام حزم تطوير مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}

---