---
title: "التحقق من وجود مخزن – واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 4.0)"
second_title: "مستند"
ArticleTitle: "إدارة ملفات إكسل عبر السحابة – التحقق من وجود المخزن"
linktype: "exists"
type: docs
url: /storage-exists/
keywords: "Aspose.Cells, وجود المخزن, واجهة برمجة تطبيقات التخزين السحابي, REST, إكسل"
description: "التحقق من وجود حاوية تخزين في Aspose.Cells Cloud. تعلّم نقطة النهاية GET /v4.0/cells/storage/{storageName}/exist، والمتغيّرات المطلوبة، وتنسيق الاستجابة، وشاهد أمثلة لاستخدام SDKs بلغات C#، Java، Python، والمزيد."
weight: 100
---

تُستخدم واجهة برمجة التطبيقات `storageExists` للتحقق مما إذا كان المخزن المحدّد موجودًا في خدمة Aspose.Cells Cloud. تُعتبر هذه الوظيفة ضرورية لضمان سير العمليات المعتمدة على المخزن دون أخطاء.
**الملخص** – تتيح نقطة النهاية `storageExists` تأكيد ما إذا كانت حاوية التخزين المحدّدة متاحة في Aspose.Cells Cloud. يُنصح باستخدامها قبل تنفيذ العمليات المرتبطة بالملفات لتفادي الأخطاء أثناء التشغيل.

## التحقق من وجود المخزن (storageExists)

### واجهة برمجة التطبيقات عبر الويب

```
GET https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **الأمان والمصادقة**

تُقدّم واجهات برمجة تطبيقات Aspose.Cells Cloud بشكل آمن وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة عبر رمز JWT</a>.

### متغيّرات الطلب

| اسم المتغيّر | النوع   | الموقع | الوصف                                     |
| ------------ | ------ | -------- | ----------------------------------------------- |
| storageName  | String | Path     | اسم المخزن الذي سيتم التحقق من وجوده. |

### **الاستجابة**

```json
{
  "Name": "StorageExist",
  "Description": ["تُشير إلى ما إذا كان المخزن المحدّد موجودًا أم لا."],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "تُشير إلى ما إذا كان المخزن موجودًا.",
        "ترجع هذه الخاصية القيمة true إذا كان المخزن موجودًا؛ وإلا ترجع false."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

**رموز حالات HTTP**

| الرمز | المعنى               | الوصف                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | نجاح (OK)            | تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request) | غياب أو خطأ في المتغيّرات (مثل نوع ملف غير مدعوم).      |
| 401  | غير مفوّض (Unauthorized)  | رمز JWT غير صالح أو مفقود.                                     |
| 413  | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح.                                 |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                          |

## كيفية استخدام واجهة برمجة التطبيقات الخاصة بالتحقق من وجود المخزن باستخدام SDKs؟

### مواصفات OpenAPI

تُعرّف <a href="https://reference.aspose.cloud/cells/#/StorageController/StorageExists" rel="nofollow noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات قابلة للوصول بشكل عام، مما يسمح للمطورين بالتفاعل بسلاسة مع واجهة REST API مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو الطريقة الأكثر كفاءة لتسريع عملية التطوير. فتُجرّد SDKs المطورين من تفاصيل التنفيذ منخفضة المستوى، مما يمكّنهم من التركيز على مهام مشاريعهم. للاطّلاع على قائمة شاملة بـ SDKs المتاحة الخاصة بـ Aspose.Cells Cloud، يُرجى زيارة <a href="https://github.com/aspose-cells-cloud" rel="nofollow noopener noreferrer">مستودع GitHub</a>.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات API لخدمات الويب Aspose.Cells باستخدام SDKs مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{</tab>}}
{{< /tabs >}}