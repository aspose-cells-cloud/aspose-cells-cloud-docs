---
title: "تحويل ملف Excel إلى JSON"
second_title: "الوثيقة"
linktitle: "تحويل ملف Excel إلى JSON"
type: docs
url: /convert-excel-file-to-json-file/
keywords: "Aspose.Cells, تحويل ملف Excel إلى JSON, واجهة برمجة التطبيقات السحابية, تحويل جداول البيانات, واجهة REST API"
description: "تعرّف على كيفية تحويل جداول بيانات Excel إلى ملفات JSON باستخدام واجهة Aspose.Cells Cloud REST API. يشمل مثالًا بـ cURL، ومقتطفات SDK (C#، Java، Python)، والمعلمات المطلوبة، والمصادقة، وتنسيق الاستجابة."
weight: 100
ArticleTitle: "تحويل ملف Excel إلى JSON باستخدام واجهة Aspose.Cells Cloud API – دليل سريع"
---

## واجهة برمجة التطبيقات REST

تقوم هذه واجهة برمجة التطبيقات REST بتحويل ملف جدول بيانات إلى ملف بصيغة JSON.

```http
POST https://api.aspose.cloud/v3.0/cells/convert/json
```

### الأمان والمصادقة

تُعد واجهات برمجة التطبيقات السحابية لـ Aspose.Cells آمنة وتشترط [المصادقة القائمة على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### الطلب

**معلمات الاستعلام**

| اسم المعلمة            | النوع   | الوصف                                                                      |
| ----------------------- | ------ | -------------------------------------------------------------------------- |
| `password`              | string | كلمة المرور المطلوبة لفتح ملف Excel (اختيارية).                            |
| `storageName`           | string | اسم وحدة التخزين التي يوجد فيها الملف (اختيارية).                           |
| `checkExcelRestriction` | bool   | يُطبّق قيودًا محددة بـ Excel عند تعديل الخلايا (اختياري).                   |

**معلمة جسم الطلب**

| اسم المعلمة | النوع | الوصف                                                                                           |
| ----------- | ---- | ----------------------------------------------------------------------------------------------- |
| `datafile`  | file | ملف Excel المراد رفعه. يجب إرساله كجزء أول في طلب بصيغة `multipart/form-data`.                   |

#### مثال على استدعاء cURL

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

### الاستجابة

تُعيد الخدمة كائن **FileInfo**. تُوضّح الحقول الأساسية أدناه:

| الحقل         | النوع    | الوصف                                                                     |
| ------------- | ------- | ------------------------------------------------------------------------- |
| `Filename`    | string  | اسم ملف JSON الذي تم إنشاؤه (مثل `myWorkbook.json`).                      |
| `FileSize`    | integer | حجم الملف الذي تم إنشاؤه بالبايتات.                                        |
| `FileContent` | string  | محتوى ملف JSON مشفرًا بنظام Base64. فك التشفير لاسترجاع محتوى JSON الفعلي. |

**مثال على استجابة**

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH ... (سلسلة base64) ..."
}
```

#### معالجة الأخطاء

إذا فشل الطلب، تُعيد واجهة برمجة التطبيقات كائن خطأ بالهيكل التالي:

| الحقل     | النوع   | الوصف                                      |
| --------- | ------ | ------------------------------------------ |
| `Code`    | string | معرّف خطأ قابل للقراءة بواسطة الآلة.       |
| `Message` | string | وصف قابل للقراءة بواسطة الإنسان للخطأ.     |

رموز الحالة HTTP الشائعة:

- **400** – طلب غير صالح (مثل: ملف مفقود أو معلمات غير صحيحة).
- **401** – غير مُصادَق (رمز وصول غير صالح أو مفقود).
- **500** – خطأ داخلي في الخادم.

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                             |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح                         | تمت تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح                 | معلمات مفقودة أو غير صالحة (مثل: نوع ملف غير مدعوم). |
| 401  | غير مُصادَق                   | رمز JWT غير صالح أو مفقود. |
| 413  | حجم الحمولة كبير جدًا          | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500  | خطأ داخلي في الخادم           | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostConvertWorkbookToJson API باستخدام SDKs

### مواصفات واجهة PostConvertWorkbookToJson API

تُعرّف <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson" rel="noopener noreferrer" title="مواصفات OpenAPI لـ Aspose.Cells – تحويل ملف عمل إلى JSON">مواصفات OpenAPI</a> واجهة برمجة تطبيقات قابلة للوصول بشكل عام وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يُظهر المثال التالي كيفية إجراء استدعاءات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH... (سلسلة base64)"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. تتعامل SDK مع التفاصيل منخفضة المستوى لتمكينك من التركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer" title="SDKs الخاصة بـ Aspose.Cells Cloud على GitHub">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء استدعاءات لخدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToJson.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToJson.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToJson.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToJson.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToJson.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToJson.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToJson.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToJson.go" >}}

{{< /tab >}}

{{< /tabs >}}

## واجهات برمجة تطبيقات أخرى تُنفّذ وظائف مماثلة

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – تحفظ ملف Excel كملف HTML مع إعدادات إضافية وتخزن النتيجة في وحدة التخزين المحددة.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – تحول ملف Excel إلى ملف HTML مع إعدادات إضافية وترد بالنتيجة في الاستجابة.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – تسترجع ملف Excel؛ يمكن استخدامها مع معلمات استعلام للحصول على الملف بصيغة HTML.