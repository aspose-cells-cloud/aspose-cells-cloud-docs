---
title: "واجهة Aspose.Cells Cloud Web API – استخراج النص"
second_title: "Aspose.Cells Cloud –Short‑Code عبر الإنترنت"
linktitle: "استخراج النص"
type: docs
url: /extract-text/
keywords: "Aspose.Cells Cloud, استخراج النص, Excel API, استخراج نص الخلايا, REST API"
description: "استخراج سلاسل فرعية أو أرقام أو أحرف من خلايا ملفات إكسل باستخدام واجهة Aspose.Cells Cloud API. يدعم الاستخراج بناءً على النص السابق/اللاحق، أو بناءً على الموقع، أو كتابة الناتج مباشرةً في نطاق جديد."
weight: 100
ArticleTitle: "توثيق API استخراج النص لـ Aspose.Cells Cloud"
---

يقوم باستخراج السلاسل الفرعية أو الأحرف أو الأرقام من خلية في ورقة العمل إلى خلية أخرى، ما يلغي الحاجة إلى صيغ معقدة مثل FIND أو MIN أو LEFT أو RIGHT.

## **واجهة ExtractText API**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/extract/text
```

### **الأمان والمصادقة**

تُعتبر واجهات Aspose.Cells Cloud API آمنة، وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### معاملات طلب **extractText** API

| اسم المعامل      | النوع    | الموقع               | الوصف                                                                                                                                           |
| ---------------- | -------- | -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet      | ملف     | FormData             | تحميل ملف ورقة العمل.                                                                                                                            |
| extractTextType  | نص (String) | استعلام (Query)      | تعداد يُشير إلى وضع الاستخراج. القيم المسموح بها: `Before`، `After`، `BeforePosition`، `AfterPosition`.                                          |
| beforeText       | نص (String) | استعلام (Query)      | النص الذي يجب أن يظهر **قبل** السلسلة الفرعية المستخرجة. يُستخدم عندما تكون `extractTextType=Before`.                                          |
| afterText        | نص (String) | استعلام (Query)      | النص الذي يجب أن يظهر **بعد** السلسلة الفرعية المستخرجة. يُستخدم عندما تكون `extractTextType=After`.                                           |
| beforePosition   | عدد صحيح (Integer) | استعلام (Query)      | عدد الأحرف المراد إرجاعها من الجانب الأيسر للخلية. يُستخدم عندما تكون `extractTextType=BeforePosition`.                                        |
| afterPosition    | عدد صحيح (Integer) | استعلام (Query)      | عدد الأحرف المراد إرجاعها من الجانب الأيمن للخلية. يُستخدم عندما تكون `extractTextType=AfterPosition`.                                         |
| outPositionRange | نص (String) | استعلام (Query)      | النطاق الهدف (مثل `Sheet1!A1`) الذي سيُكتب فيه النص المستخرج.                                                                                   |
| worksheet        | نص (String) | استعلام (Query)      | اسم ورقة العمل التي تحتوي على الخلية المصدر.                                                                                                    |
| range            | نص (String) | استعلام (Query)      | الخلية أو النطاق المصدر (مثل `A1`).                                                                                                             |
| outPath          | نص (String) | استعلام (اختياري)    | مسار المجلد في التخزين حيث سيُحفظ ملف جدول العمل الناتج. إذا حُذف، تُعاد النتيجة في جسم الاستجابة.                                              |
| outStorageName   | نص (String) | استعلام (Query)      | اسم التخزين المراد استخدامه لملف الإخراج.                                                                                                       |
| region           | نص (String) | استعلام (Query)      | إعداد إقليم ورقة العمل (مثل `US`، `EU`).                                                                                                        |
| password         | نص (String) | استعلام (Query)      | كلمة المرور لفتح ملف جدول العمل المحمي.                                                                                                         |

**مثال على طلب cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/extract/text?extractTextType=Before&beforeText=Total&outPositionRange=Sheet1!B1&worksheet=Sheet1&range=A1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx"
```

### **الاستجابة**

عند نجاح الطلب، تُعيد واجهة API حمولة JSON تحتوي على النص المستخرج وعنوان الخلية التي كُتب فيها:

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

إذا وُفر معامل `outPath`، تحتوي الاستجابة فقط على رسالة حالة؛ ويُكتب ملف جدول العمل في الموقع المحدد.

**مثال على استجابة عند حذف `outPath`**

```json
{
  "Code": 200,
  "Status":"OK"
}
```

### رموز الأخطاء

- **200 OK** – اكتمل الاستخراج بنجاح.  
- **202 Accepted** – تم قبول الطلب للمعالجة غير المتزامنة.  
- **400 Bad Request** – عنوان URI غير صالح لواجهة Aspose.Cells Cloud API أو معاملات مطلوبة مفقودة.  
- **401 Unauthorized** – رمز وصول غير صالح أو مُعرِّف العميل أو سر العميل غير صحيح.  
- **404 Not Found** – لا يمكن الوصول إلى ملف ورقة العمل المحدد.  
- **500 Server Error** – حدث خطأ غير متوقع أثناء معالجة ملف جدول العمل.

## مواصفات OpenAPI

تُعرِّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ExtractText) واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

### استخدام حزم Aspose.Cells Cloud SDK

استخدام SDK هو أفضل طريقة لتسريع التطوير. وتتولى SDK تفاصيل التنفيذ الأساسية، مما يتيح لك تنفيذ **استخراج النص** للخلايا بحد أدنى من الكود. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم Aspose.Cells Cloud SDK.

توضح الأمثلة التالية كيفية إجراء مكالمات إلى خدمات Aspose.Cells الويب باستخدام حزم SDK المختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{<tab tabNum="1" >}}

```csharp
// مثال بلغة C# – استخراج النص (حُذف الكود للإيجاز)
```

{{</tab>}}

{{<tab tabNum="2" >}}

```java
// مثال بلغة Java – استخراج النص (حُذف الكود للإيجاز)
```

{{</tab>}}

{{<tab tabNum="3" >}}

```php
// مثال بلغة PHP – استخراج النص (حُذف الكود للإيجاز)
```

{{</tab>}}

{{<tab tabNum="4" >}}

```ruby
# مثال بلغة Ruby – استخراج النص (حُذف الكود للإيجاز)
```

{{</tab>}}

{{<tab tabNum="5" >}}

```javascript
// مثال بلغة Node.js – استخراج النص (حُذف الكود للإيجاز)
```

{{</tab>}}

{{<tab tabNum="6" >}}

```python
# مثال بلغة Python – استخراج النص (حُذف الكود للإيجاز)
```

{{</tab>}}

{{<tab tabNum="7" >}}

```perl
# مثال بلغة Perl – استخراج النص (حُذف الكود للإيجاز)
```

{{</tab>}}

{{<tab tabNum="8" >}}

```go
// مثال بلغة Go – استخراج النص (حُذف الكود للإيجاز)
```

{{</tab>}}

{{< /tabs >}}