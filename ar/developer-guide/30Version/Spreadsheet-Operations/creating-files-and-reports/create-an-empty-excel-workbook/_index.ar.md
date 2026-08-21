---
title: "إنشاء مصنف Excel فارغ"
second_title: "مستند"
linktitle: "مصنف فارغ"
type: docs
url: /create-an-empty-excel-file/
aliases:
  [
    /create-an-empty-excel-workbook/,
    /workbook/new/,
    /workbook/create/empty-workbook/,
  ]
keywords: "Aspose.Cells، السحابة، إكسل، مصنف فارغ، REST API، SDK"
description: "تعلم كيفية إنشاء مصنف إكسل فارغ باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن أمثلة باستخدام cURL و SDKs."
weight: 20
ArticleTitle: "إنشاء مصنف إكسل فارغ باستخدام واجهة Aspose.Cells Cloud API"
---

تقوم هذه الواجهة البرمجية REST بإنشاء **مصنف فارغ**.

## PutWorkbookCreate API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الاستعلام

| اسم المعامل | النوع   | الوصف                                                      |
|-------------|---------|------------------------------------------------------------|
| templateFile| string  | مسار ملف مصنف قالب لاستخدامه كأساس (اختياري).             |
| dataFile    | string  | مسار ملف بيانات لتعبئة المصنف به (اختياري).                |
| isWriteOver | boolean | `true` للكتابة فوق الملف الموجود؛ و `false` خلاف ذلك.      |
| folder      | string  | المجلد الوجهة للمصنف الذي تم إنشاؤه (اختياري).             |
| storageName | string  | اسم خدمة التخزين المراد استخدامها.                         |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف                                           |
|-------------|-------|-------------------------------------------------|
| data        | file  | المحتوى الثنائي لملف المصنف المراد إنشاؤه.      |

### **الاستجابة**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**رموز حالة HTTP**

| الرمز | المعنى                        | وقت الإرجاع                              |
|-------|-------------------------------|------------------------------------------|
| 200 OK | تم إنشاء المصنف بنجاح          | التدفق الطبيعي                           |
| 201 Created | تم إنشاء المصنف (استجابة بديلة) | عندما تُعيد الواجهة البرمجية حالة "تم الإنشاء" |
| 400 Bad Request | معاملات غير صالحة         | خطأ من جانب العميل                        |
| 401 Unauthorized | رمز مفقود أو غير صالح     | خطأ في المصادقة                          |
| 409 Conflict | الملف موجود و `isWriteOver=false` | تضارب مع الملف الموجود                   |

## كيفية استخدام PutWorkbookCreate API باستخدام SDKs

### مواصفات PutWorkbookCreate API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) واجهة برمجة تطبيقات قابلة للوصول العام وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells عبر الويب. تضمين رأس `Authorization` مع رمز وصول OAuth2/JWT ساري المفعول. بالنسبة لمصنف فارغ، يكون جسم الطلب اختياريًا؛ وإذا احتجت إلى رفع ملف، أضف `--data-binary @empty.xlsx` كما هو موضح أدناه.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# إنشاء مصنف فارغ باسم newworkbook.xlsx
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     --data-binary @empty.xlsx   # احذف هذا السطر للمصنف الفارغ تمامًا
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

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فهي تُجرّدك من التفاصيل منخفضة المستوى لتتمكن من التركيز على مهام مشروعك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateEmpty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateEmpty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateEmpty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateEmpty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateEmpty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateEmpty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateEmpty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateEmpty.go" >}}

{{< /tab >}}

{{< /tabs >}}
---