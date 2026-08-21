---
title: "استرجاع البيانات الوصفية من ملفات Excel"
second_title: "مستند"
linktitle: "استرجاع دون استخدام التخزين"
type: docs
url: /ar/metadata/get/
keywords: "Aspose.Cells, Excel, البيانات الوصفية, REST API, SDK في السحابة"
description: "استرجاع البيانات الوصفية المدمجة أو المخصصة من أوراق عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API. يشمل تنسيق الطلب، المعلمات، كود مثال لـ SDK، ومعالجة الأخطاء."
weight: 23
ArticleTitle: "استرجاع البيانات الوصفية من ملفات Excel - واجهة Aspose.Cells Cloud API"
---

تقوم هذه الواجهة **REST API** باسترجاع **البيانات الوصفية** من ملف أو أكثر من ملفات Excel.  
يجب أن يتضمّن الطلب رأس `Authorization: Bearer <access_token>` يُحصل عليه عبر تدفق بيانات اعتماد العميل OAuth 2.0.

**المتطلبات المسبقة**: لاستدعاء هذه النهاية (endpoint)، يجب أن تمتلك رمز وصول (access token) ساري المفعول تم الحصول عليه من نقطة نهاية رموز OAuth 2.0 الخاصة بـ Aspose Cloud. مثال على طلب curl لاسترداد رمز وصول:

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
```

## واجهة REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/get
```

### معلمة الاستعلام (Query Parameter)

| اسم المعلمة | النوع   | الوصف                                                               |
| ------------ | ------ | ------------------------------------------------------------------------- |
| type        | string | `ALL` / `BuiltIn` / `Custom` – يحدّد مجموعات البيانات الوصفية المراد إعادتها. |

### معلمة جسم الطلب

| اسم المعلمة | النوع      | الوصف                                                         |
| ------------ | --------- | ------------------------------------------------------------------- |
| ملف Excel    | ملف بيانات | ملف Excel المزوّد كجزء أول من الطلب متعدد الأجزاء (multipart request). |

### الاستجابة

```json
[
  {
    "Name": "Author",
    "Value": "John Doe",
    "BuiltIn": true,
    "IsReadOnly": false
  },
  {
    "Name": "CustomProp1",
    "Value": "Custom Value",
    "BuiltIn": false,
    "IsReadOnly": false
  }
]
```

| الرمز | المعنى                 | الحالة                          |
|------|-------------------------|-----------------------------------|
| 200  | نجاح                    | تم إرجاع البيانات الوصفية.                |
| 400  | طلب غير صالح           | ملف مفقود أو استعلام غير صحيح.    |
| 401  | غير مُصادَق عليه        | رمز وصول غير صالح أو مفقود.         |
| 404  | غير موجود              | الملف المحدّد غير موجود.         |
| 500  | خطأ داخلي في الخادم    | فشل غير متوقّع في الخادم.        |

تُعيد الواجهة هذه الرموز القياسية لحالة HTTP مع كائن JSON للاستجابة بالخطأ عند الضرورة.

### عائلة SDK في السحابة

استخدام SDK يُسرّع التطوير من خلال التعامل مع التفاصيل منخفضة المستوى. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKات مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}